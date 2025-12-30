# IR Domains Archive
A curated archive of all .ir domains collected from Certificate Transparency logs.

## 📝 Purpose

I wanted to collect all domains under the .ir TLD. Existing lists were expensive (ranging from $34 to $433), so I created this personal solution to collect, archive, and maintain the data myself.

This repository contains historical snapshots of .ir domains in CSV and JSON format.

## 📂 Contents

CSV files: ir_domains_YYYYMMDD_HHMMSS.csv

JSON files: ir_domains_YYYYMMDD_HHMMSS.json

Each file is timestamped to track changes over time.


## 💻 How to Use

You can download the CSV or JSON files and:

Open in Excel, Google Sheets, or any CSV/JSON reader

Import into databases or analytics tools

Analyze domain growth over time

Example in Python:


```python
import json

with open("ir_domains_20251229_214500.json") as f:
    data = json.load(f)
print(data[:10])

```

## 💡 Motivation

Existing .ir domain lists were costly and incomplete.
This repository provides a free, continuously updated archive of .ir domains.