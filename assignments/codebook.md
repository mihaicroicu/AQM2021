-----------------
Codebook for the GED mini-dataset 
-----------------

This is a dataset of daily battle events, including fatality estimates, in various global conflicts. Contains three kind of conflicts : state-based (where states fight rebels), non-state (where rebels or tribes fight each-other) and one-sided (where civilians get killed).

The dataset includes battles in *"ACTIVE"* conflict-years and in *"NON-ACTIVE"* conflict years. 
An *"ACTIVE"* conflict-year is a year where a conflict had at least 25 total deaths in battles.

*id* - A unique battle event identifier

*year* - Year of observation (2010 - 2017)

*active_year* - Is this year active in terms of UCDP definitions. 
    - Years with a "1" are part of UCDP conflicts.
    - Years with a "0" are not part of UCDP conflicts.
			  
*type_of_violence* - Type of violence
   - "1" : state-based conflict
   - "2" : non-state conflict
   - "3" : one-sided violence

For a conflict to be included in the NON-STATE DATASET, the type_of_violence must be 2

*conflict_number*  - a unique identifier for conflicts. SAME system is used for "conflict_id" in the NON-STATE dataset (conflict with conflict_number == 193 in this dataset will be the same with the one with conflict_id == 193 in other dataset).
     
*conflict_name* - name of conflict. NOT SAME system as in the NON-STATE dataset
      
*group1_number* - a unique number for one of the two fighting groups fighting each-other in the battle
      
*group1* - a unique name for one of the two fighting groups fighting each-other in the battle

*group1_number* - a unique number for one of the two fighting groups fighting each-other in the battle
      
*group1* - a unique name for one of the two fighting groups fighting each-other in the battle

*latitude* - latitude of the battle

*longitude* - longitude of the battle

*priogrid_gid* - a unique spatial grid identifier for the location of the battle

*country* - country name. Tip: NEVER MATCH ON COUNTRY NAMES! Everyone names these differently.

*country_id* - a unique identifier for the country. SAME system as in the NON-STATE dataset

*region* - the continent where the battle has taken place. One of following:
   - Asia
   - Americas   
   - Africa     
   - Middle East
   - Europe

*date_prec* - a score for how precise the date of the event is.

*date_end* - the date the event took place.

*deaths* - fatality estimates for deaths taking place in each battle.

*month_event* - month when event took place (1-12)


-------------------
Codebook for the NON-STATE dataset
-------------------

This is a dataset of yearly non-state conflicts.
To be included here, one conflict must be GED type_of_violence==2 
Only *ACTIVE* conflict-years are inclued. That means a conflict must have 25 deaths in battle events in GED in that year.

*conflict_id* - a unique identifier for conflicts. SAME system is used for "conflict_number" in the GED dataset (a conflict with conflict_number == 193 in GED will be the same with the one with conflict_id == 193 in NON-STATE).

*org_class* - What kind of NON-STATE organizations do we have?
    - 1. "organized" (rebel vs. rebel)
    - 2. "supportive" (supporters of politicians/organizations vs. other supporters)
    - 3. "communal" (tribe vs. tribe or group vs. group).

*side_a_id* - a unique number for one of the two fighting groups fighting each-other in the battle
      
*side_a_name* - a unique name for one of the two fighting groups fighting each-other in the battle

*side_b_id* - a unique number for the other of the two fighting groups fighting each-other in the battle
      
*side_b_name* - a unique name for the other of the two fighting groups fighting each-other in the battle

*year* - Year of observation (2010 - 2017)

*region* - the continent where the battle has taken place. One of following:
- 1 for Europe
- 2 for Middle East
- 3 for Asia
- 4 for Africa
- 5 for Americas

*country_id* - a unique identifier for the country. SAME system as in the NON-STATE dataset

*country* - country name 

*conflict_name* - name of conflict. NOT SAME system as in the GED dataset

----------
NOTES:
----------
Both datasets are actually real, but heavily processed. For real work, when doing your own research, do not use these (they contain intentional simplifications), use the REAL deal:

UCDP GED :
**Croicu, Mihai and Ralph Sundberg, 2017, “UCDP GED Codebook version 18.1”, Department of Peace and Conflict Research, Uppsala University**
The full codebook, if curious (but note, we have simplified the coding quite a bit for your little samples) is available here: http://ucdp.uu.se/downloads/ged/ged181.pdf

UCDP Non-State Conflict Dataset :  
**Sundberg, Ralph, Kristine Eck and Joakim Kreutz (2012) Introducing the UCDP Non-State Conflict Dataset, Journal of Peace Research 49(2).**
http://ucdp.uu.se/downloads/nsos/ucdp-nonstate-181.pdf

The "real datasets" are available on UCDP's webpage.
