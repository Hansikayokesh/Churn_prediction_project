
# Customer Churn Prediction






## Project Overview
The Customer Churn Prediction project aims to analyze and predict customer churn for a stationary company using sales data. By identifying customers who are likely to stop purchasing, the company can implement effective retention strategies to enhance customer loyalty and reduce revenue loss.
## Table Of Contents

- Technologies Used
- Dataset
- Feature Engineering
- Clustering Analysis
- Machine Learning Models
- Usage
- Visualizations
- Conclusion

## Technologies Used
- Python: Programming language used for data analysis and modeling.
- Pandas: Data manipulation and analysis library.
- NumPy: Library for numerical computations.
- Seaborn: Visualization library based on Matplotlib.
- Matplotlib: Library for creating static, animated, and interactive visualizations.
- Scikit-learn: Machine learning library for classification, regression, and clustering.
## Dataset
The project utilizes the "Stationary_Company_Sales_Data1.csv" dataset, which contains information on customer orders, including:

- Order Date: Date when the order was placed.
- Ship Date: Date when the order was shipped.
- Order Priority: Priority level of the order.
- Customer Name: Name of the customer
- Product Name: Name of the ordered product.
- Cost Price: Cost of the items ordered.
- Retail Price: Selling price of the items.
- Order Total: Total cost of the order.
- Shipping Cost: Cost incurred for shipping.
- Profit Margin: Profit earned from the order.
## Feature Engineering
Key features were engineered to assess customer behavior:

- Recency: Days since the last order was placed.
- Frequency: Total number of orders placed by the customer.
- Total Spending: Cumulative spending across all orders.
- Total Profit: Cumulative profit earned from all orders.
- Churn: Binary variable indicating whether a customer is likely to churn (1) or not (0).

### Rating binning

Customers were categorized into ratings (1-5) based on their recency, frequency, spending, and profit metrics.

## Clustering Analysis
KMeans clustering was employed to group customers into five distinct clusters based on their ratings. This segmentation helps in targeting specific customer groups for retention initiatives.


## Machine Learning Models
The project implements a voting classifier ensemble composed of the following models:

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier

### Model Training And Evaluation
- Data Splitting: The dataset is divided into training and testing sets.
- Hyperparameter Tuning: Optimized using GridSearchCV.
- Performance Metric: The model's performance is evaluated using the ROC AUC score.
## Usage
To predict churn for a new customer, you can use the predict_customer_churn function:

```javascript
predict_customer_churn(customer_name, recency_rating, frequency_rating, spending_rating, profit_rating)
```

### Example Usage
```javascript
predict_customer_churn("Priya", 3, 4, 2, 5)
```



## Visualizations
The following visualizations provide insights into the data and model performance:
- Missing Values Heatmap
This heatmap shows the distribution of missing values in the dataset.
![Heatmap]("Screenshot 2024-09-22 042031.png")
- Shipment Time Boxplot
This boxplot illustrates the distribution of shipment times across different shipment modes.
- Customer Clusters Barplot
This barplot depicts the number of customers in each cluster.

## Conclusion
This churn prediction model provides actionable insights into customer behavior, enabling the company to focus its marketing efforts and enhance customer retention strategies effectively.
