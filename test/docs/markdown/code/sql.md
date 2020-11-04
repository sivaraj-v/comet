# SQL syntax

```sql
-- Syntax for SQL Server and Azure SQL Database

[ WITH <common_table_expression> [ ,...n ] ]
DELETE
    [ TOP ( expression ) [ PERCENT ] ]
    [ FROM ]
    { { table_alias
      | <object>
      | rowset_function_limited
      [ WITH ( table_hint_limited [ ...n ] ) ] }
      | @table_variable
    }
    [ <OUTPUT Clause> ]
    [ FROM table_source [ ,...n ] ]
    [ WHERE { <search_condition>
            | { [ CURRENT OF
                   { { [ GLOBAL ] cursor_name }
                       | cursor_variable_name
                   }
                ]
              }
            }
    ]
    [ OPTION ( <Query Hint> [ ,...n ] ) ]
[; ]

<object> ::=
{
    [ server_name.database_name.schema_name.
      | database_name. [ schema_name ] .
      | schema_name.
    ]
    table_or_view_name
}
```

```sql
-- Syntax for Azure SQL Data Warehouse and Parallel Data Warehouse

DELETE FROM [database_name . [ schema ] . | schema. ] table_name
    [ WHERE <search_condition> ]
    [ OPTION ( <query_options> [ ,...n ]  ) ]
[; ]
```
