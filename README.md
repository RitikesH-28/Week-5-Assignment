# Week-5-Assignment# 📊 Real-Time Parking Price Simulation System

## 📝 Overview

This project simulates a **real-time dynamic pricing system** for parking lots. It models how parking prices can adjust dynamically based on **traffic conditions**, **lot occupancy**, and **time of day**, aiming to optimize utilization and maximize revenue.

It uses streaming architecture principles with **Pathway**, and offers **interactive data visualization** via **Bokeh** and **Panel** in a live dashboard environment (e.g., Google Colab).

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
