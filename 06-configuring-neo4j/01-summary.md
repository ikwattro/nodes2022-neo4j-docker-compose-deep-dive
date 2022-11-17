* Neo4j can be configured with environment variables
** prefix is `NEO4J_` 
** Replace format is `_` for `.` and `__` for `_` from original setting to environment variable

* Settings have an order of precedence
** 1. neo4j.conf
** 2. environment variable value overrides neo4j.conf value

* Changes in environment are only applied if using `docker compose up` command

