# Uber Trip Data Analysis

This project analyzes Uber trip data collected over the year 2016, focusing on business-related rides. The goal is to explore patterns and insights regarding trip purposes, timing, distance, and frequency.

## Dataset

- Contains 1156 records with columns:
  - `START_DATE`, `END_DATE`: Trip start and end timestamps
  - `CATEGORY`: Trip category (mostly business)
  - `START`, `STOP`: Start and stop locations
  - `MILES`: Distance traveled in miles
  - `PURPOSE`: Reason for the trip (e.g., Meeting, Customer Visit)

- Requires cleaning such as handling missing values and converting date columns to datetime.

## Data Cleaning & Feature Engineering

- Missing `PURPOSE` values are filled with `"NOT"`.
- Converted date columns to datetime objects.
- Extracted new features:
  - `date`: Date portion of start datetime
  - `time`: Hour of trip start
  - `day-night`: Categorizes time of day into Morning, Afternoon, Evening, Night
  - `MONTH`: Month label (Jan, Feb, etc.)
  - `DAY`: Weekday label (Mon, Tues, etc.)
- Dropped rows with missing or invalid datetime values.

## Exploratory Data Analysis (EDA)

- Visualized trip counts by:
  - `CATEGORY`
  - `PURPOSE`
  - `day-night`
  - `DAY` (weekday)
  - `MONTH`
- Analyzed trip distances (`MILES`) distribution with boxplots and histograms focusing on trips less than 40 miles.
- Revealed insights on peak trip times, common trip purposes, and distance trends.

## Tools and Libraries Used

- Python
- Pandas
- Matplotlib
- Seaborn
- NumPy

## Usage

1. Place `UberDataset.csv` in the project directory.
2. Run the Jupyter notebook or Python script to perform cleaning, feature engineering, and visualization.
