# ServiceNow-Ticket-Analysis

Overview
Thank you for the opportunity to work on this ITSM data challenge.

While the original instructions suggested using Apache Airflow, DBT, PostgresDB, and Superset, I would like to respectfully mention that I currently specialize in Power BI and SQL for data analysis and dashboarding. Given the moderate size and complexity of the dataset, I felt confident that the entire workflow could be efficiently and effectively completed using Power BI's Power Query and DAX capabilities.

I’ve completed the analysis by loading, transforming, and visualizing the dataset end-to-end in Power BI, and I’ve ensured that the business questions were answered accurately with clear visuals and supporting insights.

Approach & Steps Followed in Power BI
1. Data Ingestion & Cleaning (Power Query)
Imported the ServiceNow ticket dump (CSV file) into Power BI using Power Query.

Applied the following data cleaning steps:
Removed duplicate rows.
Handled null or missing values.
Standardized all date formats (e.g., Created Date, Resolved Date).
Added derived columns:
Extracted Year, Month, and Day from Created Date.
Calculated Resolution Time (Hours) where missing, using Resolved Date - Created Date.

2. Data Transformation & Metric Calculations (DAX)
Created several calculated measures and columns to support the analysis:

Average Resolution Time per:
Category
Priority

Ticket Closure Rate per Assignment Group:


Ticket Closure Rate = 
DIVIDE(
  COUNTROWS(FILTER(Tickets, Tickets[Status] = "Closed")),
  COUNTROWS(Tickets)
)
Monthly Ticket Summary Table:

Aggregated number of tickets.

Calculated average resolution time per month.

Computed closure rate per month using DAX.

3. Dashboard Visuals (Power BI)
Built a comprehensive dashboard answering all the business questions:

Ticket Volume Trends: Line chart showing tickets created over time.

Resolution Time Comparison: Bar chart comparing avg. resolution time across categories.

Closure Rate by Assignment Group: Pie chart and filterable table.

Ticket Backlog View: Table displaying open tickets grouped by priority.

Interactive Filters:
Ticket Closure Rate buckets (Below 80%, 80–85%, etc.)

Additionally:
Created a matrix view showing ticket distribution by State. Added a filter to easily identify assignment groups based on performance tiers.

Assumptions
Resolution Time was considered valid only for tickets with both Created Date and Resolved Date populated.
Closure Rate was based on tickets where Status = Closed.
Priority and Category fields were assumed to be clean and standardized based on the dataset provided.

Deliverables
Power BI (.pbix) file containing all transformations, measures, and dashboards.
Documentation of key insights and narrative points (available upon request or can be included in a presentation/report format).

Final Note
While I understand that the challenge was intended to evaluate familiarity with tools like Airflow, DBT, and Superset, I chose to demonstrate my strong grasp of data analytics and visualization using Power BI and SQL, tools I currently use in my professional role. I believe this approach shows that with the right understanding of data and business needs, impactful analysis can be delivered even with different tools — especially for datasets of this scale.
