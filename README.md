week 1 :  Let’s say you’re a Product Data Scientist at Instagram. How would you measure the success of the Instagram TV product?
### **Step 1: Define The Product on IGTV

User Engagement Metrics:

Viewership: Measure the number of views on IGTV content. Track daily, weekly, and monthly views to identify trends and spikes.
Watch Time: Analyze the total time users spend watching IGTV videos. This metric provides insights into user engagement and content quality.
Completion Rate: Calculate the percentage of viewers who watch an entire IGTV video. Higher completion rates indicate compelling content.
Audience Growth:

Followers: Track the growth in the number of followers for IGTV channels. A steady increase in followers suggests interest in the platform.
Audience Retention: Monitor the churn rate of followers to identify if users are unfollowing IGTV channels at a high rate.
Content Metrics:

Upload Frequency: Measure how often creators are uploading IGTV content. Consistent content uploads can keep users engaged.
Content Type: Categorize and analyze the types of content (e.g., tutorials, vlogs, interviews) that perform well and drive user engagement.
Likes, Comments, and Shares: Assess user interactions with IGTV content, including the number of likes, comments, and shares. High engagement indicates content quality.


### **Step 2:Data Collection and Data Cleaning.

The data collwction was with Mookcrack.
```python


```python
import pandas as pd
import numpy as np
import seaborn as sns 
import matplotlib.pyplot as plt

data = pd.read_csv(r"C:\Users\Chaloh\Downloads\Instagram TV Product Report.csv")
# Handle missing values 
data.shape
data.isnull().sum()
#To see the colomns
data.colomns
#To see the data uniqueness
data.nunique()
data.['likes'].unique() 
##Read your data
data.info()
##Handle missing data
data.dropna(inplace=True)
```


### **Step 3:Data Visualization

Visualize your data to gain insights. Create plots, histograms, scatter plots, and other visualizations to understand the distribution and relationships within you
```python
## Scatter
plt.scatter(df['feature1'], df['feature2'])
plt.xlabel('Feature 1')
plt.ylabel('Feature 2')
plt.title('Scatter Plot')
plt.show()
##Histogram
plt.hist(data, bins=20)
plt.xlabel('X-axis label')
plt.ylabel('Y-axis label')
plt.title('Histogram of a Variable')
plt.show()

```


### **Step 4:Exploratory Data Analysis

Perform deeper exploratory analysis by asking questions and exploring patterns in the data. You can use Pandas operations and Seaborn/Matplotlib for advanced visualizations.

```python
##Correlation Heat Map
corr_matrix = df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()
## Gropued bar chart
sns.barplot(x='category', y='value', data=df)
plt.xlabel('Category')
plt.ylabel('Value')
plt.title('Grouped Bar Chart')
plt.show()

```


### **Step 6:Feature Engineering

Create new features or transform existing ones if needed. Feature engineering can improve the quality of your data for modeling

### **Step 7:Document Your Findings

Keep a record of your observations, insights, and any actions taken during the EDA process. Jupyter Notebooks are great for creating documentation that combines code, visualizations, and explanations.

