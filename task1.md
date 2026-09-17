# 1.

The classes I will have will be User, Professor, Student, Course, Announcement, Feed, and Enrollment

# 2. 

User to Client: The professor opens the course page in the client and writes an announcement, then posts by clicking "Post.

Client to Server: The client sends a request to the server with the announcement text, course id, and the professor’s auth credentials/session.

Server: The server checks the professor's auth credentials and sees if they are allowed to post for that course. If so, it then builds an Announcement for the Course, and decides which enrolled students’ feeds should include it.

Server to database: The server stores the announcement and other values related to it in the database.

Database to Server: The DB confirms the write or returns an error.

Server to Client: The server responds with success; the professor’s client shows the posted announcement.

Student: when the student opens their feed, the client then requests the feed from the server, which then queries the DB for announcements in the classes the student is enrolled in and then returns that list. This list is then displayed.


## 3. 

The design pattern Observer would be primed for application here. The underlying problem is that when a professor posts an announcement, the set of students that are enrolled in the course need to be made aware of it and update their displays. We do not want the code that posts these announcements to have to know the full list of students in the course and update each individual students display.

To solve this, we should create a subscription mechanism to notify the students in the course about any announcements that happen. The Subject is the Announcements Board/List and the Observers are each student's feed.



