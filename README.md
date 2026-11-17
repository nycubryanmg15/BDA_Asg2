# BDA_Asg2

## Download data and preprocess: 
Download dataset of Mar 1 - Nov 13 (27.3 GB)
Go to the assignment 2 folder and run the following in powershell (make alternative arrangements if using bash):

```
New-Item -ItemType Directory -Force -Path ".\gharchive" | Out-Null

# Mar 1–31
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-03-#1-#2.json.gz" "https://data.gharchive.org/2026-03-[01-31]-[0-23].json.gz"

# Apr 1–30
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-04-#1-#2.json.gz" "https://data.gharchive.org/2026-04-[01-30]-[0-23].json.gz"

# May 1–31
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-05-#1-#2.json.gz" "https://data.gharchive.org/2026-05-[01-31]-[0-23].json.gz"

# Jun 1–30
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-06-#1-#2.json.gz" "https://data.gharchive.org/2026-06-[01-30]-[0-23].json.gz"

# Jul 1–30
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-07-#1-#2.json.gz" "https://data.gharchive.org/2026-07-[01-31]-[0-23].json.gz"

# Aug 1–31
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-08-#1-#2.json.gz" "https://data.gharchive.org/2026-08-[01-31]-[0-23].json.gz"

# Sept 1–30
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-09-#1-#2.json.gz" "https://data.gharchive.org/2026-09-[01-30]-[0-23].json.gz"

# Oct 1–31
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-10-#1-#2.json.gz" "https://data.gharchive.org/2026-10-[01-31]-[0-23].json.gz"

# November 1–13
curl.exe --parallel --parallel-max 8 --fail --retry 3 --output "gharchive/2026-11-#1-#2.json.gz" "https://data.gharchive.org/2026-11-[01-13]-[0-23].json.gz"
```

**then run:

```
python scripts/preprocess.py --raw gharchive --out data
```


Run the notebook:
To get proof of the ablated model results, set RUN_ABLATIONS = True. Set it at False for a faster run with final output.


