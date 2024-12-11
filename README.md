# Automatidata's Data Analytic Project

## **Overview**

This project focuses on analyzing operational and performance data for Automatidata, providing actionable insights into system efficiency, resource utilization, and performance trends. Using Python, the analysis identifies key metrics and trends to drive strategic improvements.

## **Objectives**

- Explore operational and performance data for insights.
- Identify patterns and anomalies in system performance.
- Provide actionable recommendations for improving efficiency.

## **Key Features**

- **Data Cleaning and Preparation**: Handles missing values, outliers, and inconsistent formats.
- **Performance Analysis**: Investigates key performance indicators (KPIs) like uptime and response time.
- **Trend Analysis**: Visualizes temporal changes in performance metrics.
- **Anomaly Detection**: Highlights unusual patterns or data points.

## **Technologies Used**

- **Python**: Main language for analysis.
- **Libraries**:
  - `Pandas` and `NumPy`: Data manipulation and preprocessing.
  - `Matplotlib` and `Seaborn`: Visualization.
  - `SciPy` or `Statsmodels`: Statistical analysis and anomaly detection.
  - `Jupyter Notebook`: Interactive environment for coding and visual exploration.

## **Dataset Information**

- The dataset includes:
  - System metrics (uptime, response time).
  - Resource utilization data (CPU, memory).
  - Event logs and timestamps.

## **Steps to Reproduce**

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/AnalyticJosh/Automatida-s-Data-Analytic-Project.git
   cd Automatida-s-Data-Analytic-Project
   ```

2. **Set Up the Environment**:

   - Ensure Python (3.7 or higher) is installed.
   - Install required libraries:
     ```bash
     pip install -r requirements.txt
     ```

3. **Run the Notebook**:

   - Open `Automatidata_Project.ipynb` in Jupyter Notebook.
   - Execute cells sequentially to preprocess data, analyze trends, and generate insights.

## **Sample Analysis**

### Response Time Analysis

```python
sns.lineplot(x='Timestamp', y='ResponseTime', data=data)
plt.title('Response Time Over Time')
plt.show()
```

### Anomaly Detection in Resource Utilization

```python
from scipy.stats import zscore

data['CPU_Zscore'] = zscore(data['CPU_Usage'])
data['Anomaly'] = data['CPU_Zscore'].apply(lambda x: 'Yes' if abs(x) > 3 else 'No')
```

## **Results and Insights**

- Key findings:
  - Response times remained stable during most periods but spiked during high usage hours.
  - Resource utilization anomalies were detected during peak traffic, indicating bottlenecks.
  - System uptime was consistent at 99.8%, but performance dipped during maintenance windows.
- Suggested strategies:
  - Optimize resource allocation during peak periods.
  - Implement predictive maintenance strategies to minimize performance dips.

## **Visualizations**

- **Response Time Trends**: Line chart showing variations over time.
- **Resource Utilization**: Heatmap of CPU and memory usage.
- **Anomalies**: Scatter plot highlighting detected anomalies.

## **Contributions**

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a Pull Request.

## **License**

This project is licensed under the MIT License.

---

For further inquiries or feedback, please contact [Joshua Amusan](mailto\:joshuaanalyst2@gmail.com).

