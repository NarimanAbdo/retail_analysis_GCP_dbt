retail_analysis_GCP_dbt/
├── models/
│   ├── staging/         # Cleaned layer of raw data
│   ├── marts/           # Business logic and aggregated metrics
│   └── snapshots/       # SCD tracking (optional)
├── macros/              # Reusable SQL macros
├── seeds/               # Static CSV data
├── tests/               # Custom test logic
├── dbt_project.yml      # Project config
├── profiles.yml.example # Sample profile for dbt connection
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
