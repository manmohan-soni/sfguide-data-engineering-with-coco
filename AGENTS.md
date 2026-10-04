# AGENTS.md

## Snowflake Environment

- **Account:** THDNLYY-XV80350
- **Database:** DEMO_DB
- **Schema:** TPCH_TRANSFORMED
- **Warehouse:** DEMO_WH
- **Role:** DEMO_ROLE
- **dbt Profile:** coco_de_guide

## dbt Commands

Build all models:

```bash
dbt build --project-dir dbt/
```

Build a single model:

```bash
dbt build --select <model_name> --project-dir dbt/
```

## Conventions

- Model files use **snake_case** naming (e.g., `fct_orders.sql`, `dim_customers.sql`).
- All raw tables from `SNOWFLAKE_SAMPLE_DATA.TPCH_SF1` must be referenced through `_sources.yml` -- never hardcode source table references directly in models.

## Git Workflow

- Feature branches follow the pattern: `feature/<description>`
- PRs are required before merging to `main`

## Tooling

- This project uses **CoCo Desktop**. Do not use the `cortex` CLI command.
