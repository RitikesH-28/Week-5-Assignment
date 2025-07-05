# Week-5-Assignment# 📊 Real-Time Parking Price Simulation System

## 📝 Overview

This project demonstrates a real-time, dynamic pricing system for urban parking lots using streaming data
processing techniques.
 It adjusts prices based on live parameters like occupancy, traffic, and time, simulating a smart pricing
model.

---

## 🧰 Tech Stack

| Technology      | Purpose                                           |
|------------------|---------------------------------------------------|
| **Python**        | Core development language                        |
| **Pandas**        | Data manipulation and preprocessing              |
| **Pathway**       | Real-time stream processing and reactive pipeline|
| **Bokeh**         | Interactive data visualization                   |
| **Panel**         | Dashboard layout and control interface           |
| **Google Colab**  | Cloud-based development and visualization        |

---

## 🏗️ Architecture Diagram

```mermaid
graph TD
    A[Simulated CSV Data / Streaming Source] --> B[Pathway Input Connector]
    B --> C[Dynamic Pricing Engine]
    C --> D[Price & Occupancy Computation]
    D --> E[Transformed DataFrame]
    E --> F[Bokeh Charts]
    F --> G[Panel Dashboard]


## Repository Structure
 - dataset.csv: Input data
 - main.ipynb: Notebook with logic and visuals
 - requirements.txt: Dependencies
 - README.md: Documentation
 - report.pdf: This file (optional)
 - screenshots/: Dashboard images (optional)


Use Cases
 - Smart city parking optimization
 - Dynamic revenue management
 - Simulation before production deployment
 - Extendable to real-time sensor inputs

Future Enhancements
 - Integration with real-time APIs (Google Maps, etc.)
 - Predictive ML models
 - Availability notifications
- User feedback collection and price perception analytics

Author & References
 Author: RitikesH Bhardwaj
 GitHub: https://github.com/RitikesH-28
 References:
 - Pathway Docs: https://pathway.com/docs/
 - Bokeh: https://docs.bokeh.org/
 - Panel: https://panel.holoviz.org/
 - Mermaid Live Editor: https://mermaid.live/
