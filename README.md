<h1 align="center">Hi, I'm Erick 👋</h1>

<p align="center">
  <b>Data engineer in air navigation services · researching UAS traffic management</b><br>
  <sub>Ottawa, ON 🇨🇦</sub>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Scala-DC322F?style=flat-square&logo=scala&logoColor=white" alt="Scala">
  <img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL">
  <img src="https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white" alt="Spark">
  <img src="https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white" alt="Databricks">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes">
  <img src="https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="GCP">
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Azure">
</p>

---

### 🛩️ What I work on

A conflict detector never sees the airspace as it is — only as it was when the
last message arrived. My work sits on both sides of that gap: building the
pipelines that move surveillance and telemetry data at scale, and measuring what
happens to safety when that data shows up late.

By day I build big-data pipelines for air traffic analytics. The rest of the
time I write open-source surveillance tooling and run experiments on how
information freshness constrains conflict detection in low-altitude airspace.

---

### 🔬 Research focus

| Area | The question |
|---|---|
| **Age of Information in UTM** | How fresh must a track be before a conflict detector can be trusted with it? |
| **Time-to-conflict prioritization** | When telemetry streams saturate, which event has to be processed first? |
| **Communication delay modelling** | How do latency, jitter and loss on a real link degrade alerting — not a modelled link, a measured one? |
| **Airspace surveillance data** | Getting ASTERIX, ADS-B and UTM track data into forms that support analysis at scale. |

---

### 📦 Projects

**[pyasteryx](https://github.com/franmenjivar/pyasteryx)** &nbsp;
[![PyPI](https://img.shields.io/pypi/v/pyasteryx?style=flat-square)](https://pypi.org/project/pyasteryx/)
[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.22382473-blue?style=flat-square)](https://doi.org/10.5281/zenodo.22382473)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://github.com/franmenjivar/pyasteryx/blob/main/LICENSE)

A fast, **dependency-free**, specification-driven decoder for EUROCONTROL
**ASTERIX** surveillance data. Live UDP/multicast and PCAP input, absolute UTC
timestamps, named fields in engineering units, DataFrame/Parquet/GeoJSON export,
and first-class CAT062 system-track support — in a 70 KB wheel with zero runtime
dependencies.

```python
from pyasteryx import Decoder, tracks

for track in tracks(Decoder().iter_multicast("239.1.1.1", 8600)):
    print(track.callsign, track.flight_level, track.ground_speed_kt)
```

**[Field Measurement of Age of Information](https://github.com/franmenjivar/Field_Measurement_of_Age_of_Information-)** &nbsp;
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://github.com/franmenjivar/Field_Measurement_of_Age_of_Information-/blob/main/LICENSE)

Full replication package for an experiment platform measuring how stale
surveillance information degrades tactical UAS conflict detection. Real measured
Age of Information from an operational U-space campaign, a seeded and
reproducible telemetry/network/detection pipeline, thirteen analysis notebooks,
and every figure regenerable from committed results.

---

### 🔧 Stack

| | |
|---|---|
| **Languages** | Python · Scala · SQL |
| **Processing** | Spark · Databricks · Pandas · PyArrow · NumPy |
| **Orchestration** | Airflow · Prefect · Azure Data Factory |
| **Services** | FastAPI · Django · Starlette |
| **Cloud** | GCP · Azure |
| **Platform** | Kubernetes · Docker · Podman · Git · Azure DevOps |
| **ML / Analytics** | scikit-learn · TensorFlow · MLflow · statsmodels |
| **Visualization** | Power BI · Grafana · Looker · Tableau |

---

### 🎓 Background

- **M.Sc. Cyber Security** — Universidad Francisco Gavidia *(in progress)*
- **Diploma, Computer Science** — Algonquin College of Applied Arts and Technology
- **B.Sc. Electrical Engineering** — Universidad Centroamericana José Simeón Cañas

Before airspace data: energy forecasting for solar plants, credit-risk models,
and telecom data platforms. The common thread has always been time series that
somebody has to act on quickly.

---

### 📫 Elsewhere

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/efmenjivar/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0008--9056--0701-A6CE39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0009-0008-9056-0701)
[![Zenodo](https://img.shields.io/badge/Zenodo-1682D4?style=flat-square&logo=zenodo&logoColor=white)](https://doi.org/10.5281/zenodo.22382473)
