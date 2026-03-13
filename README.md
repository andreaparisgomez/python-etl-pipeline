# Python ETL Pipeline

This project implements a simple ETL (Extract, Transform, Load) pipeline in Python.

The pipeline extracts data from multiple file formats (CSV, JSON, and XML), transforms the data by converting measurement units, and loads the cleaned data into a single CSV file. The script also logs pipeline progress with timestamps.

## Features

- Extract data from:
  - CSV files
  - JSON files
  - XML files
- Combine all extracted data into a single pandas DataFrame
- Transform data:
  - Convert height from inches to meters
  - Convert weight from pounds to kilograms
- Load the transformed dataset into a CSV file
- Log pipeline execution steps with timestamps

## Technologies Used

- Python
- pandas
- glob
- xml.etree.ElementTree
- datetime

## Project Structure

```
python-etl-pipeline/
│
├── etl_pipeline.py
├── README.md
├── requirements.txt
├── .gitignore
└── sample_data/
    ├── people_1.csv
    ├── people_2.json
    └── people_3.xml
```

The `sample_data` folder contains small example datasets used to demonstrate the ETL pipeline.

## How to Run

1. Install dependencies:
```pip install pandas```

2. Run the ETL pipeline:
```python etl_pipeline.py```

3. The script will:
- extract data from CSV, JSON, and XML files
- transform height and weight units
- save the result to `transformed_data.csv`
- record execution logs in `log_file.txt`

## Example Workflow

```
Raw Data Files
(CSV / JSON / XML)
↓
Extract
↓
Transform
(inches → meters, pounds → kg)
↓
Load
(transformed_data.csv)
↓
Log Execution
```

## Purpose

This project demonstrates a basic ETL workflow and data processing pipeline using Python and pandas.
