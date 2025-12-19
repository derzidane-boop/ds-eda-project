[![Shipping files](https://github.com/neuefische/ds-eda-project-template/actions/workflows/workflow-03.yml/badge.svg?branch=main&event=workflow_dispatch)](https://github.com/neuefische/ds-eda-project-template/actions/workflows/workflow-03.yml)
# ds-project-template

Template for creating ds simple projects

## Requirements

- pyenv
- python==3.11.3

## Setup

One of the first steps when starting any data science project is to create a virtual environment. For this project you have to create this environment from scratch yourself. However, you should be already familiar with the commands you will need to do so. The general workflow consists of... 

* setting the python version locally to 3.11.3
* creating a virtual environment using the `venv` module
* activating your newly created environment 
* upgrading `pip` (This step is not absolutely necessary, but will save you trouble when installing some packages.)
* installing the required packages via `pip`

*Note: We do have the `requirements.txt` in the repository but please try to first install packages by yourself.*

At the end, you want to make sure that people who are interested in your project can create an identical environment on their own computer in order to be able to run your code without running into errors. Therefore you can create a `requirements file` and add it to your repository. You can create such a file by running the following command: 

```bash
pip freeze > requirements.txt
```

*Note: In rare case such a requirements file created with `pip freeze` might not ensure that another (especially M1 chip) user can install and execute it properly. This can happen if libraries need to be compiled (e.g. SciPy). Then it also depends on environment variables and the actual system libraries.*


--- 
## In-Case of Failure
If you fail to do the setup by yourself, then please revisit the previous repositories where you have done the setup and follow those steps.


# King County Housing – Exploratory Data Analysis

## Project Overview
This project performs an exploratory data analysis (EDA) on housing data from
King County, USA. The goal is to understand key factors influencing house
prices and to provide data-driven recommendations for a selected client.

## Data Source
The data originates from a PostgreSQL database and consists of two tables:
house details and house sales. The tables were joined using a LEFT JOIN and
exported locally as a CSV file. The dataset is intentionally excluded from
version control as required by the assignment.

## Methodology
The analysis follows a structured EDA workflow:
1. Data understanding and cleaning
2. Formulation of research questions and hypotheses
3. Distribution analysis
4. Relationship and correlation analysis
5. Client-focused recommendations

## Client Focus
The selected client is **Jennifer Montgomery**, a high-budget buyer interested
in waterfront properties with strong resale potential within one year.

## Key Findings
- House prices are strongly influenced by living area, construction grade,
  and waterfront access.
- Waterfront properties show significantly higher prices.
- Recently renovated, high-grade houses in top neighborhoods offer the best
  short-term resale potential.

## Presentation
A high-level presentation summarizing the methodology and recommendations for
non-technical stakeholders is provided in the `slides/` folder as a PDF.

## Requirements
- Python 3
- pandas
- matplotlib
- seaborn
