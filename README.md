# SQL-Repository
Collation of SQL course Projects, Exercises.


/* 
1. My partner and I want to come by each of the stores in person and meet the managers. 
Please send over the managers’ names at each store, with the full address 
of each property (street address, district, city, and country please).  
*/ 

select
	staff.store_id
    , staff.first_name
    , staff.last_name
    , address.address
    , address.district
    , city.city
    , country.country
from staff
inner join
	address on staff.address_id = address.address_id
inner join 
	city on address.city_id = city.city_id
inner join
	country on city.country_id = country.country_id;
