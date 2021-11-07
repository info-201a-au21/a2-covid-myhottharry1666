# A2: U.S. COVID Trends

## Overview
In many ways, we have come to understand the gravity and trends in the COVID-19 pandemic through quantitative means. Regardless of media source, people are consuming more epidemiological information than ever, primarily through reported figures, charts, and maps. 

This assignment is your opportunity to work directly with the same data used by the New York Times. While the analysis is guided through a series of questions, it is your opportunity to use programming skills to ask more detailed questions about the pandemic.

You'll load the data directly from the [New York Times GitHub page](https://github.com/nytimes/covid-19-data/), and you should make sure to read through their documentation to understand the meaning of the datasets. 

Note, this is a long assignment, meant to be completed over the two weeks when we'll be learning data wrangling skills. I strongly suggest that you **start early**, and approach it with patience. We're asking real questions of real data, and there is inherent trickiness involved. 

## Analysis
You should start this assignment by opening up your `analysis.R` script. The script will guide you through an initial analysis of the data. Throughout the script, there are prompts labeled **Reflection**. Please write 1 - 2 sentences for each of these reflections below:

- What does each row in the data represent (hint: read the [documentation](https://github.com/nytimes/covid-19-data/)!)?
    - national: Each row represents Covid-19 data of US on a specfic day.
    - states: Each row represents Covid-19 data of one state on a specfic day.
    - counties: Each row represents Covid-19 data of one county (in a state) on a specific day.
- What did you learn about the dataset when you calculated the state with the lowest cases (and what does that tell you about testing your assumptions in a dataset)?
  - This Covid cases data in this dataset may not be very accurate for every state. For example, the number of cases in American Samoa stays at 1, which is very suspicious.
  - When it comes to testing assumptions in a dataset, it might be better to drop some extreme value to make our analysis result more reasonable.
- Is the location with the highest number of cases the location with the most deaths? If not, why do you believe that may be the case? 
  - No, the location with the highest number of cases is not the location with the most deaths.
  - Possible Reasons:
    - The dataset has problem, e.g., miscount the number of cases, miscount the number of deaths.
    - There exists difference between medical facilities among different locations. Maybe the location with the highest number of cases has better treating facilities, so with more effective treatment, number of deaths at this locations gets better control.
- What do the plots of cases and deaths tell us about the  pandemic happening in "waves"? How (and why, do you think) these plots look so different?
  - The number of cases and the number of deaths increase / decrease periodically instead of linearly, so we cannot relax the distancing policy casually just because of a small decreasing tendency in cases / deaths.
  - The main difference between two plots is that the wave in deaths plot normally reaches peak later than that in cases plot. One possible reason is that when new cases appear, their sympotom will not become the worst (death) in the beginning, so this can explain the delay of time reaching peak.
- Why are there so many observations (counties) in the variable `lowest_in_each_state` (i.e., wouldn't you expect the number to be ~50)?
  - It is possible that there are some counties / locations with the same number of cases / deaths. Thus, with further conditions, those counties in the same state with the same number will be returned together.
- What surprised you the most throughout your analysis?