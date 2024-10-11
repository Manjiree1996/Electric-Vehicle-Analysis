# Electric-Vehicle-Analysis
# Problem Statement
This dashboard helps as to understand overall landscape of electric vehicles to providing insights into market size, growth pattern and Adoption trends over the year.
It also helps us to determine average electric range of electric vehicles. Also shows number of Battery electric vehicle and Plug-in-hybrid electric vehicles
& percentage of both providing insights into dominance of fully electric & plug-in-hybrid models & it also let them know the geographical distribution of vehicle 
across different states for identifying adoption rate.
# KPI's Requirment
1. Total Vehicles
2. Avearge Electric Range
3. Total BEV Vehicle & % of Total BEV Vehicles
4. Total PHEV Vehicles & % of Total PHEV Vehicles
# Chart Requirement
1. Total Vehicles by Model Year (From 2010 onwards)
2. Total Vehicles by State
3. Top 10 Vehicles by Make
4. Total Vehicles by CAFV Eligibility
5. Top 10 Vehicles by Model
# DAX Query Used
1. Total Vehicle = DISTINCTCOUNT (Electric_Vehicle_Population_Data [DOL Vehicle ID])
2. Average Electric Range = CONCATENATE (FORMAT (AVERAGE (Electric_Vehicle_Population_Data[Electric Range],"0.00","Km")
3. BEV Vehicles = CALCULATE([Total Vehicles], Electric_Vehicle_Population_Data[Electric Vehicle Type] ="Battery Electric Vehicle (BEV)")
4. % of BEV Vehicles = [BEV Vehicles] / [Total Vehicles]
5. PHEV Vehicles = CALCULATE([Total Vehicles], Electric_Vehicle_Population_Data[Electric Vehicle Type] ="Plug-in-Hybrid Electric Vehicle (PHEV)")
6. % of PHEV Vehicles = [PHEV Vehicles] / [Total Vehicles]

