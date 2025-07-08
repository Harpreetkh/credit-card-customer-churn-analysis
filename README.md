# Project Credit Card Churn Analysis

**Project Credit Card Churn Analysis** is a data analysis project focused on exploring and understanding the factors that influence healthcare insurance charges. Using a real-world dataset, this project investigates how personal attributes (such as age, gender, BMI, family size, and smoking habits) and geographic factors impact insurance costs. The analysis includes data cleaning, visualization, and predictive modeling to provide actionable insights for estimating healthcare expenses.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
The dataset used in this project is sourced from [Kaggle: Healthcare Insurance Dataset](https://www.kaggle.com/datasets/willianoliveiragibin/healthcare-insurance/data). It contains records of individuals, capturing both personal and geographic attributes that may influence healthcare insurance charges.

**Features include:**
- `age`: Age of the primary beneficiary (numeric)
- `sex`: Gender of the insured individual (`male`, `female`)
- `bmi`: Body Mass Index, providing an indication of body fat (numeric)
- `children`: Number of dependents covered by insurance (numeric)
- `smoker`: Smoking status of the individual (`yes`, `no`)
- `region`: Residential region in the US (`northeast`, `northwest`, `southeast`, `southwest`)
- `charges`: Individual medical insurance costs billed by health insurance (numeric)

## Business Requirements
I will be focusing on 3 requirements:
* 1. Does smoking effect insurance charges?
* 2. Identify how insurance charges vary across different regions.
* 3. Look into how BMI and whether someone smokes affects their insurance charges.


## Hypothesis and how to validate?
1. **Hypothesis:** Attrited customers have significantly lower total transaction amounts than existing customers..
   - **Validation** Created a boxplot comparing Total_Trans_Amt for attrited vs. existing customers using a custom visual.

2. **Hypothesis** Customer attrition is higher among clients with lower credit limits.
   - **Validation:** Created a bar chart showing average Credit_Limit grouped by Attrition_Flag.

3. **Hypothesis:** Attrition rates vary by marital status, with single customers having higher churn.
   - **Validation:** Clustered bar chart of Attrition_Flag counts by Marital_Status.

4. **Hypothesis:** Customers with lower education levels tend to churn more often than those with higher education levels.  
   - **Validation:** Create a 100% stacked bar chart in Power BI showing the proportion of attrited versus existing customers for each education level to compare churn rates across education groups.

## Project Plan
The project followed these steps:
* 1. Data Extraction: Load the CSV dataset using pandas.
* 2. Data Cleaning and Transformation: Checked for missing values, duplicates and ensured correct data types.
* 3. Data visualisation: Used matplotlib, seaborn and plotly to explore relationships and patterns.
* 4. Analysis and Interpretation: Each visualisation answered a business question and helped confirm or reject the hypothesis.

## The rationale to map the business requirements to the Data Visualisations
I used a different type of visualisation for each of th business requirements. For each question I used:
1. Boxplot for comparing the distribution of smoker vs non smoker in comparison to charges.
2. Barchart to show regional averages.
3. Scatterplot with trendline for analysing correlation of BMI and smoking against insurance charges.
I chose those specific visualisations as it was easier to see the relationship between the different factors and insurance charges. Also, it was appropriate for the type of data that was given.

## Analysis techniques used
* Descriptive statistics (describe(), groupby() methods)
* Boxplots and bar charts for comparison
* Scatter plots for correlation
* OLS trendline in Plotly for regression pattern detection
**Limitations**: The dataset lacks variables like pre-existing conditions, income, or employment type, which could further explain insurance charges.
**Alternative approaches**: Machine learning models could be used for prediction, but this was outside the scope of this exploratory analysis.
**Use of AI tools**: ChatGPT was used to get help with coding issues, visualisation tweaks, and Markdown formatting.

## Ethical considerations
* This data did not include any personal identifiable information so there were no data privacy concerns.

## Development Roadmap
**Challenges faced**:
* Activating and using a virtual environment in VS Code. I wasn't sure how to do this.
* Installing and managing required libraries. I assumed these would already be installed.
* Plotly errors related to rendering in Jupyter.
**Overcoming them**:
* I used ChatGPT and Github Copilot in VSCode to troubleshoot technical issues.
* I restarted kernels and updated environment settings.
**Next steps**:
* Including more data within the visualisations.
* Explore more advanced modelling.

## Main Data Analysis Libraries
* pandas – for data loading, cleaning, and transformation
df = pd.read_csv('insurance.csv')
* matplotlib – for static plots
plt.figure(figsize=(8,6))
* seaborn – for statistical visualisations
sns.boxplot(data=df, x='smoker', y='charges')
* plotly.express – for interactive charts
px.scatter(df, x='bmi', y='charges', color='smoker', trendline='ols')

## Reflection
Working on this project was a great learning experience. At the beginning, I ran into a few bumps — like setting up the virtual environment and trying to get GitHub to stop asking me to log in every time I pushed something. It was a bit annoying, but after some trial and error (and help from ChatGPT), I managed to sort it all out.

I also had to troubleshoot a few coding issues, especially when using Plotly. Sometimes the graph wouldn’t show or there were strange errors I didn’t understand at first. Each time, I took the time to dig into what was going wrong and learned a bit more about how things work in Python and Jupyter Notebooks.

Throughout the project, I made sure to stay on track with the business goals and keep my code and markdown sections tidy and clear. If I were to improve anything, I’d maybe try to use even more visualisation types or dig deeper into prediction techniques. But overall, I’m happy with how the project turned out and I feel like I’ve come a long way from where I started.

## Credits 
### Content 
- **ChatGPT**  
  I used ChatGPT extensively to guide me through the project when I encountered issues. Specific examples include:
  - Understanding how to structure markdown cells and write hypotheses and objectives.
  - Troubleshooting errors such as:
    - The `plotly` error due to a missing `nbformat` installation.
    - A `SyntaxError` with no clear trace — eventually resolved by restarting VS Code.
    - Problems with activating the virtual environment in the terminal.
  - Helping to format visualizations, like:
    - Removing error bars from a seaborn bar plot.
    - Adding a box around the legend in a Plotly scatter plot.
  - Explaining technical concepts including:
    - What `groupby().mean().reset_index()` does.
    - The difference between `sns.barplot()` and `plt.bar()`.
    - The purpose and function of legends and trendlines in data visualisations.

- **GitHub Copilot**  
  GitHub Copilot in VS Code assisted with autocompleting repetitive code and suggesting clean syntax throughout the project, especially during data visualisation and transformation tasks.

- **External Dataset Sources**  
  I reviewed exploratory analysis notebooks from other users on [Kaggle](https://www.kaggle.com/datasets/willianoliveiragibin/healthcare-insurance/data) to gain insight into typical approaches. I adapted some initial code for loading and inspecting the data (like using `.info()`, `.describe()`, and `.isnull().sum()`) from these examples.

## Acknowledgements
Thanks to:
* Code Institute for the project structure
* Kaggle for providing the dataset
* OpenAI for ChatGPT
* GitHub Copilot for coding support
* Code Institute peers for being supportive along the way
