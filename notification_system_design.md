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




---------------------------------------------Stage 4----------------------------------------------------

Sending an email and saving in db should be separate as notfying 50000 students and saving in db simultaneously brings a load on the database, that's why it crashed midway
Pseudocode:
function notify_all(student_ids: array, message: string):
        for student_id in student_ids:
            send_email(student_id, message)

        for student_id in student_ids:
            save_to_db(stuent_id, message)
            push_to_db(stuent_id, message)