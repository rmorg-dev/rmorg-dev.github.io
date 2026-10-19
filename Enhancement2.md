---
layout: default
title: "ENHANCEMENT TWO - ALGORITHMS AND DATA STRUCTURES"
permalink: /EnhancementTwo/
---

# ENHANCEMENT TWO
This artifact was first created when I took the CS-300 Data Structures and Algorithms course at SNHU. I took it in the Fall of 2024. The program was designed to read a CSV file of courses and their prerequisites. The original project outcome for this assignment was to show an understanding of creating, implementing, and understanding efficient data structures. I chose this initial artifact to demonstrate my growth in choosing and developing data structures. Since the initial course was a Data Structures course, I thought this would be the perfect opportunity to demonstrate the growth. When I initially created this artifact in my CS-300 course, I did not know anything about Big O notation. I chose the data structure based on pseudocode I wrote and the accompanying runtime analysis. While it seemed like the best from the choices I was given, I soon realized that is not the case given the tree’s inability to self-balance. This lead me down a rabbit hole of determining which data structure is better for a one-time insert function run and multiple searches which lead me to my improvement of switching out the Binary Search Tree for a dynamic array data structure with a binary search algorithm. The following improvements and skills were made to the artifact:
- Data Structure design: By implementing my own dynamic array, I am showcasing my ability to understand how memory management works within C++. It also showcases my ability to understand resource-conscious data structures and use appropriate data structures when applicable.
- Complexity Analysis: The previous Binary Search Tree had a runtime analysis that was O(log n) best case, and O(n) worst case. The benefit of my dynamic array means that search time will always be O(log n) since it cannot become unbalanced like my Binary Search Tree was vulnerable to. However, the O(log n) search time is only when the array is sorted. Since end users have the ability to add courses, this means there is an additional cost of O(n log n) every time a new course is inserted as well as when the application is first ran on a device. So the efficiency of the program ultimately depends on how often an end user is inserting courses compared to searching for courses. 
- Analysis of Trade-Off: Like previously mentioned, without the 3rd enhancement and increasing the size of the CSV file, The binary search tree would be perfectly fine to use in this specific situation with a very small file. However, if I were to add balancing logic to the tree, it would still not be the most efficient data structure to use due to the complexity of implementation for a very simple course catalog application where data is only inserted once. If the application was built for an administrator who was inserting new courses frequently, it would be a good implementation. Because the catalog in the current version of the application is loaded once and searched multiple times, the initial cost of sorting the array is justified. However, if future iterations of this program were to include an add and modify function, then the cost of the current implementation of the dynamic array will need to be reconsidered.

For this enhancement, I chose outcomes 3 and 4. However, upon further evaluation, I believe I only fully covered Outcome 3 with this enhancement. Outcome 3 is demonstrated within my code through the development of my own custom dynamic array used to hold the course information loaded from the CSV file. It is also demonstrated in my narrative write up while explaining the trade-offs made when deciding to switch to this new data structure. This enhancement was a lot of researching the differences in resource usage and time complexity between data structures and their best use cases with a lot less coding. As I was improving this information, I learned a lot more about Big O notation and why understanding data structures and their tradeoffs is important. You can use a fast search data structure for your project, but you may implement something that is unnecessarily complex for the scope, scale, and size of your project. The biggest challenge I had was understanding whether to use a static array or a dynamic array. While a static array is great for extremely resource conscious designs, the size must be declared at compile time. This makes it unpractical if my application is for a real course catalog that changes and grows over time.


+ [link to original artifact](https://github.com/rmorg-dev/CS300)
+ [link to enhanced artifact](https://github.com/rmorg-dev/CourseScheduler)

---

+ [Self-Assessment](index.md)
+ [Code Review](CodeReview.md)
+ [Enhancement One: Software Design and Engineering](Enhancement1.md)
+ [Enhancement Three: Databases](Enhancement3.md)

