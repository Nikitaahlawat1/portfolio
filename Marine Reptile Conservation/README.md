# Blue Visionary

<img width="1920" height="600" alt="image" src="https://github.com/user-attachments/assets/f8bcae96-eccd-4302-90c8-83611422a0b6" />

## 1. Project Overview

The project aims to create an interactive and educational website focused on marine conservation in Australia. The platform will provide users with vital resources and tools which include marine plastic pollution, information about endangered marine reptiles like sea turtles, tools for testing marine knowledge, a role play game about sea turtles, a system that can identify and track users’ contribution about marine conservation and information about the plastic process facilities. This website aims to empower marine conscious individuals to put more effort into marine conservation  and raise the public awareness of protecting the ocean.

## 2. Skills & Tools

### 2.1 Tools
- Python, SQL, Pandas, NumPy, GIT, Machine Learning, D3.js, Leaflet, RestAPI, Azure, Excel, CSV, APIs

### 2.2 Soft Skills
- Leadership, Team Collaboration, Communicating insights to non-technical audiences, Structured problem-solving, Cross-functional collaboration

## 3. Data Usage
The datasets below are collectively used to analyze marine biodiversity threats and plastic pollution across Australia by integrating endangered marine species data, plastic debris observations, waste management and population statistics, environmental policies, and computer vision models to support mapping, analysis, and decision-making at national and state levels.

1.	Species of National Environmental Significance and selected marine and cetacean species  - https://fed.dcceew.gov.au/datasets/erin::species-of-national-environmental-significance-and-selected-marine-and-cetacean-species/explore?location=-19.690183%2C-73.460000%2C2.72&showTable=true
2.	Threatened Species State Lists  - https://data.gov.au/data/dataset/ae652011-f39e-4c6c-91b8-1dc2d2dfee8f/resource/78401dce-1f40-49d3-92c4-3713d6e34974/download/20240716spcs.csv
3.	Species API - https://apiv3.iucnredlist.org/api/v3/docs
4.	States and territories - Australia - https://data.opendatasoft.com/explore/dataset/georef-australia-state%40public/export/?disjunctive.ste_code&disjunctive.ste_name
5.	AODN-IMOS Microdebris Data (ALL) from Jan-2021 to Apr-2024 - https://portal.aodn.org.au/search?uuid=fd3d74b0-0234-4864-bbc6-751c44e41f5e
6.	nettows_info - https://figshare.com/articles/dataset/Data_from_Marine_Plastic_Pollution_in_Waters_around_Australia_Characteristics_Concentrations_and_Pathways/865018?file=3124901
7.	plastics_info - https://figshare.com/articles/dataset/Data_from_Marine_Plastic_Pollution_in_Waters_around_Australia_Characteristics_Concentrations_and_Pathways/865018?file=3124901
8.	List of environmental legislation and policy reviewed - https://www.researchgate.net/figure/List-of-environmental-legislation-and-policy-reviewed_tbl1_331023282
9.	States and territories – Australia - https://data.opendatasoft.com/explore/dataset/georef-australia-state%40public/export/?disjunctive.ste_code&disjunctive.ste_name
10.	Plastic detection Computer Vision Project - https://universe.roboflow.com/asia-pacific-university-msg4d/plastic-detection-o3dr4
11.	Plastic Waste Management Computer Vision Project - https://universe.roboflow.com/yolov5-6agzx/plastic-waste-management-6p8kw
12.	National Waste Report 2022 - https://www.dcceew.gov.au/sites/default/files/documents/national-waste-database-2022.xlsx
13.	Waste Management Facilities Database - https://data.gov.au/dataset/ds-ga-495820b9-4a56-4409-9d1b-950589b50936/details?q=waste-management-facilities
14.	Population Dataset - https://www.abs.gov.au/statistics/people/population/historical-population/2021

## 4. Data Preparation & Wrangling

