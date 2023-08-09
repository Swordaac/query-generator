# query-generator

### The pandas query generator script is used to produce various examples of sql-like pandas queries by performing different types of table operations.

### Usage:

1. input the directories of your csv files and the directories that you want to save the results

2. create the TBL_source object with the pd.DataFrame object and the name of the table.
    eg: c = TBL_source(customer, "customer")

3. add all the foreign key pairs

4. generate base queries, the base queries generation can be customized in the function gen_base_queries(), line 1081

5. for all the queries you have, function get_new_pandas_queries() will give you queries without merging.

6. merge can be performed with a pool of different queries (line 1286).

7. generate_possible_merge_operations() will generate merged queries.

8. steps 5-7 can be repeated to generate more queries.

#### An example is listed in main, started from line 1235.


2022.12.15, Dailun Li


Bugs reported:

### selections may select the columns that does not exist in the source dataframe

    # fixed in 2022.11.27

### exception raised in foreign key detection
    # fixed in 2022.12.3

### create a config file to deal with all customized parameter

### table merges may use the wrong columns

    # notice
    # have trouble fixing the bug, now dealing with try and catch 2022.12.7



