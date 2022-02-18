1. why indexing?

- speed up read queries

2. what indexing do?

- create an aux table that contains indexed columns

3. terms:

- heap fetches: select fields outside index table (slower)
- bitmap index
- parallel seq scan: do seq scan with multiple workers

4. phases of querying?

- planning
- execution

5. b-tree index:

6. explain analyze:

- Index **only** scan (heap fetches: 0): use only index table, no outside fields selected
- Index scan: other than index table, select from additional tables
- Bitmap Heap Scan

7. exceptions:

- `select name from employees where name like '%ha%';` will not use index => slow.
- pk is often stored with index (mysql) ???

8. how to create index:

- `create index idx_employees_name on employees(name);`

9. create table with a million rows

- ref: https://www.dbrnd.com/2016/04/postgresql-how-to-generate-a-random-token-string/

```console
docker run -d -e POSTGRES_PASSWORD=123456 --name pg postgres
docker exec -it pg psql -U postgres
create table temp(t int);
insert into temp (t) select random()*100 from generate_series(0, 1000000);
```

```console
docker run -d --platform linux/amd64 --name mysql57 -e MYSQL_ROOT_PASSWORD=123456 -e MYSQL_ROOT_HOST=% mysql:5.7
docker exec -it mysql57 bash
mysql -u root -p
```
