# Data Engineering Assignment Documentation

## 1. Assumptions
- Salary range columns are numeric.
- Posting date format is yyyy-MM-dd'T'HH:mm:ss.SSS.
- Records with null salary were removed.

## 2. Data Cleaning
- Standardized column names.
- Removed null salary rows.
- Parsed posting_date into timestamp.
- Created posting_year.

## 3. Feature Engineering
- avg_salary
- salary_diff
- posting_year
- requires_masters flag

## 4. KPIs
- Top 10 job categories
- Salary distribution per category
- Highest salary per agency
- Avg salary last 2 years (dynamic)
- Highest paid skills

## 5. Deployment Approach
- Store raw data in S3
- Spark job triggered via Airflow
- Containerized with Docker
- CI/CD using GitHub Actions

## 6. Trigger Mechanism
- Scheduled daily batch via Airflow DAG
- Alternatively triggered via REST API endpoint

## 7. Challenges
- Date parsing format mismatch
- Column naming inconsistencies
- Docker file mounting issue
