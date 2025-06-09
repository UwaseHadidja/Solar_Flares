## Solar Flare Reporting Enhancement Project
## Overview

This project supports a space weather startup that aims to enhance how solar flare data is collected, analyzed, and reported—outperforming competitors like SpaceWeatherLive.com. We scraped, processed, and analyzed data from multiple sources to produce clear, data-driven insights about the top 50 most powerful solar flares, including associated coronal mass ejections (CMEs).

## Objectives
Scrape and clean data from NASA and SpaceWeatherLive.com

Perform entity resolution to match flare events across datasets

Analyze the relationship between flares, CME width, and halo status

Improve how hazardous space weather events are identified and reported

Solar_Flares/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── docs/
│ └── ... documentation files
│
├── data/
│ ├── raw/
│ ├── processed/
│ └── README.md
│
└── notebooks
└── ... Jupyter notebooks


## Methods
Data Preparation
Used Python libraries (pandas, BeautifulSoup, re) to scrape and clean HTML data from both NASA and SpaceWeatherLive.

Parsed flare strength (e.g., X28.0), date, time, CME speed, width, and halo status.

Normalized flare classes (M → value/10, X → value as-is).

Entity Resolution
flare_similarity(e1, e2): Computes how similar two flare records are.

flare_match(E1, E2): Matches each of the top 50 flares to its closest NASA counterpart.

Best match score achieved: 0.747

## Key Findings
1. CME Width Over Time
A line chart revealed that CME width fluctuates over the years, with spikes during active solar cycles.

Wider CMEs are linked with stronger and more hazardous flares.

2. Halo CMEs in Top Flares
A bar chart showed that a higher proportion of Halo CMEs is found in the top 50 flares compared to the rest.

Halo CMEs are significant because they are more Earth-directed and dangerous.

3. Flare Class Insights
The top 50 flares are dominated by X-class events, indicating extreme intensity.

These events often align with faster and wider CMEs, increasing their risk level.

## Recommendations
Based on the charts and analysis:

Prioritize Reporting on Halo CMEs
Halo CMEs are more likely to impact Earth and are strongly associated with top solar flares. Highlighting them can improve public preparedness.

Include CME Width in Public Reports
The average width of CMEs correlates with flare intensity. Adding this metric helps stakeholders assess severity quickly.

##Conclusion
This project shows that the most hazardous solar flares are often associated with wider, faster CMEs and are more likely to be Halo CMEs. A space weather startup can use these insights to create a smarter, more informative solar flare reporting platform, helping the public and industries respond faster to space weather threats.
