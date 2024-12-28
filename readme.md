# 🌞 Solar Battery Storage Manufacturers Data Analysis

## 📖 Overview
This project analyzes and processes data related to solar battery storage manufacturers. It utilizes Python for data manipulation, visualization, and geographic analysis. The script processes raw data from an Excel file to generate insightful outputs about companies involved in the solar energy storage sector.

---

## ✨ Features
- **Data Cleaning and Preprocessing**: Renames and restructures columns for consistency.
- **Visualization**: Creates graphical representations of the data using libraries such as Matplotlib, Seaborn, and Plotly.
- **Geographic Analysis**: Visualizes data on maps using Folium and integrates Google Maps for enhanced geographical insights.
- **Scalable Workflow**: Includes progress tracking using TQDM for handling large datasets.

---

## ⚙️ Installation

To run this project, you need the following libraries:

```bash
pip install numpy pandas matplotlib seaborn plotly openpyxl googlemaps tqdm folium
```

Ensure you have **Python 3.7 or later** installed.

---

## 🚀 Usage

1. **Place your dataset** in the specified location. Update the file path in the script:
   ```python
   df = pd.read_excel(r"Enter the solar battery storage manufacturers excel file path")
   ```

2. **Run the Jupyter Notebook** to execute the analysis:
   ```bash
   jupyter notebook Solar_Battery_Storage_Manufacturers.ipynb
   ```

---

## 🔍 Key Sections

| Section            | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **Data Loading**   | Loads the raw dataset from an Excel file.                                  |
| **Data Cleaning**  | Renames columns and selects relevant data fields for analysis.             |
| **Visualization**  | Generates interactive and static graphs using Plotly, Matplotlib, and more.|
| **Geographic Mapping** | Displays company locations on an interactive map using Folium.         |
| **API Integration** | Uses Google Maps API for geocoding addresses into latitude and longitude. |

---

## 📚 Libraries Used
- **Pandas**: Data manipulation and cleaning.
- **Matplotlib** and **Seaborn**: Static data visualization.
- **Plotly**: Interactive visualizations.
- **Folium**: Geographic mapping.
- **Google Maps API**: For enhanced location insights.

---

## 🌐 Google Maps API Geocoding Details

The script integrates the Google Maps API to geocode addresses into latitude and longitude for accurate geographic mapping. Here is how it works:

1. **Setup**:
   - Obtain an API key from the [Google Cloud Console](https://console.cloud.google.com/).
   - Enable the Geocoding API for your project.

2. **Integration**:
   - Replace the placeholder `YOUR_API_KEY` in the script with your actual API key:
     ```python
     gmaps = googlemaps.Client(key='YOUR_API_KEY')
     ```

3. **Geocoding Addresses**:
   - Use the `geocode` method to convert addresses into geographic coordinates:
     ```python
     geocode_result = gmaps.geocode('1600 Amphitheatre Parkway, Mountain View, CA')
     latitude = geocode_result[0]['geometry']['location']['lat']
     longitude = geocode_result[0]['geometry']['location']['lng']
     ```

4. **Batch Processing**:
   - The script processes multiple addresses using a loop and TQDM for progress tracking:
     ```python
     for address in tqdm(addresses):
         geocode_result = gmaps.geocode(address)
         # Extract latitude and longitude
     ```

---


## 📧 Contact

For any questions or support, please contact:
- **Name**: Lavish Isasare
- **Email**: lavishisasare@gmail.com

---

**🌟 Happy Coding! 🌟**

