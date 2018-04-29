## Trip List

 *  Filename MUST be `trip_list.txt`
 *  File MUST contain a record for each trip to be assigned.
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.
 
File MUST contain the following attributes:

Field         	| Type   	| Description
--------------	|--------	|-------------------------------------------------------------------------------------------------  
`person_id`     |int or str | ID that uniquely identifies the traveller. Use 0 (zero) to identify trips that do not have a disaggregate person-record associated with them.
`person_trip_id`		|int or str | ID that uniquely identifies the trip within a given household/person.  ID MAY be sequential.
`o_taz`         |int or str | Trip origin zone
`d_taz`         |int or str | Trip destination zone
`mode`          |str     	| Trip mode, which must match a valid specification for route choice and the modal hierarchy. For transit, the mode should encapsulate access and egress modes separated by hyphens.  
|  |  | Example entries include: <br> `walk-local_bus-walk` <br>	`PNR-commuter_rail-walk`  
|  |  | Example main modes: <br>	`local_bus` <br>	`premium_bus` <br>	`light_rail` <br> `commuter_rail` <br>	`street_car` <br>	`ferry`  
|  |  | Example access or egress modes: <br>	`walk` <br>	`bike_own` <br>	`bike_share` <br>	`PNR` <br> `KNR`
`purpose`       |str     	| Trip purpose, which can include any segmentation of purpose that is deemed appropriate for segmenting the route choice model so long as there are corresponding parameters specified in the route choice controls file.  
|  |  | Examples include: <br> `work` <br> `school` <br> `personal_business` <br> `shopping` <br> `meal` <br> `social` <br> `work_based` <br> `other` <br> `visitor`
`departure_time`|HH:MM:SS	| Desired departure time.
`arrival_time`  |HH:MM:SS	| Desired arrival time.
`time_target`   |str     	| Arrival/Departure preference indicator.  Options include: <br> `arrival` - arrival time is more important <br> `departure` - departure time is more important
`vot`	        |float   	| Value of time for trip in dollars / hour

File MAY contain the following attributes:

Optional Fields | Type   		| Description
--------------	|--------		|--------------------------------------------------------------------------------------------------------
`pnr_ids`	    | List of int	| Available park and rides.  A comma-delimited list of stations within brackets.  An empty list implies any accessible park and ride can be used. Example: [1219, 3354, 9485]
`person_tour_id`		| int or str	| ID that uniquely identifies the tour within a given household/person.  ID MAY be sequential.
