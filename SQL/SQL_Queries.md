# SQL Queries for OLA Ride Analysis

## Q1. Retrieve successful bookings
```sql
create view successfull_booking as
select * from ola_data where booking_status="success";

select * from successfull_booking;

## Q2 Find the average ride distance for each vehicle type
```sql

create view Avg_distance as
	select vehicle_type,avg(ride_distance) as Avg_distance from ola_data group by vehicle_type;
    
select * from avg_distance;

## Q3 Get the total number of canceled rides by customers
```sql

create view booking_cancelled_by_customer as
	select count(booking_status) as number_of_cancelled_rides from ola_data where booking_status="canceled by customer";
    
select * From booking_cancelled_by_customer;

## Q4 list the top 5 customer who booked the highest number of rides
```sql
create view top_5_customer as
select customer_id,count(*) as top_customer from ola_data group by customer_id order by top_customer desc limit 5;

select * from top_5_customer;

## Q5 Get the number of rides cancelled by driver due to personal and car related issues
```sql
create view total_cancelled_rides_by_driver as
select count(*)as total_cancelled_rides from ola_data 
where booking_status="canceled by driver" and
 canceled_rides_by_driver="personal & car related issue";
 
 select * from total_cancelled_rides_by_driver;

## Q6 find the maximum and minimum driver rating for prime sedan
 ```sql
 create view max_and_min_rating_by_prime_sedan_driver as
	select max(driver_ratings) as max_rating_by_driver,
 min(driver_ratings) as minimum_driver_rating from ola_data data where vehicle_type="Prime sedan";

select *from max_and_min_rating_by_prime_sedan_driver;

## Q7 retrive all rides where payment was made using upi
```sql

create view all_rides_with_upi as
select *from ola_data where payment_method="upi";

select * from all_rides_with_upi;

## Q8 find the average customer rating per vehicle type
```sql
create view avg_customer_rating_by_vehicle_type as
select vehicle_type,round(avg(customer_rating),2) as avg_rating from ola_data group by vehicle_type; 

select * from avg_customer_rating_by_vehicle_type;

## Q9 calculate the total booking value of rides compeleted successfully
```sql
create view total_success_booking_value as
select sum(booking_value) as total_success_booking_value from ola_data where booking_status="success";

select * From total_success_booking_value;

## Q10 list all incomplete rides along with the reason
```sql
create view incomplete_rides as
select booking_status,vehicle_type,incomplete_rides,incomplete_rides_reason from ola_data 
where incomplete_rides="yes";

select * From incomplete_rides;
