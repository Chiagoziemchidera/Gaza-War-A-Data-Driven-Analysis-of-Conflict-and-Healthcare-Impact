# Gaza_War_Incident_Analysis

![20231104_MAP005](https://github.com/user-attachments/assets/eeb65953-7db1-4f84-b233-7f0c31806b4a)


The Gaza War refers to the ongoing conflict between Israel and Hamas, the militant group that governs the Gaza Strip. The most recent escalation began on October 7, 2023, when Hamas launched a surprise attack on southern Israel, killing over 1,200 people and taking hostages. In response, Israel declared war on Hamas, launching a massive military operation involving airstrikes and a ground invasion aimed at dismantling Hamas' infrastructure.

The war has caused widespread destruction and a severe humanitarian crisis in Gaza, with tens of thousands of Palestinian casualties, mass displacement, and limited access to food, water, and medical aid. The conflict has drawn global attention, sparking debates over human rights, civilian protection, and regional stability, while diplomatic efforts for a ceasefire continue.

---

## Project Overview
This project is a deep dive into the human cost of war, using data to tell the story behind the numbers. I’ll be analyzing incident-level data from the Gaza War to understand how conflict affects lives—not just through direct attacks, but also through the collapse of healthcare systems and infrastructure.

The goal is to uncover patterns in fatalities, injuries, and causes of death, and to see which regions and types of incidents are the most devastating. Through this, I hope to highlight the broader impact of war and use data to support conversations around humanitarian response and long-term recovery.


## Dataset Description

- **Total Columns:** 7  
- **Number of rows:** 403 

###  Column Headers:

| Column Name       | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| `Death ID`        | Unique identifier for each recorded fatality.                               |
| `City`           | City or location where the incident occurred (e.g., Gaza City).             |
| `Incident_Type`   | Type of attack or event (e.g., Drone Strike, Missile Strike, Airstrike).    |
| `Fatalities`      | Number of deaths reported in the incident.                                  |
| `Injuries`        | Number of injuries reported in the same incident.                           |
| `Category`        | Indicates whether the death was caused by **Direct Conflict** or otherwise. |
| `Cause_of_death`   | Specific medical or trauma-related reason for the fatality (e.g., Traumatic Brain Injury). |

This dataset captures the types, locations, and outcomes of various conflict-related incidents.


## Problem Statement

When we think about war, we often focus on the immediate damage—airstrikes, explosions, and direct casualties. But what’s often missed is the silent toll it takes: people dying from preventable causes because hospitals are destroyed, supplies are cut off, or help just can’t reach them in time.

This project was born out of a need to understand that bigger picture. By analyzing conflict incident data, I want to uncover not just how many lives were lost but why—and how many of those deaths could have been avoided with better access to medical care. It’s a way to use data to shine a light on the human side of war that often gets overlooked.

## Data Cleaning Summary

The dataset appears to be generally clean and well-structured, but here are key observations and minor recommendations:

### Clean Aspects
- No Missing Values in the following columns (`Death ID`, `Incident_Type`, `Fatalities`, `Injuries`, `Category`, `Cause_of_death`).
- `City` had some missing values, which were named "Unknown". These rows couldn't be deleted because that entry is necessary to get a proper view of the implications of the war.
- **Appropriate Data Types:** 
  - Numeric columns like `Fatalities` and `Injuries` are correctly typed as integers.
  - Categorical/text columns are stored as text types.

 - **The DAX formula used on the Power BI report can be seen in [DAX Formula](https://github.com/Chiagoziemchidera/Gaza-War-A-Data-Driven-Analysis-of-Conflict-and-Healthcare-Impact/blob/main/DAX%20Formula)

## Analysis Insights

<img width="524" alt="WAr analysis" src="https://github.com/user-attachments/assets/2731eda0-2164-4607-80ff-ee1566bf55fb" />


## High Fatality Rate  
- **Total fatalities:** 2,405,879 across **403 recorded incidents**, indicating an extremely high fatality-to-incident ratio.  
- **Total injuries:** 303,179, meaning a significant portion of incidents result in death rather than injury.

## Leading Causes of Death  
- **Sepsis (833,733 cases)** and **asphyxiation (613,773 cases)** are major causes of death, likely due to inadequate medical access.  
- Fatalities from direct conflict include **hemorrhagic shock (592,746 cases)** and **traumatic brain injuries (317,642 cases)**, showing the violent nature of incidents.  
- **85.31% of deaths are due to lack of medical access**, while **only 14.69% are from direct conflict**, suggesting indirect consequences of war are deadlier than the immediate violence itself.

## Most Deadly Incident Types  
- **Airstrikes (879,578 deaths)** are the deadliest incident type, followed by **building collapses (558,455 deaths)** and **missile strikes (330,183 deaths)**.  
- Despite being less frequent, **rocket attacks (200,431 deaths) and drone strikes (132,148 deaths)** still contribute significantly to the total death toll.

## Injuries vs. Fatalities by Incident Type  
- **Building collapses lead to the highest number of injuries (129,789),** suggesting many victims survive but suffer severe wounds.  
- **Missile strikes (81,878 injuries) and artillery shelling (60,787 injuries)** also result in substantial injuries.  
- **Airstrikes, while extremely deadly, cause fewer injuries (only 13,191 recorded),** meaning they are more lethal on impact.

## Cities with the Most Fatalities  
- **Haiti (795,794 deaths) and Gaza City (713,121 deaths)** have suffered the highest number of fatalities, indicating they are primary conflict zones.  
- **Other highly affected areas include Deir al-Balah (337,880 deaths) and North Gaza (271,817 deaths).**  
- Some fatalities are also recorded in **Guinea (7,693), Ethiopia (2,532), and other regions**, though at significantly lower levels.

## Percentage of Fatalities vs. Injuries by Incident Type  
- **Airstrikes have an overwhelming 98.52% fatality rate**, making them the most lethal form of attack.  
- **Drone strikes (98.25%) and rocket attacks (92.96%)** also have extremely high fatality rates, meaning survival chances in these incidents are minimal.  
- **Building collapses and artillery shelling have slightly lower fatality percentages (81.14% and 83.39%, respectively),** suggesting they result in more injuries compared to direct attacks.

## Final Thoughts  
The data paints a grim picture of the human toll of war. **Airstrikes, missile strikes, and rocket attacks account for most deaths, with lack of medical access being a silent killer.** Cities like **Haiti and Gaza City** are the hardest hit, and survival chances in airstrikes and drone attacks are alarmingly low. The numbers highlight the devastating impact of modern warfare on both civilians and infrastructure.
