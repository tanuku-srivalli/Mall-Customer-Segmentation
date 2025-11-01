# Mall-Customer-Segmentation
----

## Mall Customer Segmentation using K-Means Clustering

-----

### **Overview**

This project applies the **K-Means Clustering** algorithm, an **unsupervised machine learning** technique, to segment a mall's customer base. By grouping customers based on key attributes—specifically their **Annual Income** and **Spending Score**—we aim to uncover distinct market segments.

The goal is to provide **actionable intelligence** to the marketing team, enabling them to design highly **targeted and personalized campaigns** for each segment, maximizing customer engagement and profitability.

### **Dataset**

The analysis is performed on the standard Mall Customer Segmentation dataset, which contains basic information about 200 customers.

| Feature | Description | Data Type |
| :--- | :--- | :--- |
| `CustomerID` | Unique identifier for the customer. | `int64` |
| `Gender` | Male or Female. | `object` |
| `Age` | Age of the customer. | `int64` |
| `Annual Income (k$)` | Customer's annual income in thousands of dollars. | `int64` |
| `Spending Score (1-100)` | Score assigned by the mall based on customer behavior. | `int64` |

### **Project Structure**

The project execution is organized into three main phases:

1.  **Data Preparation:** Load data and select the relevant features (`Annual Income (k$)` and `Spending Score (1-100)`) for clustering.
2.  **Model Tuning (Elbow Method):** Determine the optimal number of clusters ($\text{K}$) by calculating the **Within-Cluster Sum of Squares (WCSS)**, also known as Inertia.
3.  **Final Model & Visualization:** Train the K-Means model with the optimal $\text{K}$ and visualize the results using a scatter plot, identifying the cluster centroids.

### **Installation and Requirements**

To run the Python script, you will need the following libraries. You can install them using `pip`:

```bash
pip install pandas matplotlib scikit-learn numpy
```

### **Key Results: The 5 Customer Segments**

The **Elbow Method** determined that $\text{K}=5$ is the optimal number of clusters. The resulting visualization clearly separates the customer base into five distinct, targetable groups:

| Cluster | Income Level | Spending Score | Persona | Strategic Focus |
| :--- | :--- | :--- | :--- | :--- |
| **0** (Low/Low) | Low | Low | **Miserly** | Low priority; general marketing. |
| **1** (Medium/Medium) | Average | Average | **Balanced** | Standard promotional campaigns. |
| **2** (High/Low) | High | Low | **Careful Spenders** | Focus on luxury items or high-value incentives to increase spend. |
| **3** (Low/High) | Low | High | **Target** | High retention priority; offer discounts and loyalty rewards. |
| **4** (High/High) | High | High | **VIPs** | **Most Important Segment**; offer exclusive, premium services and personalized experiences. |

### **Visualization of Clusters**

The scatter plot below (similar to the image provided) shows the separation of customers based on their two key metrics, with the black 'X' marking the cluster **centroids**.

```
# Conceptual image of the final K-Means plot
 
```

### **Usage**

1.  Ensure you have the `Mall_Customers.csv` file in the same directory as your Python script.

2.  Run the script:

    ```bash
    python your_script_name.py
    ```

3.  The script will output the **Elbow Plot** to help confirm $\text{K}=5$, and the final **Customer Segment Scatter Plot** showing the 5 clusters.

-----
