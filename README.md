# 🏥 Hospital Management Dashboard — Power BI

A multi-page, interactive Power BI dashboard that consolidates hospital operations — patients, doctors, billing, pharmacy, and ward management — into a single self-service analytics solution.

---

## 📋 Overview

Hospital administrators deal with data scattered across multiple systems. This dashboard unifies all of it into five focused report pages, enabling ward staff, HR, finance, and executives to answer critical operational questions instantly — without waiting for the data team.

---

## 📊 Dashboard Pages

| Page | Audience | Purpose |
|------|----------|---------|
| **Patient** | Ward Staff | 360° patient profile — clinical history, surgery status, medicine consumption, satisfaction score |
| **Doctor** | HR & Finance | Doctor performance — commission, examination fees, billing contribution, assigned patients |
| **Hospital** | Admissions | Bed availability by ward type, patient demographics by age category, surgery overview |
| **Finance** | CFO & Finance Team | Billing breakdown by charge type, monthly medicine sales trends, stock vs. sales analysis |
| **Medicines** | Pharmacy Manager | Inventory view — stock levels, cost prices, sales ranking, supplier breakdown |

---

## ✨ Key Features

- **5 Report Pages** — each tailored to a distinct hospital stakeholder
- **7 Custom DAX Measures** — `total_bill_amount`, `patient_count`, `commision_earn`, `de_fees`, `dr_commision_rate`, `total_med_sale_qty`, `TOTAL_STOCK`
- **Dynamic Slicers** — filter by doctor name, patient age category, and appointment date range
- **4 Bookmarks** — toggle slicer panels open/closed for a cleaner viewing experience (`patient_slicer_off`, `slicer_on`, `dr_off`, `4dr_on`)
- **Cross-Page Navigation** — action buttons for seamless movement between dashboard sections
- **Calendar Table** — enables time-intelligence functions for monthly trend analysis
- **Tooltip Page** — rich hover-over detail on key visuals
- **Cross-Filtering** — visuals on Doctor and Hospital pages respond to each other interactively

---

## 📐 Data Model

Data is sourced from a simulated hospital relational dataset (Kaggle) and structured using a **star-schema** approach in Power BI.

```
patient_detailss  ──►  appointment
      │                    │
      ▼                    ▼
    bill              medicine-patient
                           │
                           ▼
                   medical_stock_infoo

Calendar  ──────────────────────────►  (time intelligence across all pages)
```

**Tables Used:** `patient_detailss`, `bill`, `appointment`, `medicine-patient`, `medical_stock_infoo`, `Calendar`

---

## 💡 Key Insights

**Patient Satisfaction at Individual Level**
Satisfaction scores are tracked per booking, enabling department heads to identify and investigate negative patient experiences directly.

**Transparent Doctor Commission Structure**
All doctor earnings — commission, exam fees, and billing contribution — are visible on a single filterable page, replacing disconnected spreadsheets.

**Age Demographics for Resource Planning**
Patient count by age category reveals which groups dominate the hospital population, informing staffing and specialty deployment decisions.

**Billing Revenue Composition**
The charge-type breakdown (consultation, surgery, room, pharmacy) helps the CFO identify where to invest in capacity and where to adjust pricing.

**Medicine Stock vs. Sales Gap Detection**
Two 100% stacked bar charts instantly surface overstock (dead inventory cost) and stockout risk (patient care disruption) — by medicine and by supplier.

---

## 🗂️ Project Files

```
├── HospitalManagementDashboard.pbix   # Main Power BI report file
└── README.md
```

---

## 🚀 Getting Started

1. **Clone or download** this repository
2. Open `HospitalManagementDashboard.pbix` in **Power BI Desktop**
3. Use the slicers (doctor name, age category, date range) to filter any page
4. Navigate between pages using the action buttons or the Pages panel
5. Click the bookmark toggle buttons to show/hide slicer panels

> **Requirements:** Power BI Desktop (latest version recommended)

---

## 📦 Data Source

| Attribute | Detail |
|-----------|--------|
| Source | [Kaggle — Hospital Management Dataset](https://www.kaggle.com/) |
| Format | Simulated relational hospital database |
| Tables | 5 core tables + Calendar dimension |
| Preparation | Power Query (type corrections, null handling, column renaming) |

---

## 🏗️ Technical Details

- **Data Modelling** — Star-schema with patient table as the central fact/dimension hub
- **DAX** — Custom measures for all KPI cards; no implicit measures used
- **Power Query** — All transformations applied before model load
- **Calendar Table** — Created manually to support `TOTALYTD`, date slicers, and monthly trend charts
- **Visual Types** — Clustered bar, clustered column, line chart, 100% stacked bar, pivot table, card, table

---

## 📈 Business Impact

- **Reduced admin time** — ward staff access full patient profiles in seconds instead of navigating multiple systems
- **Evidence-based HR** — doctor performance reviews backed by filterable billing and commission data
- **Real-time capacity management** — admissions team sees live bed availability by ward type
- **Self-service financial reporting** — CFO filters by date, department, and charge type without analyst support
- **Supply chain efficiency** — pharmacy identifies stockout risk and dead inventory at a glance

---

## 🙋 About

Built as a demonstration of Power BI capabilities applied to the healthcare domain — showcasing data modelling, DAX, Power Query, bookmark navigation, and multi-stakeholder dashboard design.

---

### Dashboard Preview
<img width="1769" height="915" alt="Screenshot 2026-05-02 185432" src="https://github.com/user-attachments/assets/08951fea-4f12-4943-92c7-62637252de2a" />
<img width="1774" height="908" alt="Screenshot 2026-05-02 172511" src="https://github.com/user-attachments/assets/0a246eb3-e596-47bf-95f0-00860cf0b0ed" />
<img width="1779" height="906" alt="Screenshot 2026-05-02 172453" src="https://github.com/user-attachments/assets/d50729bc-3b47-4145-897a-5d3904264c8f" />
<img width="1775" height="907" alt="Screenshot 2026-05-02 172438" src="https://github.com/user-attachments/assets/993a5eb7-645b-4d50-9892-d56592c33550" />
<img width="1748" height="927" alt="Screenshot 2026-05-02 172423" src="https://github.com/user-attachments/assets/1874327c-351d-417f-8ff3-a445c0022388" />


---
