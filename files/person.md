## Person List

 *  Filename MUST be `person.txt`
 *  File MUST contain a record for person taking a trip that requires person-level variables for route choice.
 *  File MAY contain extraneous person records.
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.
 
File MUST contain the following attributes:

Field         	| Type   	| Description
--------------	|--------	|--------------------------------------------------------------------------------------------------------
`person_id`     |int or str | ID that uniquely identifies the traveller and used to link to `trip_list.txt`.
`hh_id`         |int or str | Household ID used to link to household information in `household.txt`. Use 0 (zero) to identify people that do not have a disaggregate household record associated with them.


File MAY contain the following attributes:

Optional Fields | Type   	| Description
--------------	|--------	|--------------------------------------------------------------------------------------------------------
`age`         	|int		| Age in years.
`gender`        |str     	| Valid entries: <br> `male` <br> `female`
`worker_status` |str     	| Valid entries: <br> `unemployed` <br> `full-time` <br> `part-time`
`works_at_home` |bool     	| Boolean value for working at home.
`multiple_jobs` |bool     	| Boolean value for having two or more jobs.
`transit_pass`	|bool     	| Boolean value for having a transit pass.
`disability`	|str     	| Disability status.  Valid entries include: <br> `none` <br> `wheelchair` <br> `walker`
