## List of applications of classic algorithms in Data Engineering

Konrad Burnik

The list below is by no means a complete one.

* Binary Search
  - generally useful when searching for something in a sorted collection
  - when loading JSON files ordered by timestamp, find the exact timestamp when
    the schema of the files had changed
  - finding the optimal amount of memory/disk space needed for loading data
  - finding the optimal chunk size for exporting/loading data in chunks

* BST tree/BTREE
  - used for indexing tables in relational databases, e.g. via BTREE

* Computational Geometry
  - Intersection of lines, polygons, Convex hull
    (used in Geo databases)
  - KD-tree, range tree
    (used for nearest neighbour search e.g. for providing recommendations)

* Graphs
  - BFS traversal for getting users from the same level in hierarchical query
  - DFS traversal in a table organised as (ID, PARENT_ID) to create all paths
    from root to child nodes and store these paths
  - Connected components, finding clusters of data (in a graph database)
    (e.g. used for migrating connected ETL jobs together)

* Topological sort
  - order the DAG of tasks to be migrated/executed in order

* Interpolation
  - Having a metric stored as monthly values, calculate the weekly values as
  arithmetic progression
  - Impute missing values

* Finite differences
  - calculating the speed of loading (based on number of records loaded)

* Priority-queue
  - processing of time-series stream of data while keeping
    track of MIN,MAX,MEDIAN,ApproxCOUNT(?)

* Hashing
  - produce keys for records
  - make lookup tables used when loading rows
  - distinct values in a sliding window
  - storing and generating passwords

* Bloom filter
  - checking for duplicates

* Range-finding (interval arithmetic)
  - finding common overlap between time-ranges
  - finding total time of an activity
  - finding a time slot for scheduling an ETL job

* Parsing
  - converting between formats

* Set arithmetic
  - calculating differences between datasets (e.g. MINUS in SQL)

* Sorting
  - (obviously) ordering of records by key (e.g. ORDER BY in SQL)
  - finding MIN, MAX, MEDIAN

* Bit arithmetic
  - generally useful for all kinds of calculations
  - used for example for bitmap indexes in relational databases
  - implementing Bloom filters (see Bloom Filter)

* Linear programming
  - optimal assignment of computational resources for ETL
  - optimal scheduling of tasks w.r.t. available resources and free time-slots

* Dynamic programming
  - edit distance for strings (for fuzzy matching)
  - knapsack problem (optimal way of loading tasks on a server)
  - finding the optimal execution plan for a SQL query

* Recursion
  - JSON Parsing
  - Hierarchical queries
  - Generating subsets (GROUP BY CUBE)
  - Generating permutations for SQL testing
  - Branch-and-bound SAT solving
    (doing simple correctness check of SQL queries)

* Gauss elimination
  - solving linear systems to find a period
    where certain conditions will be met (e.g. the simplest example
    is when we have a model of the form y = ax + b where
    a and b are parameters, finding a value of period x for a given y)
    
* Nearest Neighbour
  - finding a closest match of a record based on a given metric, e.g. Euclidean distance
