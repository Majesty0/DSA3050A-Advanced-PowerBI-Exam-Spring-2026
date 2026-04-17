<img width="975" height="55" alt="image" src="https://github.com/user-attachments/assets/6c06182f-e0fe-4d8e-b787-a55bb4d6c8aa" />
Explanation
> Counts the number of unique countries present in the current filter context. This is a distinct count measure.
Decision making value:
> Useful when filtering by date or price category – shows how many countries are contributing to the aggregated numbers. For example, “How many countries experienced Very High energy prices in 2023?”

<img width="808" height="61" alt="image" src="https://github.com/user-attachments/assets/38e089d5-10c2-4826-a141-4a9f351735b2" />
*Explanation:*
> Sums the co2_emission column across all selected rows. This is a total value measure.
**Decision making value:**
> Provides the baseline carbon footprint. Policy makers can monitor whether total emissions are increasing or decreasing over time.

<img width="975" height="57" alt="image" src="https://github.com/user-attachments/assets/1fb41dc6-97f1-4533-82ac-c5b910fa7be4" />
**Explanation:**
> Calculates the arithmetic mean of daily energy consumption. This is an average metric.
**Decision making value:**
> Helps identify typical energy demand. Unusual spikes or drops can trigger investigations into industrial activity or weather events.

 <img width="873" height="142" alt="image" src="https://github.com/user-attachments/assets/f9f13aa3-f12d-4b86-b845-d8b73d59ca8a" />
**Explanation:**
> Calculates renewable energy as a percentage of total energy consumption. This is a percentage contribution measure.
**Decision making value:**
> Tracks the green energy transition. A rising percentage indicates successful decarbonization policies. Can be compared across countries or over time

 <img width="900" height="128" alt="image" src="https://github.com/user-attachments/assets/1c5cd4d2-52a0-4391-8b87-05b1672be664" />
**Explanation:**
> Computes cumulative CO₂ emissions from the start of the year to the current date in the filter context. This is a year to date calculation.
**Decision making value:**
> Allows monitoring of annual progress against emission reduction targets. For example, compare YTD emissions to the same period last year.

 <img width="975" height="128" alt="image" src="https://github.com/user-attachments/assets/1a429a47-d3fa-4703-8a75-2bf2cf5112ec" />
**Explanation:**
> Computes the percentage change in total CO₂ emissions compared to the same date range in the previous year. This is a growth over time measure.
**Decision making value:**
> Positive growth indicates worsening emissions; negative growth indicates improvement. Essential for evaluating the effectiveness of environmental policies.

<img width="947" height="161" alt="image" src="https://github.com/user-attachments/assets/78d31b12-5865-4e98-bf58-4b5fa26cdb6e" />
**Explanation:**
> Ranks countries from highest to lowest based on total CO₂ emissions. This is a ranking measure.
**Decision making value:**
> Identifies top polluters and low emitters at a glance. Helps prioritise which countries need the most urgent intervention or funding for clean energy.

 <img width="975" height="402" alt="image" src="https://github.com/user-attachments/assets/fe6cf2d2-6c7a-43d6-8c7a-3c6892f2cd36" />
**Explanation:**
> Compares average energy consumption during “High” price periods versus “Normal” price periods, showing the percentage change. This uses conditional logic (implicitly via CALCULATE with filters) and variance between two categories.
**Decision making value:**
> Quantifies how sensitive energy demand is to price spikes. A large negative impact suggests consumers reduce usage when prices rise – useful for demand side management and pricing strategy.

 <img width="975" height="381" alt="image" src="https://github.com/user-attachments/assets/96da28b3-85a8-40fe-bb08-44fa8845ea83" />
**Explanation:**
> Computes the percentage change in average energy consumption from the previous month to the current month. This is a growth/change over time measure at monthly granularity.
**Decision making value:**
> Identifies short term fluctuations in energy demand. A sudden increase might indicate unusual weather or industrial activity; a decrease could signal conservation efforts or economic slowdown.

<img width="805" height="184" alt="image" src="https://github.com/user-attachments/assets/55444431-81b8-4cfa-93f1-27d80371564c" />
**Explanation:**
> Calculates how much CO₂ is emitted per unit of energy consumed. Lower values indicate cleaner energy mix. This is a ratio / efficiency metric.
**Decision making value:**
> Tracks decarbonization progress independent of total energy use. A declining intensity means the economy is becoming cleaner even if total energy consumption rises.
 
 <img width="975" height="290" alt="image" src="https://github.com/user-attachments/assets/cfc76a88-8f57-4dff-8ee9-9e2aa125ee09" />
**Explanation:**
> Returns a comma separated string of the top 3 countries with the highest average renewable energy share. This uses ranking and concatenation.
**Decision making value:**
> Provides an at a glance recognition of leaders in renewable adoption. Useful for benchmarking and for dashboards where a dynamic text label is more space efficient than a bar chart.
 
> [!Note]
> Energy Alert Flag Requires a supporting measure for same period last year:
> Then Energy Alert Flag uses conditional logic (IF) to flag abnormal consumption.

<img width="878" height="279" alt="image" src="https://github.com/user-attachments/assets/8935c70a-00ca-4712-9d19-0d5a28a149e2" />
Explanation
> Compares current average energy consumption to the same period last year. If current consumption is more than 10% above last year, shows “Warning”; more than 20% shows “Critical”.
> Decision making value:
> Automatically alerts stakeholders to unusual spikes in energy use, prompting investigation into causes (e.g., extreme weather, equipment failure, policy changes)



