-------------------------------------Stage 1-------------------------------------

Rest-api-endpoints: 

https//localhost:5000/api/loggedin
Respone: Log In Successful

https//localhost:5000/api/alerts
Response: Deal


----------------------------------Stage 2------------------------------------------------

I suggest SQL db schema because it is more reliable database and can handle large volume of data in a structured way.
CREATE DATABASE APP;
CREATe TABLE Notification;


----------------------------------Stage 3-------------------------------------------------
 
Query is accurate but it is slow because data volume is increased by which this query is checking all the data in db
Adding Index does not effective because in this db student-id is already working as an index values
Select * From notification
where notificationType = [7, True, Placement] 