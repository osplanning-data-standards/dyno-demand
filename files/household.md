## Household List

 *  Filename MUST be `household.txt`
 *  File MUST contain a record for household with a person taking a trip that requires household-level variables for route choice.
 *  File MAY contain extraneous household records.
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.
 
File MUST contain the following attributes:

Field         	| Type   	| Description
--------------	|--------	|---------------------------------------------------------
`hh_id`         |int or str | Household ID used to link to person in `person.txt`. 


File MAY contain the following attributes:

Optional Fields | Type   	| Description
--------------	|--------	|---------------------------------------------------------
`hh_vehicles`  	|int		| Number of household vehicles in working order.
`hh_income`     |int     	| Annual household income.
`hh_size`		|int     	| Household size.
`hh_workers`	|int     	| Number of workers living in household.
`hh_presch`	 	|int     	| Number of young children 0-4 years old.
`hh_grdsch`	 	|int    	| Number of grade-school children 5-15 years old.
`hh_hghsch`		|int    	| Number of high-school children 16-17 years old.
`hh_elders`		|int     	| Number of elderly people 65 and over years old.