# Distributed Data Preprocessing Pipeline with Dask

## 🚀 Project Overview
This project addresses the challenge of handling data volumes that exceed the memory capacity of a single machine (Terabyte-scale data). It utilizes **Dask** (a parallel computing framework compatible with the Pandas API) to build a robust and scalable pipeline for cleaning, transforming, and performing complex feature engineering on large datasets in a distributed manner.

This showcases strong Data Engineering skills in scalable computation and cluster management.

## ⚙️ Key Technologies
* **Python:** Core scripting.
* **Dask:** Distributed DataFrame and Array computation.
* **Pandas:** For comparison and UDF (User Defined Function) definitions.
* **Docker Compose:** To orchestrate a Dask Scheduler and multiple Worker nodes.

## 📋 Project Scope and Deliverables
1.  **Data Simulation:** Generating a multi-gigabyte **[FILE TYPE]** dataset (e.g., Parquet, CSV) with common real-world issues (missing values, data type inconsistencies).
2.  **Cluster Setup:** Defining a Dask cluster configuration using `docker-compose.yml`.
3.  **Distributed Pipeline Implementation:** Implementing the following steps using Dask DataFrames:
    * Reading the large dataset in chunks.
    * Parallel filling of missing values (Imputation).
    * Complex, custom, window-based feature engineering (e.g., rolling averages).
    * Writing the processed data to a Data Lake (Parquet/Delta format).
4.  **Performance Benchmarking:** Comparing the wall-clock time required for the entire pipeline against a single-threaded Pandas implementation.

## 📊 Results and Benchmarks
The Dask-powered pipeline reduced the processing time for the **[DATASET SIZE] GB** dataset from **[PANDAS TIME] minutes (Pandas)** to **[DASK TIME] minutes (Dask)**, demonstrating a **[X]-fold** increase in processing efficiency through parallelism.

## 🏃 Getting Started
1.  Start the Dask cluster: `docker-compose up -d`
2.  Run the preprocessing script: `python dask_pipeline.py`
3.  Access the Dask Dashboard (port 8787) to monitor the task graphs and worker loads.
