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
 

## Key Findings
1. Created the following **new features:** Transactions per Month and Average Transaction Amount.
2. **Lower transaction frequency indicates higher churn risk**
   Customers who make fewer transactions per month (especially <2) show significantly higher attrition rates. This highlights engagement frequency as a powerful early warning signal for churn.
3. **Credit limit and utilization matter**
   Attrited customers consistently have lower credit limits and lower utilization ratios. These financial indicators suggest that low product value perception or credit access may drive disengagement.
4. **Demographics show weak predictive power**
   While differences exist in income, education, and marital status between attrited and retained customers, their statistical significance is limited. Behaviour-based features (e.g., transaction patterns) are far more predictive.
Of the chosen hypotheses, we negated two of them — Marital status and Education levels. We wanted to further deepen our analysis and formulated three more hypotheses.
5. Behavioral indicators — particularly **spending levels**, **transaction frequency**, and **credit limit** — are stronger predictors of churn than demographics like income, education, or marital status.
Intervening early with customers who show low credit usage, reduced spending, or limited credit limits can help prevent attrition. Targeted engagement strategies (e.g., usage incentives, credit upgrades, and value-added services) should be prioritized over demographic targeting.


## Business Findings
1. Focus on Transaction Activity: Monitor customers with declining transaction amounts - this is your best early warning system
2. Graduate Customer Retention: Develop specific retention strategies for graduate-level customers who show unexpectedly high churn
3. Single Customer Engagement: Create targeted programs for single customers who appear more prone to churn
4. Proactive Monitoring: Implement alerts for customers showing low transaction patterns

## Project Plan
The project followed these steps:
* 1. Data Extraction: Load the CSV dataset using pandas to analyse credit card customer data.
* 2. Data Cleaning and Transformation: Checked for missing values, duplicates and ensured correct data types for customer demographics and financial data.
* 3. Power BI Dashboard Creation: Built comprehensive dashboard with KPI cards, bar charts, and pie charts to visualize customer churn patterns.
* 4. Hypothesis Testing: Each visualisation was designed to test specific business hypotheses about customer churn behaviour.
* 5. Analysis and Interpretation: Analysed patterns in customer demographics, financial behaviour, and product usage to identify churn drivers.

## The rationale to map the business requirements to the Data Visualisations
We used different types of visualisations for each business requirement in Power BI:
1. **KPI Cards** for key metrics (Total Customers, Churn Rate, Existing vs. Attrited)
2. **Bar Charts** for comparing churn rates across demographics (Age Groups, Education Level, Income Category)
3. **Pie Charts** for showing distribution of categorical data (Card Category, Gender)
4. **Average calculations** for financial metrics (Credit Limit, Transaction Amounts)
We chose these visualisations as they clearly show the relationship between customer characteristics and churn behaviour, making it easy for stakeholders to understand retention patterns.

## Analysis techniques used
* Power BI DAX measures for churn rate calculations
* Grouped bar charts for demographic comparisons
* Mann-Whitney U Test for hypotheses validation.
* Plotly boxplots to visualise the result of the hypotheses validation process.
* KPI cards for key performance indicators
* Age group binning for better demographic analysis
* Comparative analysis between attrited vs. existing customers
**Limitations**: The dataset lacks variables like customer acquisition cost, customer service interactions, customer satisfaction scores, complaint history or detailed product usage patterns, which could further explain churn behaviour.
**Alternative approaches**: Machine learning models could be used for churn prediction, but this exploratory analysis focused on hypothesis validation through visualisation.
**Use of AI tools**: ChatGPT, and CoPilot was used for Power BI guidance, dashboard design best practices, and README formatting.

## Ethical considerations
* The dataset was anonymised and did not contain personal identifiers.
* We respected ethical AI usage guidelines and acknowledged tools used.


## Development Roadmap
**Challenges faced**:
* Activating and using a virtual environment in VS Code. We weren't sure how to do this.
* Installing and managing required libraries. We assumed these would already be installed.
* Power BI rendering issues on certain visuals
* Plotly errors related to rendering in Jupyter.
* Merging different working styles within a group setting.
* Git branching confusion early on.
* Validity of 0s in the dataset pose a major challenge in statistical calculations.
**Overcoming them**:
* We restarted kernels and updated environment settings.
* Regular sync meetings to track task completion.
* Use of GitHub project board for accountability.
* Using ChatGPT and Copilot to fill skill gaps.
* Communicating with team mates to help with issues.

**Next steps**:
* Including more data within the visualisations.
* Explore more advanced modelling.
* Connect dashboard to live data streams.
* Include time-series analysis for customer tenure.
* Discuss the validity of 0 values in the variables (for e.g., Total_Revolving_Balance).


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
  - 
**Due to limitations with the version of PowerBI being used, a link cannot be provided, however, a file is available in Dashboards folder labelled Hackathon credit card churn**

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
