## partitioning
- why? speed up query
- how? break down large table into smaller chunks
- types
  - horizontal: by rows
    - range: ids, dates
    - list: zip_code, states
    - hash (consistent hashing)
  - vertical: by columns
    - when? separate large columns (blob) out of table 
