# PostgreSQL Optimizer Analysis

This repository contains selected PostgreSQL 18.4 source directories for SWE3003 Database Systems Assignment #4.

Uploaded directories:

- `src/backend`
- `src/include`

Main analysis focus:

- SQL query entry and parsing flow
- Query analysis and rewrite
- Query planning and optimization
- Join order search
- Cost estimation
- Path and plan generation

Important starting points:

- `src/backend/tcop/postgres.c`
  - `PostgresMain()`
  - `exec_simple_query()`
  - `pg_parse_query()`

- `src/backend/optimizer/plan/planner.c`
  - `planner()`
  - `standard_planner()`
  - `subquery_planner()`
  - `grouping_planner()`

- `src/backend/optimizer/path/allpaths.c`
  - relation path generation

- `src/backend/optimizer/path/joinrels.c`
  - join relation construction and join order search

- `src/backend/optimizer/path/joinpath.c`
  - join path generation

- `src/backend/optimizer/path/costsize.c`
  - cost estimation

- `src/include/nodes/pathnodes.h`
  - planner data structures such as `PlannerInfo`, `RelOptInfo`, and `Path`
