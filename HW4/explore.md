How big is the dataset?
-  36860 lines (36859 with no header), 670166 words, 4870970 characters 
- command: wc clean_dialog.csv  
What’s the structure of the data? (i.e., what are the field and what are values in them)
- there are 4 fields: "title","writer","pony","dialog"
- command: head -n 1 clean_dialog.csv 
How many episodes does it cover?
- There are 196 episodes covered 
- command: cut -d',' -f1 clean_dialog.csv | tail -n +2 | sort -u | wc -l
During the exploration phase, find at least one aspect of the dataset that is unexpected – meaning that it seems like it could create issues for later analysis.
- There could either be duplicate episodes, or if you, for example, want to search for episodes about "Twilight Sparkle", grep would not always be safe because her name could be mentioned in dialouge or other places. This is why we search field by field, not over everything. 
