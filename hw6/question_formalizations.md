Task 1: Noise
The mayor wants to know if noise issues tend to stem from different causes across the year.

- Objective 1: Formalize the question in a way that you can actually answer. 

    Version 1: the question as posed by the stakeholder. 
        **Question (v1): Do noise issues tend to stem from different causes across the year?**

        notes:
            - 3 vague phrases: “noise issues,” “causes,” “across the year.”
            - The stakeholder = the mayor 
            - What are these noise issues? -> according to the data, there are 198 complaint types -> how many are noise complaints?
                - run cut -d',' -f6 311_only_2024.csv | grep -i "noise" | sort | uniq -c 
                - 55,522 + 68,347 + 28,686 + 1,296 + 8,279 + 379,297 + 163,002 + 48,834 = 753,263 noise complaints
                - wc -l 311_only_2024.csv gives us 3,458,321 lines in the csv => 753,263 / 3,458,321 => 22% of the complaints are noise related
                    - noise categories: "noise" (general?), "commerical", "helicopter", "house of worship", "park", "residential", "street/sidewalk", "vehicle"
            - What are the possible causes? => no cause column in csv, will use "Descriptor" column as a proxy for these causes 

    Version 2: one refinement of the question that is more measurable and maps better onto the available data. 
        **Question (v2): Do the most common types of noise complaints vary by month?** 

        notes:
            - "noise issues" → Complaint Type csv column
            - "causes" → proxy: Descriptor csv column
            - "across the year" → Created Date csv column

    Version 3: a second refinement that maps even better onto the available data. 
        **Question (v3): In 2024, how does the volume of each type of noise complaint reported change from month to month?** 
    

    Version 4: the final version of the question that is directly quantifiable and maps onto the available data. 
        - **Question(v4): For each month of 2024, what are the percentages of each type of noise complaint?**

- Objective 2:
- Objective 3:

___________________________________________________________________________________________

Task 2: Urban Rodents
The Departments of Sanitation and Health would like to know where in the city rats and mice are most likely to create sanitation issues. In discussion with them, you determine that they aren’t thinking in terms of geography, but more in terms of the kinds of buildings/properties/structures we find around a city.

- Objective 1: Formalize the question in a way that you can actually answer. 

    Version 1: the question as posed by the stakeholder. 
        **Question (v1): In the city, what types of buildings/properties/structures are rats and mice most likely to create sanitation issues in?**

    Version 2: one refinement of the question that is more measurable and maps better onto the available data. 
        **Question (v2): What kinds of buildings or properties get the most rodent complaints?** 

    Version 3: a second refinement that maps even better onto the available data. 
        **Question (v3): What types of buildings or properties got the most rodent complaints in 2024?** 

    Version 4: the final version of the question that is directly quantifiable and maps onto the available data. 
        **Question (v4): In 2024, how many rodent complaints were made at each location type documented, from greatest amount to the smallest amount?** 

- Objective 2:
- Objective 3:
