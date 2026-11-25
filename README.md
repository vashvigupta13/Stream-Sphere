# StreamSphere OTT Platform: Content & User Engagement Analysis

MBA End-Term Project, SQL and Data Management (PMDE30605), IILM University, Greater Noida.

A PostgreSQL database for a hypothetical OTT streaming platform. It links users, content, subscriptions, viewing history, ratings and payments, cleans the data and answers content, engagement and revenue questions with SQL.

## Group members

Shruti Saraswat, Khushi Sharma, Vashvi Gupta, Harshit Shukla, Priyal Patel

Faculty: Dr. Lalit Kumar

## Repository contents

```
README.md                                   project summary and run instructions
data/                                       six CSV files and data_dictionary.csv
sql/streamsphere_project.sql                full SQL script (sections 1 to 10)
report/StreamSphere_Project_Report.pdf      project report (ER diagram, queries, outputs, insights)
```

## How to run

1. In pgAdmin, create a database: `CREATE DATABASE streamsphere;` and open a Query Tool on it.
2. Run **Section 1** of `sql/streamsphere_project.sql` to create the tables and indexes.
3. Import the CSV files (right-click table > Import/Export Data, Format csv, Header on) in this order:
   users, content, subscriptions, viewing_history, ratings, payments.
4. Run the rest of the script from **Section 2** onwards.

## What the script covers

| Section | Content |
|---------|---------|
| 1 | Table creation: primary keys, foreign keys, CHECK constraints, indexes |
| 2-3 | Table verification and data load |
| 4-6 | Data quality checks, cleaning (blank cities, genre labels), verification |
| 7 | Ten analysis queries: joins, aggregation, CASE, subqueries, CTE, RANK() window function, DATE_TRUNC |
| 8 | Integrity audit: revenue at risk, payment failures, cancellation rate, cross-table date checks |
| 9 | Constraint tests (invalid inserts rejected) |
| 10 | Transactions: COMMIT, ROLLBACK, SAVEPOINT on a subscription renewal |

## Key findings

- Movies are 17 of 40 titles but 57.9% of watch minutes; series have higher completion (73.6% vs 64.0%).
- The most-watched title, *Midnight Run*, has the lowest average rating (1.91).
- Premium and Standard earn 77% of revenue, but Standard has a 27.6% cancellation rate.
- ₹7,980 (18.2% of billed value) is failed or pending.

The dataset is hypothetical and was created for this course project.

