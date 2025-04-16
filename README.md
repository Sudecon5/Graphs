# Graphs: A quick overview 
Different types of graphs are used based on the nature of the data and the insights one wants to convey.
## Types of Graphs 📍
### 1. Bar Graph ☑️
**When to Use:**<br/>
 -Compare categories (e.g., sales by product).<br/>
 -Show discrete data with distinct groups.<br/>
**Example:**<br/>
-Comparing GDP of different countries.<br/>
-Sales performance across regions.<br/>

**Code in Python**💻
```
#Libraries
import numpy as np
import matplotlib.pyplot as plt

#Make a random dataset:
height = [3, 12, 5, 18, 45]
bars = ('A', 'B', 'C', 'D', 'E')
y_pos = np.arange(len(bars))

#Create bars
plt.bar(y_pos, height)

#Create names on the x-axis
plt.xticks(y_pos, bars)

Show graphic
plt.show()
```
### 2. Line Graph ☑️
**When to Use:**<br/>
-Track trends over time (e.g., stock prices, temperature changes).<br/>
-Show continuous data.<br/>
**Example**<br/>
-Monthly revenue growth.<br/>
-Temperature fluctuations across seasons.<br/>
**Code in python** 💻
```
import matplotlib.pyplot as plt
import numpy as np

ypoints = np.array([3, 8, 1, 10])

plt.plot(ypoints, linestyle = 'dotted')
plt.show()
```
### 3. Pie Chart☑️
**When to Use:**<br/>
-Show proportions or percentages of a whole. <br/>
-Highlight composition (e.g., budget allocation). <br/>
**Example:**<br/>
-Market share of companies. <br/>
-Distribution of expenses in a budget. <br/>
**Code in Python**💻
```
import matplotlib.pyplot as plt
labels = 'Elephant', 'Rabbit', 'Dogs', 'Cat'
sizes = [15, 30, 45, 10]

fig, ax = plt.subplots()
ax.pie(sizes, labels=labels)
```
### 4. Histogram☑️
**When to Use:**<br/>
-Display frequency distribution of continuous data.<br/>
-Identify patterns (e.g., normal distribution).<br/>
**Example:**<br/>
-Age distribution in a population.<br/>
-Exam score ranges.<br/>
**Code in Python**💻
```
counts, bins = np.histogram(x)
plt.stairs(counts, bins)
```
### 5. Scatter Plot☑️
**When to Use:**<br/>
-Reveal relationships between two variables. <br/>
-Identify correlations or outliers. <br/>
**Example:**<br/>
-Height vs. Weight analysis.<br/>
-Advertising spend vs. Sales.<br/>
**Code in Python**💻
```
import matplotlib.pyplot as plt
import numpy as np

x = np.array([5,7,8,7,2,17,2,9,4,11,12,9,6])
y = np.array([99,86,87,88,111,86,103,87,94,78,77,85,86])

plt.scatter(x, y)
plt.show()
```
### 6. Stacked Bar Graph☑️
**When to Use:** <br/>
-Compare totals across categories while showing sub-category breakdowns. 
**Example:** <br/>
-Total sales by region, split by product lines. <br/>
**Code in Python**💻
```
import plotly.express as px

long_df = px.data.medals_long()

fig = px.bar(long_df, x="nation", y="count", color="medal", title="Long-Form Input")
fig.show()
```
### 7. Box Plot (Box-and-Whisker)☑️
**When to Use:** <br/>
-Show data spread (median, quartiles, outliers). <br/>
-Compare distributions across groups. <br/>
**Example:** <br/>
-Salary distribution across departments. <br/>
**Code in Python**💻<br/>
```
import matplotlib.pyplot as plt
import numpy as np
# Generates multiple datasets
data1 = np.random.normal(0, 1, 100)
# Creates subplots
fig, axs = plt.subplots(1, 3, figsize=(15, 5))
# Plots Boxplot for Data 1
axs[0].boxplot(data1)
axs[0].set_title('Data 1')
axs[0].set_xlabel('Sample')
axs[0].set_ylabel('Value')
# Adjusts layout
plt.tight_layout()
plt.show()
```
### 8. Heatmap☑️
**When to Use:** <br/>
-Visualize matrix data (e.g., correlation matrices).<br/> 
-Show intensity (e.g., website clicks by hour/day). <br/>
**Example:**<br/>
-Correlation between variables in a dataset.<br/> 
**Code in Python**💻
```
# Calculate the correlation matrix
correlation_matrix = filtered_df.corr()

# Create the heatmap
plt.figure(figsize = (10,8))
sns.heatmap(correlation_matrix, cmap = 'coolwarm')
plt.show()
```
### 9.Area Graph☑️
**When to Use:**<br/>
-Emphasize cumulative totals over time. <br/>
**Example:** <br/>
-Stacked area chart for multi-category trends (e.g., revenue by product). <br/>
**Code in Python**💻
```
# library
import numpy as np
import matplotlib.pyplot as plt

# Create data
x=range(1,6)
y=[1,4,6,8,4]

# Area plot
plt.fill_between(x, y)
plot.show()
```
### 10. Bubble Chart☑️
**When to Use:**<br/>
-Emphasize cumulative totals over time. <br/>
Example: <br/>
-Stacked area chart for multi-category trends (e.g., revenue by product).<br/> 
**Code in Python**💻
```
# library
import numpy as np
import matplotlib.pyplot as plt

# Create data
x=range(1,6)
y=[1,4,6,8,4]

# Area plot
plt.fill_between(x, y)
plot.show()
```

For more documentation and API regarding graphs follow
| [w3school](https://www.w3schools.com/python/matplotlib_pyplot.asp),
 [DataCamp](https://www.datacamp.com/tutorial/matplotlib-tutorial-python),
 [Matplotlib](https://matplotlib.org) |
