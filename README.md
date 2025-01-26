# Data Insights on Chicago Crimes

## Dataset
The dataset contains reported crime incidents (excluding murders) in Chicago from 2001 to the present, sourced from the Chicago Police Department's CLEAR system. The addresses are anonymized at the block level, and the data is updated daily, with the exception of the most recent seven days. Please note that crime classifications are preliminary and may be revised following further investigation.
---

## Webpage
Interactive visualizations for Projects 2 and 3 are hosted [here](https://smysar2.github.io/). On the left are visualizations from Project 2, while spatial multi-linked visualizations from Project 3 are on the right. 

![Webpage Screenshot](https://github.com/uic-cs424/assignment-4-black-hawks/assets/144352425/b6513cc5-0fcc-4479-9ed9-a5b551d6dac0)

---

## Visualizations

### **Top Left Visualization**
Utilizing D3, this visualization allows users to explore crime trends and arrest rates over years or districts. Dropdown menus offer filters by year, district, and crime attributes (e.g., arrests, non-arrests).  
Key Features:
- Combined **bar and line charts** for crime counts and arrest rates.
- Tooltip-enabled **dotted chart** compares pre- and post-COVID-19 crime counts.  

**Insights:**
- Crime counts have decreased over time, with arrests showing a steeper decline than non-arrests.
- District 8 has the highest crime counts, while District 11 leads in arrests.

![Chart Screenshot](https://github.com/uic-cs424/assignment-4-black-hawks/assets/144352425/acd067dc-5694-47f2-9ded-3be277841e18)

---

### **Bottom Left Linked Visualization**
A two-part interactive graph analyzes crime trends by either **crime type/district** or **year/crime type**:
1. **Crime Type/District**:
   - A bar chart shows counts for top crime types or districts.
   - Selecting a bar updates a dotted chart for community-specific counts.  
   - Bar intensity reflects count magnitude.  
2. **Year/Crime Type**:
   - A line chart visualizes crime trends over years.
   - Brushing an area updates a stacked bar chart for arrest vs. non-arrest counts across crime types.

**Insights:**
- Theft and battery are the most common crimes. 
- Narcotics crimes show high arrest efficiency, indicating effective enforcement.

![Bar Chart](https://github.com/uic-cs424/assignment-4-black-hawks/assets/144352425/32b5eb93-9ec4-4d2a-b2a0-6679190fb0fa)
![Dotted Chart](https://github.com/uic-cs424/assignment-4-black-hawks/assets/144352425/945f3876-769c-48be-b094-84f5e8081513)

---

### **Right-Side Spatial Multi-Linked Visualization**
A spatial map shows the top 10 crime types for a selected year. Users can:
- Hover or click on crime types to reveal a **line chart** showing district-wise trends.  
- Select a district on the line chart to display a **donut chart** comparing arrested vs. non-arrested incidents.

**Insights:**
- Spatial patterns highlight crime distribution hotspots.
- Comparative district-level analysis enables law enforcement optimization.

![Spatial Visualization](https://github.com/uic-cs424/assignment-4-black-hawks/assets/144352425/fd946a1a-4f7b-452b-bee2-caeb9d39dbb0)

---

## Urban Toolkit (UTK) Integration

### Initial Setup:
We attempted to use UTK for data processing and visualization:
1. Installed UTK via `requirements.txt` and followed examples from [Urban Toolkit Docs](http://urbantk.org/getting-started/).  
2. Tried loading OpenStreetMap (OSM) data using:
   ```python
   import utk
   uc = utk.OSM.load('ChicagoUSA', layers=['buildings'])
