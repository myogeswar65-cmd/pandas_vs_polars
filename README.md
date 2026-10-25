**Pandas and Polars:**

A comparative study of Pandas and Polars for data manipulation in Python, using a real-world retail transaction dataset. This project evaluates execution time, memory efficiency, and usability through practical data-processing operations and visualizations.

Overview

Pandas and Polars are popular Python libraries for working with structured data. Although both provide DataFrame operations, they differ in execution engines, memory management, and processing capabilities.

This project implements the same data-processing workflow using both libraries and compares their performance in Google Colab.

Objectives

- Understand the purpose and functionality of Pandas and Polars.
- Compare execution time for common data-processing operations.
- Measure and visualize DataFrame memory usage.
- Perform equivalent operations using both libraries.
- Identify the strengths, limitations, and suitable use cases of each library.

Dataset

Dataset: Online Retail

Source: UCI Machine Learning Repository
https://archive.ics.uci.edu/dataset/352/online+retail

The dataset contains retail transaction information, including:

- Invoice number
- Product code and description
- Quantity purchased
- Invoice date
- Unit price
- Customer ID
- Country

A sample of 150,000 records was used for the experiment to keep execution manageable in Google Colab.

Technologies Used

Technology| Purpose
Python| Programming language
Google Colab| Notebook environment
Pandas| Data manipulation and analysis
Polars| High-performance DataFrame processing
NumPy| Numerical operations
Matplotlib| Benchmark visualization
Requests and OpenPyXL| Dataset downloading and reading

Implementation Workflow

The same dataset and equivalent operations were used for both libraries.

1. Load Dataset: Load the shared CSV dataset using Pandas and Polars.
2. Filter Rows: Retain records with positive quantities and unit prices.
3. Select Columns: Select the columns required for analysis.
4. Group and Aggregate: Calculate total quantities, revenue, and unique invoice counts by product.
5. Join Datasets: Join aggregated sales with a product lookup table.
6. Sort and Transform: Sort products by revenue and calculate revenue per unit and revenue share.
7. Display Results: Display and validate the resulting tables.
8. Performance Benchmark: Measure execution time for each operation.
9. Memory Benchmark: Compare DataFrame memory usage.
10. Visualization: Create separate charts for performance and memory usage.

Performance Benchmark

The performance visualization compares execution time across loading, filtering, selection, grouping and aggregation, joining, and sorting and transformation.

The recorded results showed that Polars was faster for several operations, including loading, selection, grouping and aggregation, and joining. Pandas performed better for filtering in the observed run.

Performance may vary depending on the operation, data types, library versions, and runtime conditions.

Memory Benchmark

The measured DataFrame memory usage was:

Library| Memory Usage
Pandas| 39.91 MB
Polars| 11.90 MB

In this experiment, Polars used approximately 70.2% less DataFrame memory than Pandas.

These measurements represent the loaded DataFrames, not peak process memory during execution.

Key Findings

- Both libraries completed the required data-manipulation workflow.
- Polars showed substantially lower DataFrame memory usage in the recorded experiment.
- Polars performed better in several operations, while Pandas was faster for filtering in the observed run.
- Pandas offers a mature ecosystem and broad compatibility with Python data-science tools.
- Polars offers parallel execution and lazy query optimization capabilities.
- Benchmark results should be interpreted in the context of the specific dataset and environment.

Pandas vs. Polars

Feature| Pandas| Polars
API familiarity| Widely used and familiar| Different expression-based API
Execution| Primarily eager| Eager and lazy
Parallel processing| Limited automatic parallelism in standard operations| Supports parallel execution
Memory efficiency| Can use more memory depending on data types| Can provide a smaller memory footprint
Ecosystem| Extensive Python data-science integration| Growing ecosystem
Best suited for| Exploratory analysis and broad library compatibility| Efficient transformation pipelines and optimized processing



Conclusion

This project provided practical experience in comparing Pandas and Polars using a real-world retail dataset. By applying equivalent data-processing operations and measuring execution time and memory usage, the experiment demonstrated the differences between the two libraries.

The results favored Polars in memory efficiency and several measured operations, while Pandas performed better in certain individual steps. The appropriate library depends on the project's data volume, processing requirements, ecosystem compatibility, and measured performance.

How to Run

1. Open the notebook in this repository.
2. Open it in Google Colab.
3. Install the required dependencies if needed.
4. Run the notebook cells in sequence.
5. Review the resulting tables, benchmark measurements, and visualizations.

Repository Contents

- "pandas_vs_polars.ipynb" — Implementation and benchmark notebook.
- "Pandas_and_Polars_Report_M_Yogeswar.pdf" — Project report with analysis, observations, and visualizations.

Author

M Yogeswar

---

This project was created for educational purposes to explore DataFrame processing, performance benchmarking, memory analysis, and visualization in Python.
