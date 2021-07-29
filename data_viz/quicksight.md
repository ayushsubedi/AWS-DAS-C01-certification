# QuickSight
https://aws.amazon.com/quicksight/

- Scalable, serverless, embeddable, ML powered BI service built for the cloud
- Offers Pay-per-session pricing, cost effective for large scale deployments
- ML insights to summarize business metrics in plain language or user machine learning to predict outcomes such as anomaly detection or forecasting without prior data science experience
- Ask question using natural language, on all your data, and receive answers in seconds
- User management tools are provided to easily manage and scale users
- SPICE- in memory engine for faster data retrieval (Superfast Parallel in-memory Calculation Engine)
  - Uses columnar storage, in memory, machine code generation
  - accelerates interactive queries on large datasets
- 10 GB of SPICE    
- Not a typical AWS offering
- Data Sources: Redshift, Aurora/RDS, Athena, EC2-hosted databases, Files from S3, JDBC/ODBC, SaaS, Excel, CSV, TSV, Common or extended log format
- Minimal ETL (renaming, calculated field, etc)
- Stories: Guided tours through specific views of an analysis to convey key points
- no upfront costs for liscences
- collaborative analytics
- combine variety of data into one analytics

### Limitations
- minimal ETL
- built to be a ad-hoc tool

### Security
- MFA 
- VPC connectivity (add Quicksight IP address range to your db security groups)
- Row-level security (row granularity)
- Column-level security (column granularity)
- Private VPC access (Elastic Network Interface, AWS Direct Connect)
- Resource access (Must enssure QuickSight is authorised to use Athena/S3/buckets)
- Data access (Create IAM policies to restrict what data in S3 is authorized)
- Users defined via IAM, or email signup
- Active Directory connector with Quicksight enterprise edition
  - All keys are managed by AWS, cannot use customer-provided keys
  - enterprise edition only
  - can tweak security access using IAM if necessary

### Quicksight Machine Learning Insights
- ML-powered anaomaly detection
  - uses random cut forest
  - identify top contributors to significant changes in metrics

- ML-powered forcasting
  - uses random cut forest
  - detects seasonality and trends
  - excludes outliers and imputes missing values

- Autonarratives
  - Adds story/texts to dashboards

- Suggested Insights
  - provides ready to use insights
 
### Visual Types
- AutoGraph
- Bar Charts (stacked, histograms, etc)
- Line graphs (changes over time)
- Scatter plot, heat maps (correlation)
- Pie chart
- Pivot tables (for tabular data)
- Stories (create narratives)
- KPIs 
- Geospatial charts
- donut charts
- gauge charts 
- word clouds


### Pricing
- Annual Standard $9/user/month
- Enterprise $18/user/month
- Extra SPICE (beyond 19GB -> .25(standard), .38(enterprise) /GB/user/month
- Additional features in Enterprise: Active Directory, Encryption at rest

How can you point QuickSight to fetch from your database stored on the EC2 instance in your VPC ?
-> Add Amazon Quicksight IP range to the allowed IPs of the hosted DB
