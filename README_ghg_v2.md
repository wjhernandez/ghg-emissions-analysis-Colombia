# Análisis de Emisiones GHG y Huella de Carbono
### Colombia en el Contexto Latinoamericano. Metodología GHG Protocol (Greenhouse Gas Protocol)

**Autora:** Wendy J. Hernández  
**Perfil:** Ingeniería Química · Especialización Ambiental · Data Analytics  
**Stack:** Python · Power BI · Excel  
**Dataset:** [Our World in Data — CO2 and Greenhouse Gas Emissions](https://ourworldindata.org/co2-and-greenhouse-gas-emissions)

---

## Contexto

El seguimiento y reporte de emisiones de GHG (Greenhouse Gas — Gases de Efecto Invernadero) es el primer paso de cualquier estrategia de descarbonización. El estándar internacional de referencia es el **GHG Protocol (Greenhouse Gas Protocol. Protocolo de Gases de Efecto Invernadero)**, desarrollado por el WRI (World Resources Institute) y el WBCSD (World Business Council for Sustainable Development).

Colombia se comprometió bajo el Acuerdo de París a reducir sus emisiones GHG en un **51% para 2030** respecto al escenario BAU (Business As Usual / Tendencia sin acción climática), uno de los compromisos NDC (Nationally Determined Contributions — Contribuciones Determinadas a Nivel Nacional) más ambiciosos de América Latina.

### Preguntas de análisis

> 1. ¿Cuál es la tendencia histórica de emisiones de CO2 en Colombia y cómo se compara con la región latinoamericana?
> 2. ¿Qué factores explican la intensidad de carbono de Colombia (kgCO2 por USD de PIB)?
> 3. ¿Está Colombia en trayectoria para cumplir su NDC al 2030?
> 4. ¿Cómo se distribuyen las emisiones per cápita entre los países de la región?

---

## Dataset

**Fuente:** Our World in Data (OWID), CO2 and Greenhouse Gas Emissions  
**Referencia:** Ritchie, H., Rosado, P. & Roser, M. (2023). Our World in Data. https://ourworldindata.org/co2-and-greenhouse-gas-emissions  
**Período:** 1990 — 2022  
**Cobertura:** 15 países de América Latina + referencia global

| Variable | Descripción | Unidad |
|---|---|---|
| co2 | Emisiones CO2 totales | MtCO2 |
| co2_per_capita | Emisiones CO2 per cápita | tCO2/habitante |
| co2_per_gdp | Intensidad de carbono | kgCO2/USD PIB |
| coal_co2 / oil_co2 / gas_co2 | Emisiones por combustible | MtCO2 |
| methane | Emisiones CH4 (metano) | MtCO2eq |
| nitrous_oxide | Emisiones N2O (óxido nitroso) | MtCO2eq |
| total_ghg | Emisiones GHG totales | MtCO2eq |
| share_global_co2 | Participación en emisiones globales | % |

---


### Clasificación GHG Protocol

| Scope | Descripción | Aplicación en este análisis |
|---|---|---|
| Scope 1 | Emisiones directas por combustión | coal_co2 + oil_co2 + gas_co2 + cement_co2 |
| Scope 2 | Energía eléctrica indirecta | Consumo eléctrico × Factor emisión red (varía anualmente, UPME) |
| Scope 3 | Otras emisiones indirectas | No incluido en este análisis |

---

## Cómo Ejecutar

**1. Clonar el repositorio**
```bash
git clone https://github.com/wjhernandez/ghg-emissions-colombia.git
cd ghg-emissions-colombia
```

**2. Instalar dependencias**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

**3. Descargar el dataset manualmente**

El dataset de OWID (Our World in Data) requiere descarga manual:

- Ve a este link en el navegador:
  https://github.com/owid/co2-data/blob/master/owid-co2-data.csv
- Haz clic en el botón **"Download raw file"** (ícono de descarga en la esquina superior derecha)
- Guarda el archivo como `owid-co2-data.csv` en la carpeta `notebook/` del repositorio

El dataset incluye datos actualizados con el Global Carbon Budget 2024 (datos hasta 2023).


## 5. Conclusiones
Conclusiones

Colombia muestra una tendencia creciente en emisiones de CO2 desde 1990, aunque con una desaceleración en los últimos años. En comparación con otros países de América Latina, su nivel absoluto de emisiones es moderado, pero mantiene una participación relevante en la región.

La intensidad de carbono de Colombia es relativamente baja frente a economías más industrializadas de la región, lo que indica una matriz energética menos intensiva en carbono. Sin embargo, esta ventaja estructural no es suficiente por sí sola para garantizar el cumplimiento de los compromisos climáticos.

Las emisiones per cápita en Colombia se mantienen por debajo de países como México, Chile o Argentina, lo que refleja tanto el nivel de desarrollo industrial como patrones de consumo energético. Aun así, existe una tendencia al alza que debe ser monitoreada.

El análisis de fuentes de emisión evidencia una alta dependencia de combustibles fósiles, particularmente petróleo y gas, lo que representa un desafío clave para la transición energética.

En el escenario proyectado, Colombia enfrenta un riesgo de no cumplir completamente su meta NDC al 2030 bajo una trayectoria Business As Usual. Esto sugiere la necesidad de acelerar medidas de mitigación, especialmente en sectores energéticos y productivos.

En términos estratégicos, el país tiene una oportunidad clara de avanzar en descarbonización aprovechando su potencial en energías renovables, eficiencia energética y políticas públicas orientadas a reducción de emisiones.

## Relevancia para Estrategia ESG Empresarial

Este análisis aplica directamente a:

- **Reporte de sostenibilidad GRI (Global Reporting Initiative):** indicadores GRI 305 (Emisiones)
- **Inventarios corporativos GHG Protocol:** metodología Scope 1/2/3
- **Due diligence climático:** evaluación de riesgo de transición para inversionistas
- **Estrategia Net Zero:** definición de líneas base y metas de reducción
- **Consultoría ESG:** benchmark sectorial y nacional para clientes corporativos

---

## Referencias

- Ritchie, H., Rosado, P. & Roser, M. (2023). *CO₂ and Greenhouse Gas Emissions*. Our World in Data.
- WRI & WBCSD (2015). *The Greenhouse Gas Protocol: A Corporate Accounting and Reporting Standard*.
- UPME (2022). *Factor de Emisión de CO2 de la Red Eléctrica Colombiana*. Unidad de Planeación Minero-Energética.
- DNP (2021). *Contribución Determinada a Nivel Nacional (NDC) de Colombia. Actualización 2020*.
- IPCC (2022). *Sixth Assessment Report — Working Group III: Mitigation of Climate Change*.

---

*Proyecto desarrollado como parte del portafolio de Data Analytics con enfoque en sostenibilidad, ESG y cambio climático.*
