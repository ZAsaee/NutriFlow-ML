s3://nutriflow-pipeline/
├── raw/
│ └── food-facts/
│ └── v0.1/
│ └── food_facts_20250614.gz
└── processed/
└── food-facts/
└── v0.1/
├── parquet/ # partitioned by main_category=*
└── analysis/ # class_counts_v0.1.csv, etc.


Never write back into `raw/`.
