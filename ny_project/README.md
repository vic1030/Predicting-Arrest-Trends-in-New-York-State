# Predicting Arrest Trends in New York State  
### Analyzing Socioeconomic, Economic, and Housing Factors (2015-2022)  

## Project Overview  
This project aims to predict county-level adult arrest counts in New York State by analyzing social, economic, and housing characteristics. We developed and evaluated machine learning models to understand the influence of these factors on crime rates and provide actionable insights for policymakers.

## Objectives  
1. Identify which socioeconomic and housing factors are most strongly associated with arrest counts.  
2. Develop predictive models to estimate total arrest counts and understand temporal and spatial trends.  

## Project Deliverables  
- **Final Report:** [View the full report](docs/report.pdf)  
- **Model Card:** [View the model card](docs/model_card.pdf)  
- **Deployed Model API:** [http://appliedml.infosci.cornell.edu:2568/__docs__/](http://appliedml.infosci.cornell.edu:2568/__docs__/)  
- **Code Repository:** All code for data processing, exploratory data analysis (EDA), feature engineering, and model training is stored in this repository.

## Data  
The analysis-ready dataset integrates arrest counts with social, economic, and housing indicators for counties in New York State from 2015 to 2022. It includes:  
- **Arrest Data:** Total arrests, felony/misdemeanor types.  
- **Economic Data:** Unemployment rates, median household income, poverty levels, health insurance.  
- **Social Data:** Education levels, disability status, veterans, and language barriers.  
- **Housing Data:** Total housing units, mortgage ratios.

## Data Sources
- **Arrest Data:**: https://data.ny.gov/Public-Safety/Adult-Arrests-18-and-Older-by-County-Beginning-197/rikd-mt35/about_data
- **Economic, sococial & housing Data:** https://data.census.gov/profile/New_York?g=040XX00US36

## Model Selection  
The **Poisson Regression model with `factor(Year)`** outperformed the other models that we tested, as it effectively captured year-specific trends and delivering higher predictive accuracy.

## File Structure
```plaintext
project-skillful-wombat/
│
├── data/                    
│   └── merged_data.csv          # Cleaned data
│
├── docs/                    
│   ├── report.pdf               # Rendered main report
│   ├── model-card.pdf           # Rendered model card
│   └── best-model.pdf           # Rendered best model file
│
├── archive-code/            
│   ├── proposal.qmd             # Initial Proposal
│   ├── explore.qmd              # Initial EDA process
│   └── presentation.qmd         # Presentation template
│
├── renv/                    
│   └── activate.R               # R environment management
│
├── README.md                    # Main project documentation
├── report.qmd                   # Main project script
├── best-model.qmd               # Model selection & publishing script
├── model-card.qmd               # Model card script
│
├── Dockerfile                   # Docker configuration for API
├── service-auth.json            # (Ignored) Google Cloud credentials
├── .gitignore                   # Ignore sensitive and unnecessary files
├── .renviron                    # Environment file
├── .Rprofile                    # Project-specific options
├── _quarto.yml                  # Quarto configuration
└── project.Rproj                # RStudio project file
```

## Reproducibility  
To reproduce the analysis:  
1. Clone this repository.  
2. Run the scripts `report.qmd`, `best-model.qmd`, `model-card.qmd` sequentially.  
3. Use the provided `merged_data.csv` for model training.  

## Authors  
- **Joyce Yan**  
- **Lydia Lin**  
- **Victoria Xiao**  
 

