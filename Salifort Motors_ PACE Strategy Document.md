**Course Seven**

# **Google Advanced Data Analytics Capstone**

![][image1]

# **Instructions** 

Use this PACE strategy document to record your decisions and reflections as a data professional as you work through the capstone project. As a reminder, this document is a resource guide that you can reference in the future and a space to help guide your responses and reflections posed at various points throughout the project. 

# **Portfolio Project Recap**

Many of the goals you accomplished in your individual course portfolio projects are incorporated into the Advanced Data Analytics capstone project including:

* Create a project proposal  
* Demonstrate understanding of the form and function of Python  
* Show how data professionals leverage Python to load, explore, extract, and organize information through custom functions  
* Demonstrate understanding of how to organize and analyze a dataset to find the “story”   
* Create a Jupyter notebook for exploratory data analysis (EDA)  
* Create visualization(s) using Tableau  
* Use Python to compute descriptive statistics and conduct a hypothesis test  
* Build a multiple linear regression model with ANOVA testing  
* Evaluate the model   
* Demonstrate the ability to use a notebook environment to create a series of machine learning models on a dataset to solve a problem  
* Articulate findings in an executive summary for external stakeholders 

**Project proposal**

# **Salifort Motors: Increase in Employee Retention and Satisfaction**

## **Overview**

 *Analyze Employee Survey responses and create a model that can help predict whether an employee will leave the company based on the employee survey data .* 

---

| Milestones | Tasks | PACE stages |
| :---: | ----- | ----- |
| **1 Week**  | Gather as much data as possible pertaining employees and relevant information Conduct Preliminary analysis of gathered data to begin brainstorming approach to the business problem (Employee Satisfaction and Retention)  Prep Data for EDA  | **Plan** |
| **1-2 Weeks**  | **Perform Exploratory Data analysis by addressing missing values, duplicates, incorrect data types and potentially doing some feature engineering.  Gather Basic Statistical Data to help understand raw data and lead to pattern discoveries.  Create Basic Visuals to present to Stakeholders  Meet with Stakeholders to share findings**  | **Analyze** |
| **1 Week**  | **Reflect on Preliminary Analysis  Discuss Potential Model/s  Prepare data for model creation and rollout**  | **Plan** |
| **2-3 Weeks** | **Choose and proceed with creating initial model/s Document findings  Create Stakeholder Summary**  | **Construct** |
| **1-2 Weeks** | **Refine Model as needed by stakeholders  Document New Findings  Create Stakeholder Summary**  | **Construct 2.0** |
| **1-2  Months** | **Stakeholders and Company Roll out Model**  | **Execute** |
|  |  |  |

[image1]: <data:image/png;base64,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>