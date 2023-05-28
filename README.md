### Teztable backend management platform

1. Project overview
1.1project background

This project is to design and implement a platform where customers can log in and view the details of the orders and the results of tests. The functions of the platform mainly include user management, order management, and report management.

1.2 project introduction

This project includes the client side, test side, and company operation side.
Core modules include user management, order management, and report management.
This is the functional module diagram of the project:




















1.3 use case diagram

Below, I have used a use case diagram to illustrate the interactions between users and our system, showcasing the functionalities it can perform. From this diagram, you can see that the system has three users, and each user has different permissions. The company's operational team can create and delete users, while clients and testers can log in, modify their profiles, and perform logouts after receiving assigned accounts. Additionally, clients can create test requirements within the system, which the company reviews and assigns to suitable testers. Once testers complete the testing and list all issues, clients can check the issues and operate on this issues and give feed back to testers. If issues are corrected and passed the test, then issues will be deleted from the page.
 <img width="451" alt="image" src="https://github.com/frirsta/admin-dashboard/assets/88880169/30e2a43f-e9cb-4414-bdc4-ad10ed5ff331">




2 Database design
2.1 ER diagram
The ER diagram currently defines 5 entities and their attributes. The invoice and report entities are still uncertain. Based on the information I have obtained, the report is simply a project progress report sent to the client and does not require database CRUD operations. Therefore, I believe it is unnecessary to create a separate table for it. As for the invoice entity, I need to confirm the attributes before making a determination.
For these 5 entities, I will create 5 tables in the database to store relevant information about administer, tester, client, test, and issue. These tables, except for the issue table, will use their own ID as the primary key for unique identification. However, for the issue table, I will use a combination of the test table's ID and the issue's ID as the composite primary key.

<img width="451" alt="image" src="https://github.com/frirsta/admin-dashboard/assets/88880169/894df173-7859-4d5c-ae80-f7e7eaaae3bf">



