# BigQuery

This is a SQL script to create a logistic regression model in BigQuery. The model predicts whether a visitor will make a purchase on a return visit to an e-commerce website. The script first creates a temporary table 'all_visitor_stats' that groups visitors by their ID and labels them as 1 (will make a purchase on a return visit) or 0 (will not make a purchase on a return visit).

Then, it selects features for each unique session, such as the latest e-commerce progress, bounce rate, time on site, page views, traffic source, device category, and country. These features are selected from the 'web_analytics' table and joined with the 'all_visitor_stats' table using the visitor ID.

The script only predicts for new visits and uses data from August 2016 to April 2017 for training. The model is named 'classification_model_2' and is saved in the ecommerce dataset.

Please ensure that you have the necessary permissions and quota on BigQuery before running this script. Also, replace the dataset and table names with your actual dataset and table names if they are different.

Remember, machine learning models are only as good as the data they are trained on. So, make sure your data is clean and relevant!
