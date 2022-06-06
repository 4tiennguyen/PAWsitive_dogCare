# Designing a Database for PAWsitive Dog Care

My teammate and I want to create a fake business called PAWsitive Dog Daycare. The business is not real, but is treated as if it is real throughout this report to achieve the best database design. So below we
* Gathered business requirements by interviewing the business owners for their database needs.
* Performed design process (in at least third normal form) such as conceptual design, logical design and physical design.
* Created development and test database. Tested required data conversion.
* Designed a UI/UX for the front end.
* Presented and wrote a report communicating the results to non-technical and technical audiences.  

To get the full project report, please visit [my github](https://github.com/4tiennguyen/PAWsitive_dogCare/blob/main/cs157A_Report.pdf) 

# EXECUTIVE SUMMARY
A new company, PAWsitive Dog Daycare is seeking a database for its dog daycare center that offers boarding, grooming and training. The company wants a database that keeps track of their employees’ schedules and customers’ bookings information. The database must go through a formal database design lifecycle to be in at least third normal form. This report describes the process of going through the database design lifecycle to create the database, the detailed design of the database, and the final product/release version of the database and UI.  
Based on the company’s intended use for the database, the end result to access the database will be a web application that anyone can access through the URL. We designed a database that met the needs of the company and provided them with a usable web application. The initial implementation of the database can be done one time by the database designers but once the website is launched all future data can be input through the website.
# BUSINESS RULES
* A manager manages other employees and their schedules. She can change any employee's schedule and modify the price of services.
* Groomer/Trainer/Boarding attendant: These employees can only view their schedules but cannot make changes.
* There are 4 types of employees which are a manager, groomer, trainer, and boarding attendant, so the type of employee must be kept track of somehow.
* Customers can see all available time slots, and can’t see any time slots that are full.
* Customers can reserve a booking time slot for one dog at a time.
* A customer account can have many different dogs and each reservation is made for only one dog at a time.
* The business must have a way to store up to date vaccine information for dogs.
* Both employees and customers can view the pricing and services, but only managers can edit or add new services.
* Customers can create an account before logging in. A customer must have an account before a booking is made and at least one dog must be added to the customer's account at the time of account creation.
* Because customers can have multiple dogs, each booking must have one and only one dog specified.
* Customers can add a dog after logging in.
* An employee can’t have bookings at the same time, so their schedule hours cannot overlap.
Customers pay at the time of check in at the register, if booked for multiple services at one time (common for grooming) then all bookings for that day will be summed together and paid for at once. 
* An employee can only work in one department.
* Boarding employee maximum number of dogs per bookings is 8
* For now, the company only has private training sessions which means each training employee only trains one dog at a time.
# DESIGN
### Conceptual Design
![image](https://user-images.githubusercontent.com/34051678/172109832-d5e34e2a-1ab0-4492-a6f5-26e6d48116fb.png)
### Logical Design
![image](https://user-images.githubusercontent.com/34051678/172109965-0d817c09-a396-439f-a3d3-fd294c328da3.png)
### Physical Design
We initially implemented the database in mySQL which we used as a test environment to create the tables, add constraints, and create the views. Writing the SQL code to create the tables followed easily from the ERD diagram. We decided to create the tables and add the primary keys in the initial table creation, but add foreign keys afterwards. This choice was made simply as a stylistic choice to improve code readability. 
To view the Sql code, please visit [physical design](https://github.com/4tiennguyen/PAWsitive_dogCare/blob/main/CS157_FINAL_PROJECT.sql).
