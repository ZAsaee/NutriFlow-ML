## 2025-06-14 — Raw Drop v0.1

* **Object key:** s3://nutriflow-pipeline /raw/food-facts/v0.1/food_facts_20250614.gz  
* **Local size:** 4 237 891 654 bytes  
* **S3 size:**    4 237 891 654 bytes (match)  
* **Delimiter:**  '\t'  
* **Encoding:**   UTF-8 (no � chars in first 50 rows)  
* **Notes:** Header row present, 158 columns.

## 2025‑06‑15 – Glue job dry‑run
* **Job:** ff_flatten_nutrients_dev  ✔
* **Role:** foodfacts‑dev‑glue
* **Script URI:** s3://nutriflow‑pipeline/scripts/flatten_nutrients.py
* **Result:** Succeeded, log message seen.

## 2025‑06‑15 – Crawler + Athena sanity
* **Database:** foodfacts_phase_a  ✔
* **Table:** ff-partial-phasea
* COUNT(*) = 30_000 rows
* **Label counts:** a = 5703, b = 2311 , c = 3133 , d = 4848 , e = 9417, unknown = 4443 , not-applicable = 145
