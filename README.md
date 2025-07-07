# Dynamic Pricing Dashboard for Urban Parking Lots

A real-time dynamic pricing dashboard that adjusts parking lot prices using occupancy, traffic, queue length, vehicle type, and other factors. Built with **Pathway**, **Panel**, and **Bokeh**.

---

## Tech Stack

- **Python 3**
- **Pandas** – data manipulation
- **NumPy** – numerical operations
- **Pathway** – streaming data engine
- **Panel** – dashboard UI
- **Bokeh** – interactive visualizations
- **Google Colab** – for notebook development

---

##  Architecture Diagram

![Architecture Diagram](assets/architecture_diagram.png)

---

##  Folder Structure

```
📁 dynamic-pricing-dashboard/
├── 📁 code/
│   ├── dynamic_pricing_dashboard.py
│   └── dynamic_pricing_dashboard.ipynb
├── 📁 data/
│   └── dataset.csv
├── 📁 outputs/
│   └── pricing_output_all_systems_all_models.json
├── 📁 assets/
│   └── architecture_diagram.png
├── README.md
└── requirements.txt
```

---

##  Features

- Select parking **System Code** and **Pricing Model**
- View interactive **time-series pricing chart**
- Supports 3 pricing models:
  - Linear
  - Demand-Based
  - Competitive
- Automatically generates a combined JSON file with **all model outputs for all parking lots**

---

## How to Run the Dashboard

###  Option 1: Run on Google Colab (Recommended)

This project was developed and tested in **Google Colab** and works fully there, including Panel and Bokeh dashboard rendering.

1. Open the `code/dynamic_pricing_dashboard.ipynb` file in Colab.
2. Run all the cells step by step.
3. Make sure to call:
```python
pn.extension()
pn.serve(dashboard, show=True)
```
to see the interactive dashboard.

>  Colab may give you a public link (`Running on public URL`) — use that to view the dashboard.

---

###  Option 2: Run Locally (Optional)

1. Install dependencies:
```bash
pip install pathway panel bokeh pandas numpy
```

2. Serve the dashboard:
```bash
panel serve code/dynamic_pricing_dashboard.py --autoreload
```

Then open [http://localhost:5006](http://localhost:5006) in your browser.

---

## Output File

Once the dashboard starts, a combined pricing JSON is generated:

```
outputs/pricing_output_all_systems_all_models.json
```

It contains price records for **every parking lot (SystemCodeNumber)** under all three pricing models.

---



## 👤 Submitted By

**Name**: *Your Name*  
**GitHub**: [https://github.com/your-username](https://github.com/your-username)  
**Program**: Summer Analytics 2025 – Final Submission





