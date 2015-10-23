
## Dyno-Demand

A GTFS-based data transit network data standard suitable for dynamic transit modeling.

**version**: 0.1.0  
**updated**: 17 June 2015  
**created**: 17 June 2015  
**authors**:  

 * Bhargava Sana  (San Francisco County Transportation Authority) 
 * Lisa Zorn (LMZ LLC)  
 * Elizabeth Sall (UrbanLabs LLC)  

[issues]: https://github.com/osplanning-data-standards/dyno-demand/issues
[repo]: https://github.com/osplanning-data-standards/dyno-demand

NOTE: This is a draft specification and still under development. If you have comments
or suggestions please file them in the [issue tracker][issues]. If you have
explicit changes please fork the [git repo][repo] and submit a pull request.

### Changelog

-  `0.1.0`: initial commit; [Technical Memo Documentation](http://fast-trips.mtc.ca.gov/library/)  

### Known Issues
  
* Trips currently do not relate to tours or trip chains.  Since this is not currently a capability in 
the dynamic transit model [Fast-Trips](http://github.com/MetropolitanTransportationCommission/fast-trips) 
for which this format was designed, this is not deemed an immediate issue that needs resolution.




# Specification

A Dyno-Demand dataset consists of required and optional data files that together 
describe the demand for transportation.  

A Dyno-Demand dataset MUST include the following files:

Filename 								| Description										
----------								| -------------										
[`trip_list.txt`](/files/trip_list.md)	| Trip attributes													

A Dyno-Demand dataset MAY include the following files:

Filename 								| Description										
----------								| -------------		
[`person.txt`](/files/person.md)		| Person attributes
[`household.txt`](/files/household.md)	| Household attributes