In the initial exploration phase, the dataset was assessed for common quality issues that could distort results, including missing values, inconsistencies, outliers, and potentially corrupted records. Where issues were detected, decisions were made to either clean the affected fields or remove problematic rows to maintain analytical integrity.

To ensure the dataset was suitable for downstream analysis and modeling, additional preprocessing steps were applied as needed, including normalization (to enforce consistent units of measurement) and transformations to improve interpretability and model compatibility. Data wrangling also included feature creation, variable transformations, and restructuring tables to support more efficient analysis. Standardization was prioritized throughout to reduce the risk of errors during later stages.

After cleaning and standardizing the data, an Entity Relationship Diagram (ERD) was developed to define and document relationships between entities, minimize redundancy, and improve query reliability. Based on the ERD, entity attributes were exported into separate CSV files to create well-structured datasets that can support deeper analysis, machine learning workflows, and advanced statistical methods.

## 5. Data Visualisations and Insights

### 5.1 Endangered marine species insights by state
This visualisation highlights endangered marine species from each state and provides a state by state view of where endangered species are most at risk. By identifying the most endangered species within their state, young marine conservation enthusiasts can focus their efforts on learning about and advocating for these critical species. This helps students prioritise conservation actions through school projects, social media campaigns, or community outreach, supporting the preservation of biodiversity in local marine ecosystems.

<img src="https://github.com/Nikitaahlawat1/portfolio/blob/fe4058a3f38eb84d5f0570b6a52632bccba49cbe/assets/end_sp.png" alt="Alt text" width="1000">

### 5.2 Marine plastic pollution insights by state

Visualisations below presents data insights on pollution, focusing on the distribution of marine plastic pollution by state across Australia’s coastal and marine regions. By visualising pollution data, busy individuals who work or live in urban areas can quickly understand the extent and locations of pollution and focus cleanup efforts on the most affected regions near them. This supports more informed action, highlights the urgency of marine conservation, and makes it easier to engage even with limited time for research or direct involvement.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/Nikitaahlawat1/portfolio/blob/b2bb1640feaeff7dfd2ba490157e0e7be4d0d8bd/assets/plas_dis.png" alt="Image 1" width="500">
    </td>
    <td align="center">
      <img src="https://github.com/Nikitaahlawat1/portfolio/blob/b2bb1640feaeff7dfd2ba490157e0e7be4d0d8bd/assets/plas_trend.png" alt="Image 2" width="500">
    </td>
  </tr>
</table>

### 5.3 Plastic waste reduction tracker insights

This section covers a feature that lets users record and monitor their plastic waste reduction activities. Users can track details such as single use plastics avoided, reusable items adopted, and plastic waste properly recycled. By turning these actions into a clear personal record, the tracker helps users see the impact they are making, understand their contribution to reducing plastic pollution, and stay motivated to keep practicing more sustainable habits.

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/Nikitaahlawat1/portfolio/blob/b2bb1640feaeff7dfd2ba490157e0e7be4d0d8bd/assets/rec_track.png" alt="Image 1" width="500">
    </td>
    <td align="center">
      <img src="https://github.com/Nikitaahlawat1/portfolio/blob/b2bb1640feaeff7dfd2ba490157e0e7be4d0d8bd/assets/plas_con.png" alt="Image 2" width="500">
    </td>
  </tr>
</table>

### 5.4 Plastic processing facilities for better waste management insights

Interactive map below provides a system that helps eco conscious users locate and visit plastic processing facilities so they can handle collected plastic waste responsibly. It makes it easier to find nearby places to clean, sort, and recycle plastic waste, supporting daily efforts to combat plastic pollution. By encouraging facility visits, the system helps reduce plastic waste in local communities and strengthens sustainable waste management.

<img src="https://github.com/Nikitaahlawat1/portfolio/blob/b2bb1640feaeff7dfd2ba490157e0e7be4d0d8bd/assets/re_fac.png" alt="Alt text" width="1000">
