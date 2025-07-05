# 🚗 Real-Time Competitive Pricing Simulation for Parking

This project demonstrates a real-time dynamic pricing simulation system for a smart parking solution. It uses real-time streaming data and adjusts parking prices dynamically based on **traffic intensity**, **demand**, and **timestamp**. The goal is to make pricing **adaptive and competitive**, while ensuring fairness and maximizing utility for both service providers and consumers.

This project was developed as part of a Week 5 assignment exploring **real-time data pipelines**, **event-driven pricing**, and **interactive visualization dashboards** using modern Python tools.

---

## 🔧 Tech Stack Used

| Layer              | Technology                           | Purpose                                                   |
|-------------------|---------------------------------------|-----------------------------------------------------------|
| 📊 Data Handling   | `pandas`, `numpy`                     | Reading and preprocessing time-series CSV data            |
| 🔄 Stream Engine   | `Pathway`                             | Real-time data ingestion, transformation, and pipeline    |
| 📈 Visualization   | `Bokeh`, `Matplotlib`                 | Interactive plotting and graphs                           |
| 🖥️ Dashboard       | `Panel`                               | Displaying real-time visual output                        |
| 🧪 Environment     | Google Colab / Jupyter Notebook       | Cloud-based execution or local analysis                   |
| 📁 Input Data      | CSV File (`dataset.csv`)              | Simulated or real parking data                            |

---

## 📐 System Architecture

```mermaid
graph TD
    A[📂 CSV Input Data] --> B[🧠 Preprocessing]
    B --> C[🔁 Pathway Streaming Pipeline]
    C --> D[💰 Dynamic Pricing Algorithm]
    D --> E[📈 Bokeh Visualization]
    E --> F[🖼️ Panel Dashboard]
    C --> G[📤 Real-time Pricing Output]
📚 Project Structure and Workflow
1. Dataset
The data comes from a CSV file named dataset.csv, containing the following columns:

Area – Parking zone

LastUpdatedDate and LastUpdatedTime – Time of last data point

BasePrice – Initial parking fee

Traffic – Real-time traffic rating (e.g., Low, Medium, High)

Demand – Customer demand rating (e.g., Low, Medium, High)

All timestamps are merged to create a continuous Timestamp column.

2. Real-Time Data Processing with Pathway
The system uses Pathway to simulate a streaming input, monitoring changes in data.

A custom logic table updates prices dynamically using real-time values.

The algorithm scales prices based on:

High traffic → Higher prices

High demand → Surge pricing

Low activity → Discounts to attract drivers

3. Dynamic Pricing Logic
Pricing logic applies weights to the traffic and demand signals. Example logic:

python
Copy
Edit
def compute_dynamic_price(base, traffic, demand):
    factor = 1.0
    if traffic == 'High':
        factor += 0.3
    elif traffic == 'Medium':
        factor += 0.15

    if demand == 'High':
        factor += 0.4
    elif demand == 'Medium':
        factor += 0.2

    return round(base * factor, 2)
4. Visualization
Bokeh creates interactive plots for:

Price vs Time

Traffic vs Demand overlays

Area-wise price differences

Panel hosts a real-time dashboard with:

Drop-down filters for Area or Time

Tooltips and dynamic charts

Real-time refresh capability (if run in Colab)

5. Execution Instructions
🖥️ Setup Instructions
bash
Copy
Edit
# Clone the repo
git clone https://github.com/RitikesH-28/Week-5-Assignment.git
cd Week-5-Assignment

# Install dependencies
pip install pandas numpy bokeh panel matplotlib pathway
▶️ Run the Notebook
Open main_notebook.ipynb in Jupyter or Google Colab

Upload or load dataset.csv

Run cells step-by-step to:

Load and preprocess data

Stream data via Pathway

Compute real-time prices

Launch interactive dashboard

📁 Folder Structure
bash
Copy
Edit
Week-5-Assignment/
│
├── dataset.csv                # Sample data with pricing fields
├── main_notebook.ipynb       # Main simulation code
├── README.md                 # Full documentation
├── report.pdf (optional)     # Additional project write-up (if available)
📑 Sample Output Features
🚦 Real-time charts for traffic and pricing impact

🏷️ Annotated graphs with tooltips

📉 Live adjustment of pricing over a stream

📍 Area filter and custom selection

📄 Optional Documentation
If you want to add a formal project report:

Prepare a report.pdf including:

Introduction

Objective

System Design

Code Overview

Output Screenshots

Conclusion

Upload the PDF in the repository root (/report.pdf)

🙏 Acknowledgments
Pathway for real-time processing framework

Bokeh and Panel for powerful Python-based visualization

Google Colab for seamless cloud execution

📬 Contact
Developed by: RitikesH-28
GitHub: https://github.com/RitikesH-28
For questions, open an issue or message directly.
