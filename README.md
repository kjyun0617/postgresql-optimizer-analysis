# PostgreSQL Optimizer Analysis

This repository contains selected PostgreSQL 18.4 source files used for SWE3003 Database Systems Assignment #4.

The purpose is to analyze:
- SQL parsing entry point
- Query planning flow
- Join order optimization
- Cost estimation
- Path selection

Main reading path:
1. `src/backend/tcop/postgres.c`
   - `pg_parse_query()`
   - entry point for converting raw SQL text into PostgreSQL raw parse trees

2. `src/backend/optimizer/plan/planner.c`
   - planner flow

3. `src/backend/optimizer/path/joinrels.c`
   - join relation construction and join order search

4. `src/backend/optimizer/path/joinpath.c`
   - join path generation

5. `src/backend/optimizer/path/costsize.c`
   - cost estimation logic

6. `src/backend/optimizer/util/pathnode.c`
   - path node construction and path comparison support

7. `src/include/nodes/pathnodes.h`
   - planner-related data structures such as RelOptInfo and Path
