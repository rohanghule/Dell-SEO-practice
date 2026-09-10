Dell SEO Analytics Practice Dataset

Generated for Microsoft Fabric hands-on practice.

Full source files:
1. 01_seo_traffic.csv
2. 02_seo_keyword_performance.csv
3. 03_seo_orders.csv
4. 04_keyword_master.csv
5. 05_page_master.csv
6. 06_country_master.csv
7. 07_product_master.csv
8. 08_ingestion_config.csv

Main dataset date range: 2025-10-01 to 2026-09-30

Approximate row counts:
seo_traffic: 50,500
seo_keyword_performance: 30,000
seo_orders: 10,002
keyword_master: 2,000
page_master: 500
country_master: 10
product_master: 50
ingestion_config: 7

Data quality issues intentionally included:
- duplicate transaction records
- country variations such as USA / United States / US
- device case variations
- null product/page IDs
- negative visits/revenue
- zero visits
- invalid ranking positions
- zero impressions
- invalid order status
- inactive dimension records

Incremental batches are under:
incremental_batches/
batch_01 = Oct 2025-Jan 2026
batch_02 = Feb 2026-May 2026
batch_03 = Jun 2026-Sep 2026
