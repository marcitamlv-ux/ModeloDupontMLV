# 📊 Modelo Dupont en Streamlit

Este proyecto permite cargar datos financieros desde un archivo Excel y calcular automáticamente los indicadores clave del modelo Dupont para evaluar la rentabilidad de un negocio. Está desarrollado en Python y desplegable en Streamlit.

## 🚀 Funcionalidades

- 📂 Carga de archivos Excel con los datos financieros
- 📈 Cálculo automático de:
  - Margen Neto (%)
  - Rotación (veces)
  - Apalancamiento (veces)
  - ROE (%)
  - ROA (%)
  - Pay Back Capital (veces)
  - Pay Back Activos (veces)
- 📤 Exportación del reporte en Excel
- 🔁 Adaptable a cualquier número de períodos (columnas)
- 🧮 Fórmulas dinámicas y visualización en tabla transpuesta

## 🗂 Estructura esperada del Excel

El archivo Excel debe contener los siguientes renglones (en la primera columna) con los valores por período en las columnas:

| Indicador           | 1992 | 1993 | 1994 | ... |
|---------------------|------|------|------|-----|
| Ventas Netas        | ...  | ...  | ...  |     |
| Utilidad Neta       | ...  | ...  | ...  |     |
| Activos Totales     | ...  | ...  | ...  |     |
| Capital Contable    | ...  | ...  | ...  |     |

## 🧠 Fórmulas utilizadas

- **Margen Neto (%)** = Utilidad Neta / Ventas Netas
- **Rotación (veces)** = Ventas Netas / Activos Totales
- **Apalancamiento (veces)** = Activos Totales / Capital Contable
- **ROE (%)** = Margen Neto × Rotación
- **ROA (%)** = Rotación × Apalancamiento
- **Pay Back Capital (veces)** = 1 / ROE
- **Pay Back Activos (veces)** = 1 / ROA

## ▶️ Cómo correr localmente

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu_usuario/tu_repo.git
   cd tu_repo
   ```

2. Instala las dependencias:
   ```bash
   pip install -r requirements.txt
   ```

3. Ejecuta la aplicación:
   ```bash
   streamlit run app.py
   ```

## ☁️ Cómo desplegar en Streamlit Cloud

1. Crea un repositorio en GitHub y sube:
   - `app.py` (con el código)
   - `requirements.txt`
   - `README.md`

2. Ve a [streamlit.io/cloud](https://streamlit.io/cloud) y conecta tu repositorio.