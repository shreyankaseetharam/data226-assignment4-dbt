# DATA 226 Assignment 4 - dbt and Snowflake

This repository contains my DATA 226 Assignment 4 implementation using dbt and Snowflake.

## Project components

- Transform models configured as ephemeral CTEs
- Analytics model for `session_summary`
- dbt snapshot for tracking session history
- Data-quality tests for the `sessionId` field

## Project structure

models/
├── source.yml
├── schema.yml
├── transform/
│   ├── user_session_channel.sql
│   └── session_timestamp.sql
└── analytics/
    └── session_summary.sql

snapshots/
└── snapshot_session_summary.sql

sql/
└── raw_setup.sql

## Commands used
dbt debug
dbt compile
dbt run
dbt snapshot
dbt test

## Snowflake objects
The raw source tables are located in: DEMO_DB.RAW
The analytics model is created in: DEMO_DB.ANALYTICS.SESSION_SUMMARY
The snapshot table is created in: DEMO_DB.SNAPSHOT.SNAPSHOT_SESSION_SUMMARY

## Security note
Snowflake credentials, passwords, private keys, passphrases, and profiles.yml are not included in this repository.
