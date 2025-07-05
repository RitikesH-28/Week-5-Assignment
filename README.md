# 🚗 Real-Time Parking Price Simulation Engine  
> A real-time data pipeline using Pathway for dynamic, competitive parking pricing with live analytics and dashboard.

---

## 📌 Overview

This project showcases a real-time pricing simulation system for smart parking management using **Pathway**, a modern data framework for stream processing and analytics. By ingesting and transforming live or simulated parking data (traffic, demand, timestamps), it dynamically adjusts parking prices per area to ensure competitive rates based on actual conditions.

This project combines **Python**, **Pathway**, **Panel**, and **Bokeh** to create a reactive and interactive dashboard, perfect for applications in **smart city infrastructure**, **transport optimization**, or **IoT-driven urban planning**.

---

## 🚀 Key Features

- 🔁 Real-time ETL pipeline using Pathway
- 💡 Dynamic pricing based on traffic & demand
- 📈 Interactive Bokeh/Panel dashboard
- ⚡ Fast updates & live visualization
- 🧠 Scalable and memory-efficient
- 📦 Easily deployable with Docker or Colab

---

## 🧰 Tech Stack

| Layer        | Tools & Libraries        | Role                          |
|--------------|--------------------------|-------------------------------|
| Data Input   | `CSV` / Live Streaming   | Simulated parking traffic     |
| Engine       | `Pathway`                | Real-time processing          |
| Processing   | `Pandas`, `NumPy`        | Data transformation           |
| Visualization| `Bokeh`, `Matplotlib`    | Interactive plots             |
| Dashboard    | `Panel`                  | GUI/UX interactivity          |
| Environment  | `Google Colab`, `Docker` | Dev & deployment              |

---

## 📐 Architecture Diagram

mermaid
graph TD
    A[📂 dataset.csv or Live Stream] --> B[🧠 Pathway Processing Engine]
    B --> C[💸 Dynamic Pricing Logic]
    C --> D[📈 Bokeh + Panel Visualization]
    D --> E[🖼️ Interactive Dashboard (Colab / Web)]
⚙️ How It Works
Data Ingestion:
The system reads from a simulated CSV or live data stream, containing fields like Area, Traffic, Demand, LastUpdatedTime, etc.

Preprocessing:
Columns are merged into timestamps, cleaned, and passed into Pathway’s stream abstraction using PythonReader.

Dynamic Pricing Logic:
Based on input conditions, pricing is adjusted:

High Traffic → +30% increase

High Demand → +40% increase

Combined surge effects apply

Streaming & Updates:
Pathway manages state, consistency, and late updates using in-memory streaming.

Visualization:
Bokeh & Panel render charts showing:

Price over time

Area-wise comparisons

Demand/Traffic overlays

📦 Installation
🔧 Local Setup
bash
Copy
Edit
# Clone the repository
git clone https://github.com/RitikesH-28/Week-5-Assignment.git
cd Week-5-Assignment

# Install dependencies
pip install pandas numpy pathway panel bokeh matplotlib
▶️ Run Locally
Load dataset.csv

Open main_notebook.ipynb in Jupyter or Colab

Run cells in order

Dashboard launches via pn.serve(...) or inline for notebooks

🐳 Docker Deployment
Dockerfile (example):

dockerfile
Copy
Edit
FROM python:3.10-slim

RUN pip install -U pathway pandas numpy bokeh panel matplotlib

WORKDIR /app
COPY . /app

CMD ["python", "main_script.py"]
Build & Run:

bash
Copy
Edit
docker build -t parking-simulator .
docker run -it --rm -p 5006:5006 parking-simulator
☁️ Cloud & Colab Support
You can also run this project in Google Colab with just one click:

Open main_notebook.ipynb in Google Colab

Upload dataset.csv

Run all cells

Launch interactive output inside notebook using Panel

🧪 Example Output
📉 Time series of parking prices

📍 Pricing comparison by area

⚠️ Visual alerts for high congestion zones

📊 Combined heatmap for traffic and demand

📁 Repository Structure
bash
Copy
Edit
Week-5-Assignment/
├── dataset.csv                # Simulated parking data
├── main_notebook.ipynb       # Notebook with full simulation
├── main_script.py            # Python version (optional)
├── Dockerfile                # For Docker-based deployment
├── README.md                 # Full project documentation
└── report.pdf (optional)     # Formal project report
📜 Licensing
This project is open-sourced under the MIT License for academic/demo purposes.

If you plan to use this in production, consult the licensing terms of Pathway, which uses BSL 1.1 (free for most uses, transitions to Apache-2.0 in 4 years).

📚 References
🔗 Pathway Docs

📘 Bokeh Documentation

🖼️ Panel Library

☁️ Google Colab

💬 Support & Community
Need help?

🧑‍💻 Raise an issue in this repository

💬 Join the Pathway Discord: community link

📧 Contact: ritikeshbhardwaj.dev@gmail.com

👏 Acknowledgments
Huge thanks to:

The Pathway Team for their incredible real-time framework

The developers behind Bokeh and Panel for great open-source visualization tools

Open-source contributors everywhere ❤️
