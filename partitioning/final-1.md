## Exercise

- 1. Create a container that runs postgres inside
- 2. Run the container, get into container's cli, runs psql

```console
docker-compose up -d
docker exec -it postgres-partitioning-practice bash
psql -U postgres
```

- 3. Create a new table `grades`

```sql
create table grades
(
    id serial not null,
    g int not null
)
```

- 4. insert 10 mil records into `grades`

```sql
insert into grades (g) select floor(random() * 100) from generate_series (0, 10000000)
```

- 5. create index for `grades` on `g` column

```sql
create index grades_index on grades(g);
```

- 6. run queries on `grades` and do analyze it

```sql

```

- 7. create a partitioned table by range as a placeholder (not storing actual data)

```sql
create table grades_parts (id serial not null, g int not null) partition by range(g);
```

- 8. Create actual partitioned tables:

```sql
create table g0035 (like grades_parts including indexes);
create table g3560 (like grades_parts including indexes);
create table g6080 (like grades_parts including indexes);
create table g80100 (like grades_parts including indexes);
```

- 9. attach placeholder with each partitioned table:

```sql
alter table grades_parts attach partition g0035 for values from (0) to (35);
alter table grades_parts attach partition g3560 for values from (35) to (60);
alter table grades_parts attach partition g6080 for values from (60) to (80);
alter table grades_parts attach partition g80100 for values from (80) to (100);
```

- 10. copy from original table to partitioned table placeholder, data is auto-distributed to partitions:

```sql
insert into grades_parts select * from grades;
```

- 11. create index for leader partitioned table:

```sql
create index grades_parts_idx on grades_parts(g);
```

- 12. compare perf btw original table and partition table:

```sql
explain analyze select count(*) from grades where g = 30;
explain analyze select count(*) from grades_parts where g = 30;
```
