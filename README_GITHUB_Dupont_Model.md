# 📊 Streamlit Dupont Model

This is a Python + Streamlit application to calculate and visualize the **Dupont Profitability Model** using data uploaded via Excel. It is designed for business finance users who want to analyze ROE, ROA, and efficiency indicators in a user-friendly web interface.

---

## 🚀 Features

- Upload Excel file with financial data
- Automatically calculate:
  - Net Margin (%)
  - Asset Turnover (x)
  - Leverage (x)
  - ROE (%)
  - ROA (%)
  - Payback on Equity (x)
  - Payback on Assets (x)
- Dynamic multi-period support
- Downloadable Excel report
- Ready to deploy to [Streamlit Cloud](https://streamlit.io/cloud)

---

## 📁 Project Structure

```
📦 dupont-streamlit-app
├── app.py                 # Streamlit application
├── README.md              # This file
├── requirements.txt       # Python dependencies
└── sample_data.xlsx       # Example input (optional)
```

---

## 📊 Expected Input Format

The Excel file must have **indicators as rows** and **periods as columns**. Required rows:

| Indicator          | 2022 | 2023 | ... |
|--------------------|------|------|-----|
| Ventas Netas       | 1000 | 1100 |     |
| Utilidad Neta      | 150  | 160  |     |
| Activos Totales    | 500  | 550  |     |
| Capital Contable   | 300  | 320  |     |

---

## 🧠 Dupont Formulas Used

- `Margen Neto (%) = Utilidad Neta / Ventas Netas`
- `Rotación (veces) = Ventas Netas / Activos Totales`
- `Apalancamiento (veces) = Activos Totales / Capital Contable`
- `ROE (%) = Margen Neto × Rotación`
- `ROA (%) = Rotación × Apalancamiento`
- `Pay Back Capital = 1 / ROE`
- `Pay Back Activos = 1 / ROA`

---

## ▶️ Running Locally

```bash
git clone https://github.com/yourusername/dupont-streamlit-app.git
cd dupont-streamlit-app
pip install -r requirements.txt
streamlit run app.py
```

---

## ☁️ Deploy to Streamlit Cloud

1. Push this repo to GitHub
2. Go to [streamlit.io/cloud](https://streamlit.io/cloud)
3. Click **“New app”** and connect your repo
4. Set the main file as `app.py`
5. Done ✅

---

## 📄 License

MIT License.