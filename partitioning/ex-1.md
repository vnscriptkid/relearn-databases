## Exercise

- 1. Create a container that runs postgres inside
- 2. Run the container, get into container's cli, runs psql
- 3. Create a new table `grades`
- 4. insert 10 mil records into `grades`
- 5. create index for `grades` on `g` column
- 6. run queries on `grades` and do analyze it
- 7. create a partitioned table by range as a placeholder (not storing actual data)
- 8. Create actual partitioned tables:
- 9. attach placeholder with each partitioned table:
- 10. copy from original table to partitioned table placeholder, data is auto-distributed to partitions:
- 11. create index for leader partitioned table:
- 12. compare perf btw original table and partition table:
