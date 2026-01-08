## Understanding Which Top Elements Drive Most of the Change

In many business scenarios, changes in key metrics—like take rate, conversion rate, or delivery performance—are often driven by a small number of top contributors. Identifying these quickly helps teams take focused action and allocate resources efficiently. 



This [Google Sheet](https://docs.google.com/spreadsheets/d/1G_sw5Ruy48p7ergXjlkpAUBTfGEFktEG5nr3h6JQqxI/edit?usp=sharing) template simplifies that process for both analytics and business team. 

It automatically calculates the **contribution to variance (CTV)** and highlights their **concentration** by Pareto principle.





A Sample Pareto Chart of CTV



### Example: Analyzing a Percentage Metric

We shows the template with percentage metric, and it’s easy to adapt into an absolute metric version.

Suppose an e-commerce platform notices that the ads fee take rate is rising in a trending Category A. The question is:





* Is this increase driven by just a few top sellers of category A?

If the answer is yes, the account manager can intervene with targeted promotions to further boost sales, focusing effort where it will have the most impact.

(* This example’s data is simulated by LLM and does not contain or represent any real-world data.)



## How the Template Works

The google sheet template has three tabs:

### Step 1: Load Raw Data





Tab “raw_data”

Paste the raw data starting at cell B2:





* Include a **date column** for comparison and **numerator / denominator** for your metric (e.g., Ads Spend / GMV by seller).



* Column A (already set up) helps align comparison windows for analysis.

### Step 2: Contribution Calculator





Tab “calculation”

In the top lines of “Calculation” tab, configure:





* Date window (e.g. pre-period: March–April, post-period: July



* **Dimension** (e.g. seller_id)



* **Metric Numerator / Denominator** (e.g. Ads Fee / GMV)



* **Metric name** (e.g. enter “Take Rate” in cell H3)



The template then calculates contributions automatically using pre-set functions.



### Step 3: Visualize Concentration by 80/20 Principle





Tab “Chart & Output”

We are all familiar with the **Pareto Principle (80/20 Principle)**, which suggests that a small share of factors often explains the majority of the outcome.



In the output tab, we have a Pareto chart of Contribution to Variance (CTV):





* **Blue Bars** (left axis): shows the contribution of each seller.



* **Orange Line** (right axis): the **cumulative contribution percentage** (capped at 100%).



* **Threshold** in cell F1 can be adjusted (e.g., 70–80%) to decide how much of the variance should focus on.



Below the chart, 3 KPI boxes summarize key results: In this example, 
just **9 /150 sellers contributed 72% of the total variance, while covering only 30% of overall GMV.**



On the right-hand side, a ranked list shows contribution percentage in descending order. 
Conditional formatting highlights the top contributors so the team can quickly see who and where to focus action.





There is another chart showing the Coverage of Contribution %, which helps validate the Pareto Principle. 
Ideally, **when the concentration is high, we expect to see a tall, narrow gray rectangle on the left side.**



## How It Helps





* **Saves time on analysis** – reduces the need for manual pivot tables, formulas, and formatting by a reusable template.



* **Turns data into action** – identifies key drivers so business teams can focus resources where they matter most.





Thanks for reading!

