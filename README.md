# Software-Reliability-Incident-Intelligence-System
An intelligent reliability platform that continuously analyzes application logs, infrastructure metrics, API performance, and system events to detect abnormal behavior, predict potential incidents, identify probable root causes, and provide actionable incident intelligence.


sentinel-ai/
├── README.md
├── LICENSE
├── .gitignore
├── .env.example
├── docker-compose.yml
├── pyproject.toml                 # or requirements.txt for V1
├── Makefile                       # optional developer shortcuts
│
├── docs/
│   ├── architecture.md
│   ├── data_dictionary.md
│   ├── model_cards/
│   │   ├── anomaly_model.md
│   │   └── incident_model.md
│   └── images/
│
├── backend/
│   ├── app/
│   │   ├── main.py
│   │   ├── core/
│   │   │   ├── config.py
│   │   │   ├── logging.py
│   │   │   └── security.py
│   │   ├── api/
│   │   │   ├── routes_health.py
│   │   │   ├── routes_telemetry.py
│   │   │   ├── routes_incidents.py
│   │   │   └── routes_services.py
│   │   ├── schemas/
│   │   │   ├── telemetry.py
│   │   │   ├── incident.py
│   │   │   └── service.py
│   │   ├── db/
│   │   │   ├── session.py
│   │   │   ├── models.py
│   │   │   └── repositories.py
│   │   ├── services/
│   │   │   ├── ingestion.py
│   │   │   ├── aggregation.py
│   │   │   ├── anomaly_service.py
│   │   │   ├── incident_service.py
│   │   │   └── root_cause_service.py
│   │   └── ml/
│   │       ├── feature_builder.py
│   │       ├── inference.py
│   │       └── model_registry.py
│   └── tests/
│       ├── test_ingestion.py
│       ├── test_features.py
│       └── test_incidents.py
│
├── frontend/
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Overview.jsx
│   │   │   ├── Services.jsx
│   │   │   ├── Incidents.jsx
│   │   │   └── IncidentDetail.jsx
│   │   ├── components/
│   │   │   ├── MetricCard.jsx
│   │   │   ├── HealthScore.jsx
│   │   │   ├── TimeSeriesChart.jsx
│   │   │   └── IncidentTable.jsx
│   │   ├── api/client.js
│   │   └── App.jsx
│   └── package.json
│
├── data-science/
│   ├── notebooks/
│   │   ├── 01_eda.ipynb
│   │   ├── 02_feature_engineering.ipynb
│   │   ├── 03_anomaly_detection.ipynb
│   │   ├── 04_incident_prediction.ipynb
│   │   └── 05_root_cause_analysis.ipynb
│   ├── src/
│   │   ├── load_data.py
│   │   ├── preprocess.py
│   │   ├── features.py
│   │   ├── train_anomaly.py
│   │   ├── train_incident.py
│   │   └── evaluate.py
│   ├── artifacts/                 # gitignored trained models
│   └── reports/
│
├── simulator/
│   ├── app.py                     # instrumented demo service
│   ├── traffic_generator.py
│   ├── fault_injector.py
│   └── scenarios/
│       ├── latency_spike.py
│       ├── memory_pressure.py
│       ├── db_slowdown.py
│       └── error_burst.py
│
├── sdk/
│   └── python/
│       ├── sentinelai/__init__.py
│       └── sentinelai/client.py
│
├── scripts/
│   ├── seed_demo_data.py
│   ├── train_models.py
│   └── run_demo.py
│
└── .github/
    └── workflows/
        ├── backend-tests.yml
        └── frontend-build.yml
