# Analysis of Bike-Sharing Rental Demand Based on Seasonal, Weather and Working-Day Patterns

## 1. Project Overview

This project analyses bike-sharing rental demand using daily rental data from 2011 and 2012. The aim is to understand how seasonal variations, weather conditions, and working-day patterns relate to bicycle rental demand.

Microsoft Excel was used for data cleaning and preprocessing, while Microsoft Power BI was used to create an interactive dashboard and analyse rental trends.

## 2. Dataset Description

- **Dataset:** `day.csv`
- **Data type:** Daily bike-sharing rental records
- **Period covered:** 2011–2012
- **Records:** 731 daily observations
- **Tools:** Microsoft Excel, Microsoft Power BI and GitHub

The dataset contains information about rental counts, casual and registered users, seasons, weather conditions, calendar variables, and environmental measurements.

## 3. Data Cleaning and Preprocessing in Excel

The following steps were performed in Microsoft Excel:

1. Imported the original `day.csv` dataset.
2. Preserved the original data in the `Raw_Data` worksheet.
3. Created a `Cleaned_Data` worksheet for preprocessing.
4. Converted the cleaned data range into an Excel table named `BikeData`.
5. Checked for duplicate records; no duplicates were found during the check.
6. Checked for missing values in the inspected columns.
7. Validated categorical codes, including season, year, month, holiday, weekday, working day, and weather situation.
8. Added a rental validation column to check whether casual and registered rentals add up to the total rental count.
9. Created additional columns to improve readability and analysis.

### Calculated Columns

- **Year:** Converts the year code into 2011 or 2012.
- **SeasonName:** Converts season codes into readable season names.
- **MonthName:** Converts month numbers into month names.
- **DayType:** Identifies records as Working Day or Non-working Day.
- **WeekdayName:** Converts weekday codes into readable weekday names.
- **WeatherCondition:** Converts weather codes into readable descriptions.

The rental validation formula used was:

`=IF([@casual]+[@registered]=[@cnt],"OK","Check")`

## 4. Power BI Analysis

The cleaned `BikeData` table was imported into Microsoft Power BI to create visualisations and analyse rental demand.

### DAX Measures

**Total Rentals**
```DAX
Total Rentals = SUM(BikeData[cnt])
```

**Average Daily Rentals**
```DAX
Average Daily Rentals = AVERAGE(BikeData[cnt])
```

**Casual Rentals**
```DAX
Casual Rentals = SUM(BikeData[casual])
```

**Registered Rentals**
```DAX
Registered Rentals = SUM(BikeData[registered])
```

## 5. Dashboard Visualisations

The dashboard includes the following visuals:

- **KPI Cards:** Total rentals, average daily rentals, casual rentals, and registered rentals.
- **Monthly Rental Trend:** Analyses changes in average daily rentals across the months.
- **Seasonal Rental Analysis:** Compares average daily rentals across seasons.
- **Weather Analysis:** Examines average daily rentals under different weather conditions.
- **User-Type Comparison:** Compares casual and registered rentals across 2011 and 2012.

### Interactive Filters

The dashboard includes slicers for:

- Year
- Season
- Weather condition
- Day type (Working Day / Non-working Day)

These filters allow users to explore demand patterns under different conditions.

## 6. Report Pages

The Power BI report is organised into four pages:

1. **Dashboard:** Displays key performance indicators, rental trends, and interactive filters.
2. **Executive Narrative:** Explains the project background, dataset scope, objectives, and analytical approach.
3. **Key Insights:** Summarises the patterns identified through the dashboard visuals.
4. **Recommended Solutions:** Presents potential operational recommendations based on the observed patterns.

## 7. Key Areas of Analysis

The project focuses on understanding:

- How rental demand varies by month and season.
- How rental demand differs under various weather conditions.
- How rental activity compares between working and non-working days.
- How casual and registered user rentals differ.
- How rental activity changed between 2011 and 2012.

Specific findings should be interpreted using the actual dashboard results. Observed associations do not, by themselves, establish causation.

## 8. Tools and Technologies

- **Microsoft Excel:** Data cleaning, validation, and calculated columns.
- **Microsoft Power BI:** Data modelling, DAX measures, interactive visualisations, and dashboard development.
- **GitHub:** Project documentation and version-controlled project files.

## 9. Limitations

- The analysis covers daily records from 2011 and 2012 only.
- The dataset may not represent present-day rental demand.
- The analysis identifies patterns and associations but does not prove that weather, season, or working-day status directly causes changes in demand.
- Recommendations should be evaluated against newer data before being applied operationally.

## 10. Conclusion

This project demonstrates a data analytics workflow using Excel and Power BI, from data cleaning and validation to interactive visualisation and interpretation. By examining seasonal, weather, and working-day patterns, the dashboard helps users explore changes in bike-sharing rental demand and supports data-informed operational planning.

## 11. Project Files

A suggested GitHub repository structure is:

```text
Bike-Sharing-Rental-Demand-Analysis/
├── README.md
├── day.csv
├── Bike_Sharing_Cleaned.xlsx
├── Bike_Sharing_Rental_Demand_Analysis.docx
└── Bike_Sharing_Dashboard.pdf
```

Include only files that are actually present in your repository. Add the original dataset source URL and any relevant attribution before publishing.
