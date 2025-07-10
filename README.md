# Project Credit Card Churn Analysis

**Project Credit Card Churn Analysis** is a comprehensive group data analysis project focused on exploring and understanding the factors that influence customer attrition in the credit card industry. Using a real-world dataset from Kaggle, this project investigates how customer demographics, financial behaviour, and product usage patterns impact churn rates. The analysis includes data transformation, Power BI dashboard creation, and hypothesis validation to provide actionable insights for customer retention strategies.
The project incorporates data extraction, transformation, visualisation, and business insights using Python and Power BI.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
The dataset used in this project is sourced from [Kaggle: Bank Churners Dataset](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers). It contains records of credit card customers, capturing both demographic and financial attributes that may influence customer churn behaviour.

**Features include:**
- `Customer_Age`: Age of the customer (numeric)
- `Gender`: Gender of the customer (`M`, `F`)
- `Education_Level`: Educational background (High School, Graduate, etc.)
- `Marital_Status`: Marital status (Single, Married, Divorced)
- `Income_Category`: Annual income range categories
- `Credit_Limit`: Customer's credit limit (numeric)
- `Total_Trans_Amt`: Total transaction amount (numeric)
- `Attrition_Flag`: Whether customer churned (`Existing Customer`, `Attrited Customer`)

## Business Requirements
We will be focusing on 4 key requirements:
* 1. Analyse the relationship between credit limits and customer churn
* 2. Investigate how transaction amounts correlate with attrition rates
* 3. Examine demographic factors (education, marital status) that influence churn
* 4. Identify high-risk customer segments for targeted retention strategies


## Hypothesis and how to validate?
1. **Hypothesis:** Attrited customers have significantly lower total transaction amounts than existing customers..
   - **Validation** Created a clustered column chart comparing Total_Trans_Amt for attrited vs. existing customers using a custom visual.

2. **Hypothesis** Customer attrition is higher among clients with lower credit limits.
   - **Validation:** Created a bar chart showing average Credit_Limit grouped by Attrition_Flag.

3. **Hypothesis:** Attrition rates vary by marital status, with single customers having higher churn.
   - **Validation:** Clustered bar chart of Attrition_Flag counts by Marital_Status.

4. **Hypothesis:** Customers with lower education levels tend to churn more often than those with higher education levels.  
   - **Validation:** Created a 100% stacked bar chart showing proportion of attrited vs existing customers by education level, supplemented with calculated attrition rates for proper comparison.
 

## Key Findings & Business Insights

### Dashboard Results Summary
Based on the Power BI dashboard analysis, the following key insights were discovered:

#### Customer Demographics & Churn Patterns
- **Total Customer Base:** [Insert your total customer count from KPI card]
- **Overall Churn Rate:** [Insert your churn rate percentage from KPI card]
- **Age Groups:** [Describe which age groups have highest/lowest churn rates - e.g., "Customers aged 40-50 show the lowest churn rate at X%, while younger customers (20-30) have higher churn at Y%"]
- **Gender Distribution:** [Describe any gender-based churn patterns from your analysis]

#### Financial Behavior Insights
- **Credit Limit Impact:** [Describe relationship - e.g., "Customers with credit limits below $5,000 show 25% higher churn rates, confirming our hypothesis"]
- **Total Transaction Amount:** [Describe spending patterns - e.g., "Churned customers had average transaction amounts of $X compared to $Y for retained customers"]
- **Card Category Performance:** [Describe which card types have higher churn - e.g., "Blue cards show highest churn at X%, while Platinum cards have lowest at Y%"]

#### Product & Service Insights
- **Card Category Distribution:** [Describe the distribution - e.g., "Blue cards represent 80% of customer base but also 85% of churn, indicating need for Blue card retention strategies"]
- **Relationship Count:** [Describe how number of products affects retention - e.g., "Customers with 3+ products show 40% lower churn rates"]

### Strategic Recommendations
1. **Customer Retention Strategies:** Focus retention efforts on high-risk segments (lower credit limits, single-product customers)
2. **Product Development:** Enhance Blue card benefits and consider premium upgrade incentives
3. **Risk Management:** Implement early warning systems for customers showing declining transaction patterns
4. **Marketing Focus:** Target middle-aged customers (40-50) for expansion as they show highest retention rates

### Business Impact
- **Revenue Protection:** [Estimate revenue at risk from churn based on your analysis]
- **Customer Lifetime Value:** [Insights on high-value customer characteristics]
- **Operational Efficiency:** [Recommendations for resource allocation to retention efforts]

## Project Plan
The project followed these steps:
* 1. Data Extraction: Load the CSV dataset using pandas to analyze credit card customer data.
* 2. Data Cleaning and Transformation: Checked for missing values, duplicates and ensured correct data types for customer demographics and financial data.
* 3. Power BI Dashboard Creation: Built comprehensive dashboard with KPI cards, bar charts, and pie charts to visualize customer churn patterns.
* 4. Hypothesis Testing: Each visualization was designed to test specific business hypotheses about customer churn behavior.
* 5. Analysis and Interpretation: Analyzed patterns in customer demographics, financial behavior, and product usage to identify churn drivers.

## The rationale to map the business requirements to the Data Visualisations
I used different types of visualizations for each business requirement in Power BI:
1. **KPI Cards** for key metrics (Total Customers, Churn Rate, Existing vs. Attrited)
2. **Bar Charts** for comparing churn rates across demographics (Age Groups, Education Level, Income Category)
3. **Pie Charts** for showing distribution of categorical data (Card Category, Gender)
4. **Average calculations** for financial metrics (Credit Limit, Transaction Amounts)
I chose these visualizations as they clearly show the relationship between customer characteristics and churn behavior, making it easy for stakeholders to understand retention patterns.

## Analysis techniques used
* Power BI DAX measures for churn rate calculations
* Grouped bar charts for demographic comparisons
* KPI cards for key performance indicators
* Age group binning for better demographic analysis
* Comparative analysis between attrited vs. existing customers
**Limitations**: The dataset lacks variables like customer acquisition cost, customer service interactions, or detailed product usage patterns, which could further explain churn behavior.
**Alternative approaches**: Machine learning models could be used for churn prediction, but this exploratory analysis focused on hypothesis validation through visualization.
**Use of AI tools**: ChatGPT was used for Power BI guidance, dashboard design best practices, and README formatting.

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

## Main Analysis Tools
* **Power BI Desktop** – for creating interactive dashboards and visualizations
  - KPI cards for key metrics
  - Bar charts for demographic analysis
  - Pie charts for categorical distributions
  - DAX measures for churn rate calculations
* **pandas** – for initial data loading and inspection
  - `df = pd.read_csv('BankChurners.csv')`
* **Power BI Data Model** – for data relationships and calculated columns
  - Age group binning
  - Churn rate measures
  - Customer segmentation

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
