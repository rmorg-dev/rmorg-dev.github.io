---
layout: default
title: "ENHANCEMENT THREE - DATABASES"
permalink: /Enhancement3/
---

# ENHANCEMENT THREE
This artifact was first created when I took the CS-300 Data Structures and Algorithms course at SNHU. I took it in the Fall of 2024. The program was designed to read a CSV file of courses and their prerequisites. The original project outcome for this assignment was to show an understanding of creating, implementing, and understanding efficient data structures. I chose this initial artifact to demonstrate my ability to implement a database on a project that does not initially contain one. The original artifact allowed you to read in a CSV file, however this step would need to be completed during every run of the program which is inefficient. The following improvements and skills were made/demonstrated in the artifact:
-	Database Security: By using sqlite3_bind_text for the course number searched by the user instead of directly concatenating it into a SQL query, I ensure that users are not allowed to input malicious SQL statements into the database.
-	Database design: By storing my prerequisites in a table that is linked to the course number, I ensure that the many-to-many relationship between courses and their prerequisites is effectively demonstrated using SQLite.
- Resource-conscious decision making: By using my previously implemented dynamic array, I can store course numbers and check if a user-inputted course even exists before accessing the disk or running SQL queries on the database. I also made sure to update my dynamic array to only store the course numbers instead of the previous design of being the main data structure. By removing the course name and prerequisite storage of the array, I removed redundant and unnecessary memory usage within the application.

For this enhancement, I chose outcome 5. Outcome 5 is demonstrated within my code using the sqlite3_bind_text function to have parameterized queries as well as choosing SQLite to reduce a potential network attack vector that would be present in a database like MongoDB. This was the hardest enhancement so far. I had to reteach myself SQL as well as understand how to use SQLite within a week. I also created an entirely new CSV file using the SNHU course catalog which made me run into a few unique issues like how to handle and parse quoted strings since some of the names of courses had commas within their names. I also realized midway through that having a database and a full array with search functionality was redundant, so I had a slight issue deciding how to continue this enhancement. I eventually landed on my current solution of using the array as a check for user-input before accessing and checking the database which works well with my overall showcase of resource-conscious design throughout the entire portfolio. I also ended up adding a button to my design to add courses to the database, however when looking back, this addition completely strayed from the idea of my application being solely used as a search application as well as introduced complications to the previously implemented data structure and the trade-offs I mentioned. 


+ [link to original artifact](https://github.com/rmorg-dev/CS300)
+ [link to enhanced artifact](https://github.com/rmorg-dev/CourseScheduler)

---

+ [Self-Assessment](index.md)
+ [Code Review](CodeReview.md)
+ [Enhancement One: Software Design and Engineering](Enhancement1.md)
+ [Enhancement Two: Data Structures and Algorithms](Enhancement2.md)
