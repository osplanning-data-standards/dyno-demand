## Trip List

 *  Filename MUST be `trip_list.txt`
 *  File MUST contain a record for each trip to be assigned.
 *  File MUST be a valid CSV file.
 *  The first line of each file MUST contain case-sensitive field names.
 *  Field names MUST NOT contain tabs, carriage returns or new lines.
 
File MUST contain the following attributes:

Field         	| Type   	| Description
--------------	|--------	|--------------------------------------------------------------------------------------------------------
`person_id`     |int or str | ID that uniquely identifies the traveller. Use 0 (zero) to identify trips that do not have a disaggregate person-record associated with them.
`o_taz`         |int or str | Trip origin zone
`d_taz`         |int or str | Trip destination zone
`mode`          |str     	| Trip mode, which must match a valid specification for route choice and the modal hierarchy. 
-				|-	 		|    For transit, the mode should encapsulate access and egress modes.  Example entries include:
-				|-		 	|    	`walk-local_bus-walk`
-				|-			|    	`PNR-commuter_rail-walk`
-				|		 	|    Example main modes:
-				|		 	|    	`local_bus`
-				|		 	|    	`premium_bus`
-				|		 	|    	`light_rail`
-				|		 	|    	`commuter_rail`
-				|		 	|    	`street_car`
-				|		 	|    	`ferry`
-				|		 	|    Example access or egress modes:
-				|		 	|    	`walk`
-				|		 	|    	`bike_own`
-				|		 	|    	`bike_share`
-				|		 	|    	`PNR`
-				|		 	|    	`KNR`
`purpose`       |str     	| Trip purpose, which can include any segmentation of purpose that is deemed appropriate for segmenting the route choice model so long as there are corresponding parameters specified in the route choice controls file.
-				|		 	|    `work`
-				|		 	|    `school`
-				|		 	|    `personal_business`
-				|		 	|    `shopping`
-				|		 	|    `meal`
-				|		 	|    `social`
-				|		 	|    `work-based`
-				|		 	|    `other`
-				|		 	|    `visitor`
`departure_time`|HH:MM:SS	| Desired departure time.
`arrival_time`  |HH:MM:SS	| Desired arrival time.
`time_target`   |str     	| Arrival/Departure preference indicator.
-				|		 	|    `arrival` - arrival time is more important
-				|		 	|    `departure` - departure time is more important
`vot`	        |float   	| Value of time for trip in dollars / hour

File MAY contain the following attributes:

Optional Fields | Type   		| Description
--------------	|--------		|--------------------------------------------------------------------------------------------------------
`pnr_ids`	    | List of int	| Available park and rides.  A comma-delimited list of stations within brackets.  An empty list implies any accessible park and ride can be used. Example: [1219, 3354, 9485]

