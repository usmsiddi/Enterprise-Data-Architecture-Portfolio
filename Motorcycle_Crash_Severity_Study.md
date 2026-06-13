                                                    UNC Department of Data Science — Advanced Analytics Review	1
 
Understanding Motorcycle Crash Severity Through Behavior and Conditions 

Usman Siddiqui, University of North Carolina 

 
  
Abstract—This project explores what really makes motorcycle crashes deadly. The common idea that motorcycles are 30 percent more fatal than cars is repeated everywhere, but nobody explains why that number exists or what drives it. I used California SWITRS crash data and national helmet statistics from NHTSA to study how lighting, alcohol involvement, and the day of the week relate to injury severity. I created a series of visualizations that show how certain behaviors and conditions change the outcome of a crash. The results suggest that a lot of the danger comes from choices and context, not the motorcycle itself 
I. INTRODUCTION 
When I started riding motorcycles, I kept seeing the same message. Motorcycles are 30 percent more fatal than cars. But the message never went deeper than that. It bothered me because I wanted to know if the danger came from the machine or from the way people ride and the conditions they choose to ride in. That question motivated this project. 
 
To explore this, I focused on three factors that are known to change crash severity. I looked at lighting conditions because visibility matters. I looked at alcohol involvement because behavior affects reaction time and decisions. And I looked at the day of the week because riding patterns change a lot on weekends. These factors let me ask a simple question. Are motorcycles deadly on their own or is the risk created by what people do on the bike and when they choose to ride. 
 
I used SWITRS because it provides detailed police reported crash records for California. It includes severity, lighting, alcohol, and time factors. I also used national helmet information from NHTSA because helmet use gives extra context about behavior and risk. The goal was to build clear visuals that anyone can use to understand what makes a motorcycle crash more serious. 
 
II. Related Work 
 
Many researchers have looked at motorcycle injuries and the factors that make them worse. Studies show that helmets reduce head injuries and save lives [1, 2]. Other work shows that night time riding increases risk because visibility is low [3, 4]. Alcohol has also been linked to more severe outcomes and harder crashes [5]. National reports from NHTSA explain yearly trends in motorcycle fatalities and helmet use [6]. More technical studies model how rider behavior, speed, and surroundings shape crash severity [7]. Human factors research looks at how decision making and attention affect crash risk [8]. Overall, past work supports the idea that risk is not fixed. It moves up and down based on what the rider does and the conditions around them. 
 
III. Data and Methods 
 
3.1 Data Sources 
 
SWITRS Data (California 2018 to 2023) 
This dataset includes every police reported crash in the state. I filtered it to only motorcycle related crashes. The fields included severity, lighting, alcohol involvement, day of week, weather, and many other details. 
 
NHTSA Helmet Data (2023) 
This provided helmet usage rates and estimates of how helmets reduce fatality risk. I used it mainly as supporting information for understanding behavior. 
 
3.2 Data Cleaning 
 
Before building visuals, I cleaned the data in a few simple steps: 
 
•	filtered the records to only motorcycle crashes 
•	fixed the severity codes so they read as Fatal, Severe Injury, 
Minor Injury, and Complaint of Pain 
•	changed lighting codes A to E into full words 
•	changed the day of week numbers into day names 
•	removed empty rows and unused fields 
•	fixed data types so Tableau would not break 
 
3.3 Visualization Method 
 
I created three main visuals: 
 
•	a grouped bar chart to compare lighting conditions with crash severity 
•	a heat map to show fatal crashes across the days of the week • a lollipop chart comparing alcohol involved crashes vs not involved for each severity level 
 
All three visuals were added to a dashboard with simple filters so someone could explore the patterns on their own. 
> REPLACE THIS LINE WITH YOUR PAPER IDENTIFICATION NUMBER (DOUBLE-CLICK HERE TO EDIT) < 	2 
 
 
 
IV. Findings 
 
4.1 Lighting and Severity 
 
Daylight has more total crashes because that is when most people ride. But when you look at the percent that become fatal, night time crashes are much more severe. Fewer crashes happen at night, but the ones that do happen are more deadly. 
Low visibility seems to amplify the impact of a crash. 
 
4.2 Day of Week 
 
The heat map showed that fatal crashes rise sharply on weekends. Friday and Saturday had higher fatality concentrations. This lines up with recreational riding and also heavier alcohol use during those days. 
 
4.3 Alcohol Involvement 
 
Even though alcohol related crashes were fewer in number, their fatality percentage was much higher. This supports the idea that behavior is one of the strongest drivers of severity. The difference between sober and alcohol involved crashes was clear in the lollipop chart. 
 
V. Discussion 
 
Taken together, the charts show the same pattern. Motorcycle danger is not fixed. It changes dramatically based on visibility, day of the week, and riding behavior. Night time riding, weekend riding, and alcohol use all increase fatality rates. This means the 30 percent number that we hear everywhere is not the full story. A more complete message is that certain choices raise the risk a lot more than others. I believe this type of analysis could help instructors, insurance companies, and safety educators explain risk in a more honest and useful way. 
 
 
VI. Limitations 
 
•	the dataset only includes California 
•	helmet data was national but not tied to individual crashes 
•	not all SWITRS fields were fully complete 
•	speed, rider experience, and actual protective gear use were not included 
•	I focused on only three factors due to time 
 
VII. Conclusion 
 
This project shows that motorcycle fatality risk is not simply built into the machine. It moves up and down depending on behavior and conditions. Night time riding, alcohol involvement, and weekend patterns increase risk more than anything else I looked at. These findings support a shift away from the message that motorcycles are just deadly by default. 
Instead, the message should be that certain behaviors and  References 
 
[1]	California Highway Patrol, “Statewide Integrated Traffic Records System (SWITRS) Collision Data,” 2018–2023. 
Available: https://tims.berkeley.edu 
 
[2]	National Highway Traffic Safety Administration 
(NHTSA), “Motorcycle Helmet Use in 2023: Results from the 
National Occupant Protection Use Survey,” DOT HS 813 634, 
2024. Available: https://www.nhtsa.gov 
 
[3]	C. S. Olsen, J. C. Thomas, and J. L. Bundy, “Motorcycle helmet effectiveness in reducing head injury,” Journal of Trauma, vol. 71, no. 5, pp. 1067–1071, 2016. 
 
[4]	P. M. Sharif, M. Safarpour, and R. Mohammadi, “Factors behind improved helmet use in motorcyclists,” BMC Public Health, vol. 23, 2023. 
 
[5]	L. Song, Y. Luo, and W. Chen, “Time-of-day variations in crash injury severity,” Accident Analysis & Prevention, vol. 
159, 2021. 
 
[6]	P. Walisutwattanasak, K. Naito, and P. J. Hopke, “Analyzing factors affecting motorcycle crashes during day and night,” MDPI Safety, vol. 10, no. 1, 2024. 
 
[7]	M. H. Wang, S. H. Kuo, and H. J. Chen, “Alcohol involvement as a risk factor in motorcycle crash severity,” Injury Epidemiology, vol. 9, no. 1, 2022. 
 
[8]	R. B. Voas, J. K. Wells, A. S. Tippetts, and J. Fell, “Methodology for determining motorcycle operator crash risk,” U.S. Department of Transportation, Report DOT HS 810 812, 2007. 
 
Acknowledgment: 
I used ChatGPT to help brainstorm ideas, clarify concepts, troubleshoot Tableau steps, and revise wording in my write up. All decisions, analysis, and final interpretations are my own. 
 
<img width="519" height="157" alt="image" src="https://github.com/user-attachments/assets/6e0a55a9-9d78-4e6a-a15c-aceb189f5c61" />
