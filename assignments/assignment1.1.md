## ASSIGNMENT 1.1 ## 

In order to pass, you do not need to successfully complete the HARD task, but at least have tried to answer it. The purpose of the hard task is to show you a few of the caveats and problems of working with data!

Two commonly used datasets in conflict research are the UCDP Non-State Conflict dataset, which provides a list of armed conflicts where *states were not involved* on a country-year level and the UCDP Geo-Referenced Event Dataset (GED) which provides details on individual battles (down to day and village level). GED provides battle events for all three conflict types, *state-based*, *non-state* and *one-sided*. 

I've prepared two simplified and cleaned-up versions of the two datasets here:

GED: https://raw.githubusercontent.com/mihaicroicu/AQM2019/master/assignments/data/ged_assign1.csv

Non-State: https://raw.githubusercontent.com/mihaicroicu/AQM2019/master/assignments/data/nonstate_assign1.csv

Please use these files *and only these files* for the assignment.

A codebook describing what is in these files is available here: https://github.com/mihaicroicu/AQM2019/blob/master/assignments/codebook.md


Tasks:

Explore the two datasets and write scripts doing the following:

1. `EASY` `code` Calculate a **yearly** count of battle events and a yearly sum of total fatalites for the *non state* category. Non-state conflict is conflict having a `type_of_violence == 2`. Provide the code doing this.

2. `EASY` `code` How many distinct state-based conflicts (not events, but conflicts) are **NOT** active in each year in the GED dataset? Provide the code doing this.

A common problem researchers and anlysts have is that non-state conflict is sub-divided into three sub-types called organization types (communal, organized and supportive). This data is not available in `GED` but is available in `Non-State`. You want to know the behavior of those conflicts based around a *communal* organization type (this is called "communal conflict" or "tribal conflict in literature).

Thus:

3. `MEDIUM` `code+write` Write the code that produces a dataset containing **sums of fatalities** and **counts of battle events** by **conflict-year** (i.e. each row should be a conflict for a given year, e.g. NSF, 1990 should be a row; NSF, 1991 should be another row and so on) and **only covers communally organized non-state conflict**. For your research you need only **active** conflict-years included in your dataset. Write a short (1-3 paragraphs) summary describing *the choices you made* and the *plan* you did to solve this.

Another common problem researchers have is needing monthly data. You have this problem for your research too!

Thus:

4. `MEDIUM` `code` Make a dataset where you summarize `GED` computing **sums of fatalities** and **counts of battle events** by country-month only for **Africa**, only for **2016** and only for **state-based conflict**.

5. `HARD` `write+code` Your reviewer asks you to compute the **1-month lag** of **counts of battle events** and **sums of fatalities** for the dataset you computed at task **4.**. Can you do it using the dataset you computed at task **4.**? Why? Why not? Think about what happens to the lags when a month has no events and no fatalities in that month, but the month before and after does have events. Write 1-2 paragraphs. Is this dataset : https://raw.githubusercontent.com/mihaicroicu/AQM2019/master/Data/scaffold.csv
of any assistance? Why? Why not? Show all the code you used to explore the data (if you used any) and write the code to compute the lags.

*Provide the answers as a commented code file (eg. an `R` script)*. Text parts can be written either as *comments in the code* or in a *separate document*. While we taught you how to do this using `R` and `tidyverse/dplyr`, you can use any open-source programming language you want - we are able to grade `R`, `Python`, `SQL` and `Julia`. You **MAY NOT** use `STATA`, `SAS`, `MINITAB`, `MATLAB` or `SPSS` (as they are not open-source).
