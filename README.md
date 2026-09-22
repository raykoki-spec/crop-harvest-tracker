# File: README.md

# Farm Harvest Tracker

A crop harvest tracker for both small scale and large scale farmers.
Reads farm data from a csv file, computes total bags harvester per crop and compares it to the set target.

## What It Does

- Logs farm harvest data from a CSV file
- Computes and assign the total harvested bags for each crop
-Checks if each crop surpassed the set target 
- Formats a clear report

## Setup

```bash
pip install -r requirements.txt
```

## Usage

```python
for row in reader:
    harvested = int(row["bags_harvested"])
    target = int(row["target_bags"])
    pct = (harvested / target) * 100
    status = "On target" if harvested >= target else f"Short by {target - harvested} bags"
    print(f"{row['field']:<15} {row['crop']:<10} {harvested:>10} {target:>8} {status:>12}")
```

## Sample Output

```
North Plot      Maize              48       50 Short by 2 bags
South Plot      Beans              22       30 Short by 8 bags
East Plot       Wheat              61       55    On target
```

## Stack

Python

Built-in modules: `csv`, `io`
