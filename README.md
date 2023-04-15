# Airlines-Booking-System
Implement Database management system for Airline Booking System using SQL Server Database

### Business Requirement:
  The requirement is to develop a database system that can be utilized for Airline service bookings and reservations. An Airline booking system will efficiently and safely keep record of **booking records, flight schedules and passenger information**. Booking information should be accessible from the database with minimal effort. Airlines require a method of managing everything as they must constantly handle bookings from passengers. By keeping a single centralized database and only saving data once, the system **minimizes redundancy**. 
	
  Customers can use this database to verify their tickets and reservations, get price information, and retrieve information on a number of flights that are available at various times on a particular date. It keeps track of the source, destination, and any layovers as well as all the other information required to arrange a trip.
	
  The database implementation is to be done in **Microsoft SQL Server** database.
	
### Business Entities & Relationships:
  Following are the required Entities and its corresponding properties. There will be one-to-many and one-to-one relationships existing among the different entities available in order to make the data less redundant.

1. Airport - AirportCode, Name, Location, Country
2. FlightDetails - Flight_ID, Name, Source, S_ID, Destination, D_ID, D_datetime, A_datetime
3. FlightClass - Class_ID, ClassName
4. Passengers - Name, P_ID, Age, Gender, EmailId, Mobileno
5. FlightService - ServiceID, Service
6. Seats- SeatID,FlightID, Class_ID, Service_ID
7. FlightCost - Flight_ID, SeatID , Amount
8. DateTime - Date, Weekday, Month, Year
9. Payment - PaymentID, Amount
10. PaymentStatus- PaymentID, BookingID, Status
11. Bookings - BookingID, P_ID, Flight_ID, Seat_ID, TravelDate, Src, Dest


*One-to-Many relationships* - Flight_Details to Bookings, Airport to Flight_Details, DateTime to Flight_Details, FlightDetails_FlightCost, Passengers to Bookings, FlightService to Seats, FlightClass to Seats, DateTime to Bookings, Flight_Details to Seats  
_One to one relationships_ - FlightCost to Seats, Payment to PaymentStatus, PaymentStatus to Bookings, Seats to Bookings


### ER Diagram:

Here is the Entity-Relationship diagram for the relationships described as above.

![image](https://user-images.githubusercontent.com/64007718/232231949-0626fb96-e74c-4788-8377-dfbe9028516f.png)
