# <p align="center">🛣️ REDUCING THE NUMBER OF ROAD FATALITY ACCIDENTS 🚘</p> 

## 📖 Background
We work for the road safety team within the department of transport, and they are looking into how they can reduce the number of major incidents. 

The safety team classes major incidents as fatal accidents involving 3+ casualties. They are trying to learn more about the characteristics of these major incidents so they can brainstorm interventions that could lower the number of deaths. 

They have asked for our assistance with answering a number of questions.


## 📌 Problem Statement

Our goal for this project is to create a report that covers the following:

1. What time of day and day of the week do most major incidents happen?
2. Are there any patterns in the time of day/ day of the week when major incidents occur?
3. What characteristics stand out in major incidents compared with other accidents?
4. On what areas would you recommend the planning team focus their brainstorming efforts to reduce major incidents?

Through data cleaning, analysis and visualization we will answer these questions in order to help our stakeholder to increase road safety by understanding when and how fatal accidents tend to happen and, consequently, take actions to prevent them and save lives.

This project was inspired by a [DataCamp Competition](https://www.datacamp.com).

## 💾 Data Understanding

### Code Used:

* Python Version : 3.9
* Packages : Pandas, Numpy, Matplotlib, Seaborn, Plotly

### Importing Dataset:

The reporting department have been collecting data on every accident that is reported. We have two sources of information available:
* A dataset containing data on every accident that is reported;
* A lookup file for 2020's accidents.

*Published by the department for transport. https://data.gov.uk/dataset/road-accidents-safety-data* 
*Contains public sector information licensed under the Open Government Licence v3.0.*

<!-- ### Data Dictionary


Variable | Definition
------------ | -------------
 |  accident_index                            | 
 |  accident_year                             |
 |  accident_reference                        |
 |  longitude                                 |
 |  latitude                                  |
 |  accident_severity                         |
 |  number_of_vehicles                        |
 |  number_of_casualties                      |
 |  date                                      |
 |  day_of_week                               |
 |  time                                      |
 |  first_road_class                          |
 |  first_road_number                         |
 |  road_type                                 |
 |  speed_limit                               |
 |  junction_detail                           |
 |  junction_control                          |
 |  second_road_class                         |
 |  second_road_number                        |
 |  pedestrian_crossing_human_control         |
 |  pedestrian_crossing_physical_facilities   |
 |  light_conditions                          |
 |  weather_conditions                        |
 |  road_surface_conditions                   |
 |  special_conditions_at_site                |
 |  carriageway_hazards                       |
 |  urban_or_rural_area                       | -->
