# Financial Market Analysis and Prediction System

## Project Overview
This project implements an end-to-end system for analyzing and predicting financial market trends using Apache Spark for distributed data processing and MongoDB Atlas for scalable storage. The system processes large volumes of historical stock market data, applies machine learning models for price prediction, and provides insights through data visualization.

**Disclaimer**: This project is for educational purposes only. Do not use it for making financial decisions.

## Features
- **Data Processing**: Handles large-scale financial data with preprocessing, feature engineering, and normalization.
- **Machine Learning Models**: Implements Linear Regression, ARIMA, and Random Forest models for stock price prediction.
- **Performance Optimization**: Utilizes Parquet for storage, batch/stream processing, and MongoDB indexing strategies.
- **Visualization**: Generates insights through correlation matrices, volatility patterns, and technical indicators.

## Dataset
The dataset includes historical market data for multiple stock tickers (e.g., AAPL, MSFT, TSLA) and indices (SPY, QQQ) from January 1960 onwards. Each record contains:
- Open/High/Low/Close prices
- Trading volume
- Technical indicators (e.g., moving averages, Bollinger Bands)

## System Architecture
1. **Data Ingestion**: Collects data from external sources.
2. **Spark Processing**: Performs distributed transformations, aggregations, and caching.
3. **MongoDB Storage**: Stores processed data and predictions with optimized indexing.
4. **Model Training**: Trains and evaluates ML models on historical data.
5. **Visualization**: Displays insights and predictions.

## Key Results
- **Model Performance**: Linear Regression outperformed ARIMA and Random Forest (RMSE: 1.05, R²: 0.9996).
- **Storage Comparison**: Parquet format showed 60% faster querying than CSV.
- **Processing**: Batch processing had higher throughput, while streaming offered lower latency.

# Requirements

- Python 3.8 or higher  
- Java JDK 8 or 11  
- Apache Spark (3.x)  
- MongoDB Atlas account  
- Jupyter Notebook
  
## Open Notebook in Google Colab

Open the notebook `integrated_spark_mongodb_notebook.ipynb` in Google Colab.

## Install Dependencies

```bash
pip install pyspark notebook
```

For MongoDB connector:

```bash
pip install pymongo
```

## Download MongoDB Spark Connector

- Download the connector `.jar` file from [MongoDB Connector for Spark](https://www.mongodb.com/docs/spark-connector/current/installation/)
- Place it in a known directory (e.g., `C:\spark\jars`)

## Run the cells

`integrated_spark_mongodb_notebook.ipynb` and run the cells.

# Notes

- Use your **MongoDB Atlas connection string** (with credentials) in the Spark session builder.  
- Ensure your Atlas cluster allows access from your IP address.  
- Update the Spark session builder in the notebook with the correct `.jar` file path.


## Future Work
- **Advanced Modeling**:  
  Integrate transformer-based models and reinforcement learning.
- **Real-time Features**:  
  Add real-time data streaming and alerting mechanisms.
- **Dashboard Development**:  
  Develop an interactive dashboard with user authentication.

## Contributors
- Sawsan Abdulbari  
- Linda Marin  
- Yasmin Ebrahimi  

## License  
This project is for educational use only. See the repository for details.  

## Contact  
For questions or contributions, please open an issue on the [GitHub repository](https://github.com/SawsanAbdulbari/ml-finance-spark-mongodb).
