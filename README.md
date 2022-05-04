# Threshold Simulator


## User Story 

#### Who? Persona Strengths  

Cash-Based-Intervention Focal points in Operations

#### What? Goal: what they need to do?  

Make an informed decision on what weights and scoring threshold identifies the most vulnerable profiles within budget constraints. 

#### Why? Context: In which kind of situation?  

Visualize how different household profiles affect vulnerability scores, which then impact eligibility 

#### Frustration: what prevents doing their work​

Currently...  Lack of methodology/tool to visualize impact of different thresholds (and weights) in the beneficiaries list. 

#### Motivation: benefit – expected user gain – 

Ideally...The tool will show scores for the three components, and a final composite score. With option to modify cutoff threshold to see the impact in number of eligible profiles. ​
Ability to modify the weights of the three components in the final score and see the impact in eligible profiles. ​

Ability to visualize scores based on specific profiles : age, gender, household size, specific needs and coping mechanisms, geographic zone. 


## Specification and technical requirement 

    Stage 1: Develop a Static Notebook with parameters using key functions

    Stage2: validate with users the static version

    Stage 3: Develop a Dynamic dashboard with ability for users to change parameters

###   1. Input data:

 Upload Assessment dataset on the App...

###  2. User input: (dynamic control from CBI officer...)

*   Confirm the variable name for the 3 dimensions

*   Select key variables for visualizations (choose multiple from existing variable in data)

*  Set up and Select as per usage scenario:

   *  Scenario 1: Sliders with weights for each dimensions to aggregate in one unique score – then threshold

   *   Scenario 2: Sliders with eligibility and prioritization thresholds for each of the 3 dimensions

###   3. Output viz to facilitate iteration based on user input: 

*   Display key variable to display as faceted charts – prioritized vs not_prioritized 

*   Key metrics – Total # prioritized -  # eligible 

###  4. Data extract at the end of the research iteration: 

*  All original data with additional column - "Not eligible", "Eligible", "Prioritized" (plus composite unique score in case of usage scenario 1)​

*   Additional worksheet with metadata on user input decision

## Main Functions

    `write_prioritisation_decision()` -> this will write the user input (metadata) in a selected object​

    `calculate_prioritisation()` -> create a new `prioritisation` variable based on the metadata​

    `show_profiles()` -> ggplot2 facet chart based on the list of defined variable to visualise faceted based on `prioritisation` variable
