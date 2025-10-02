# Adtype_Effectiveness_analysis
Python code for evaluating ROI and effectiveness of ad types in media
A comprehensive Python-based solution for analyzing and modeling the effectiveness of different advertising types on sales performance. This tool helps marketers and data analysts understand advertising ROI, contribution, and impact using advanced statistical modeling techniques.

Adstock Transformation: Captures lagged effects of advertising spend
Comprehensive Analysis:

Linear regression modeling
Contribution analysis by ad type
ROI (Return on Investment) calculation
Statistical significance testing
Multicollinearity detection (VIF)

Prerequisites

Python 3.7 or higher
Jupyter Notebook or JupyterLab

Required Data Format
Your data file should contain the following columns:
Date, week id, sales, ad type 1 spend, ad type 2 spend , ad type 3 spend etc
See sample data attached

 Usage

Open the Jupyter Notebook file in your browser
Run each cell sequentially (Cell 1 through Cell 7)
When prompted, select your data file using the file dialog
Review the analysis results and visualizations

Adstock Transformation
The analysis applies an adstock transformation to capture the lagged effects of advertising:
adstock(t) = spend(t) + decay_rate × adstock(t-1)
Default decay rate: 0.5 (adjustable)
This accounts for the fact that advertising effects don't disappear immediately but decay over time.

Adjusting Adstock Decay Rate
In Cell 5, modify the decay_rate parameter:
pythondecay_rate = 0.5  # Change this value (0 to 1)

Higher values (0.7-0.9): Longer-lasting ad effects
Lower values (0.2-0.4): Shorter-lasting ad effects

Best Practices

Data Quality: Ensure your data has at least 20-30 observations for reliable results
Date Ordering: Data should be in chronological order
Outlier Detection: Review unusual data points before analysis
Domain Knowledge: Interpret results in the context of your business
Regular Updates: Re-run analysis as new data becomes available
