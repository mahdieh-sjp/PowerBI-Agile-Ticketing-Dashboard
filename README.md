# Agile Data Demands & Ticketing Dashboard

## Overview
This project is an end-to-end Power BI dashboard designed to track agile team performance and manage data warehouse service requests. It simulates a Jira ticketing environment to monitor SLA compliance, visualize squad workloads, and forecast sprint velocity, mirroring the daily operations of a banking Business Data Delivery Tribe.

## Key Features & Technical Implementations

* **Relational Data Modeling:** Designed a Star Schema architecture connecting a central fact table (F_ServiceRequests) to lookup dimension tables (D_Assignee, D_System).

* **Advanced DAX & KPIs:** Engineered custom measures for 14-day rolling sprint velocity, open ticket backlogs, and dynamic SLA breach flags (48-hour resolution limit).

* **Embedded Data Science:** Bypassed native Power BI visual limitations by embedding a Python/Seaborn script directly into the dashboard to render statistical distributions (Violin Plots) of ticket resolution times.

* **Predictive Analytics ("What-If"):** Implemented an interactive numeric parameter allowing stakeholders to simulate the impact of hiring additional developers on projected sprint velocity.

* **Enterprise Data Governance:** Configured Row-Level Security (RLS) to restrict dashboard views based on login credentials, ensuring squad managers only access data relevant to their specific agile teams.

## Repository Contents

* `Agile_Ticketing_Dashboard.pbix`: The interactive Power BI dashboard file.

* `data_generator.py`: The Python script (using Pandas and NumPy) utilized to synthesize 6 months of relational agile ticketing data and intentional SLA delays.

* `dashboard_ss.png`: A high-resolution image of the final dashboard layout.

## How to View

Clone this repository to your local machine.

Ensure you have Power BI Desktop installed.

Open the .pbix file. (Note: To view the embedded Seaborn visual, a local Python environment with `pandas`, `matplotlib`, and `seaborn` installed must be mapped in Power BI settings).
