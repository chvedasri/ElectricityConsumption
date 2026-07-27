# Electricity Consumption Analysis in India

**Interactive Tableau and Flask web application analyzing state-wise electricity consumption across India (2019–2020) — built for state discom planners, policy analysts, and researchers to uncover regional trends and understand the impact of 2020's disruptions on power demand.**

Electricity consumption data across Indian states is publicly available but scattered and inconsistent, making it difficult to compare regions or spot trends. This project transforms raw state consumption records into a structured Microsoft SQL Server pipeline, an interactive Tableau solution — 10 visualizations, 4 dashboards, and a guided Story — and a Flask web application that makes the analysis accessible from any browser without installing SQL Server or Tableau.

---

## Quick Links

| Resource | Link |
|---|---|
| **GitHub Repository** | [github.com/chvedasri/ElectricityConsumption](https://github.com/chvedasri/ElectricityConsumption/tree/main) |
| **Dataset** | [Google Drive link](https://drive.google.com/file/d/1JxIkHNwXxjFztKq7ad0_KtkukCqTckNy/view) |

---

## Overview

Electricity is a vital driver of economic activity, and its consumption reflects both industrial productivity and household energy access. In 2015–16, agriculture accounted for the highest share (17.89%) of electric energy usage in India. Despite the country's relatively low electricity tariffs, its per capita electricity consumption remains below global averages, indicating both growth potential and infrastructural challenges.

The COVID-19 pandemic introduced a unique scenario for energy consumption analysis. With lockdowns enforced across India, various sectors saw drastic shifts in energy usage — some declining due to shutdowns (e.g., industries, transportation), and others rising (e.g., residential).

This project focuses on an in-depth analysis of electricity consumption patterns across Indian states from January 2019 to December 5, 2020, covering a crucial period including the COVID-19 pandemic and nationwide lockdown (March–June 2020). The dataset offers an exhaustive view of state-wise electricity usage and provides a foundation for understanding regional and national energy trends.

**Scenario 1 – Change in Overall Consumption Trends**
From January 2019 to December 2020, India's electricity consumption patterns underwent significant changes influenced by seasonal demand variations, economic growth fluctuations, and the impact of the nationwide COVID-19 lockdown. Tracking month-by-month consumption over this period highlights how national electricity usage shifted compared to previous years, revealing both expected and unusual consumption patterns.

**Scenario 2 – Regional Variations in Demand**
Electricity consumption did not follow the same pattern across all regions of India. Northern, Southern, Eastern, Western, and Northeastern states experienced differing usage levels due to climate, industrial presence, and population density. Comparing these regions from January 2019 to December 2020 helps in understanding uneven electricity demand distribution and identifying areas of higher or lower growth.

**Scenario 3 – Recovery After Lockdown**
Following the COVID-19 restrictions, electricity demand began to recover, but the pace of recovery differed widely across states. Some states quickly reached or exceeded pre-lockdown levels, while others lagged behind. Evaluating this recovery phase between mid-2020 and the end of 2020 reveals how economic activity and energy needs rebounded in diverse ways.

**Dataset coverage:** All Indian states/union territories · 5 power regions (ER, NER, NR, SR, WR) · January 2019 – December 5, 2020

---

## Key Features

- **State Consumption Maps (2019 & 2020)** — geographic view of state-level consumption for each year
- **Total Consumption Chart** — ranked bar chart comparing every state across both years
- **Usage By Region Chart** — regional (ER/NER/NR/SR/WR) comparison of 2019 vs 2020
- **Top N / Bottom N Charts** — instantly surfaces the highest- and lowest-consuming states, adjustable via a parameter
- **Quarter-wise & Month-wise Charts** — captures when in the year the 2020 decline occurred
- **Usage By Year Trend Line** — month-by-month trend across both years
- **4 Dashboards** — Overview, Overall Consumption Trends, Regional Variations in Demand, and Recovery After Lockdown
- **7-Point Guided Story** — "Electricity Consumption in India (2019–2020)"
- **Flask Web Application** — Home, Dashboard, Story, Visualizations, and Conclusion pages

---

## Who This Is For

| Scenario | Question They Need Answered | How the Dashboard Helps |
|---|---|---|
| **Scenario 1 — Overall Consumption Trends** | How did India's national electricity usage shift month-by-month from January 2019 through December 2020, and where do the expected vs. unusual patterns show up? | Usage By Year trend line, Month-wise and Quarter-wise charts |
| **Scenario 2 — Regional Variations in Demand** | How did consumption levels differ across Northern, Southern, Eastern, Western, and Northeastern states, and what does that reveal about uneven demand distribution? | State Consumption Maps, Usage By Region chart, Top N / Bottom N charts |
| **Scenario 3 — Recovery After Lockdown** | After the mid-2020 lockdown, which states recovered quickly and which lagged behind pre-lockdown levels? | Quarter-wise and Month-wise charts (mid-2020 to end of 2020), Total Consumption chart |

---

## Technology Stack

| Layer | Technology |
|---|---|
| Data Source | CSV/Excel — state-wise electricity consumption data, Jan 2019–Dec 2020 |
| Data Cleaning & Aggregation | Microsoft SQL Server, T-SQL |
| Visualization & Dashboards | Tableau Desktop / Tableau Public |
| Geographic Mapping | Tableau built-in mapping |
| Web Framework | Flask (Python) |
| Frontend | HTML, CSS |
| Version Control | Git & GitHub |

---

## Data Preparation

The raw state consumption dataset was cleaned and aggregated using Microsoft SQL Server before connecting to Tableau:

1. Removed duplicate and blank rows
2. Standardized state and region name spellings
3. Mapped every state to its power region (ER, NER, NR, SR, WR)
4. Derived Year, Quarter, and Month fields from the date column for time-based charts
5. Aggregated consumption by state, region, quarter, and month via T-SQL queries
6. Exported clean, query-ready tables for Tableau to connect to

**Known limitation:** the dataset covers January 2019 to December 5, 2020, so longer-term multi-year trends cannot yet be assessed; consumption figures are state-level totals, without district-level granularity.

Full preprocessing steps and business questions: `5. Project Development Phase/Preprocessing Steps and Business Questions`

---

## Repository Structure

All project deliverables are organized following the 7-phase project structure:

```
1. Ideation Phase/                → Define Problem Statements, Empathy Map Canvas,
│                                    Brainstorming - Idea Generation - Prioritization
2. Requirement Analysis/          → Customer Journey Map, Data Flow Diagram and
│                                    User Stories, Solution Requirements,
│                                    Technology Stack
3. Project Design Phase/          → Problem - Solution Fit, Proposed Solution,
│                                    Solution Architecture
4. Project Planning Phase/        → Project Planning (Product Backlog, Sprint
│                                    Planning, Stories, Story Points)
5. Project Development Phase/     → Dataset Description, Preprocessing Steps and
│                                    Business Questions, Dashboard and Story
│                                    Screenshots
6. Performance Testing Phase/     → Performance Testing
7. Project Documentation/         → Final Report
8. Project Demonstration/         → Demonstration Video
```

Each document is provided in both `.docx` and `.pdf` format.

---

## Business Questions Answered

| # | Question | Answered By |
|---|---|---|
| 1 | How did national electricity usage shift month-by-month across 2019–2020? | Usage By Year trend line |
| 2 | How did each state's consumption change between 2019 and 2020? | 2019 & 2020 State Consumption Maps |
| 3 | Which states consume the most overall? | Total Consumption chart |
| 4 | Which regions were hit hardest by the 2020 decline? | Usage By Region chart |
| 5 | Which states have the highest and lowest consumption? | Top N / Bottom N charts |
| 6 | When during the year did the 2020 decline occur, and how did recovery differ by state? | Quarter-wise and Month-wise charts |

Full detail with screenshots: `5. Project Development Phase/Dashboard and Story Screenshots`

---

## Demonstration Video

A full walkthrough of the dashboards, Story, and Flask web application is available in:
`8. Project Demonstration/Video_Demo.mp4`

---

## Final Report

The complete project report — "Plugging Into the Future: An Exploration of Electricity Consumption Patterns" — covering introduction, ideation, requirement analysis, design, planning, testing, results, advantages/disadvantages, conclusion, and future scope, is available in:
`7. Project Documentation/Final Report`

---

## License

This project uses publicly available electricity consumption data for educational and analytical purposes.
