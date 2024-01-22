Student Management System
Overview
The Student Management System is a database management system designed to manage information related to students,
teachers, classes, and subjects. It provides a structured storage and retrieval mechanism for essential data related to educational institutions.

Database Structure

1.The system is implemented using a PostgreSQL database with the following tables:
2.user_login: Stores user login details, including user ID, password, first name, last name, sign-up date, and email ID.
3.parent_details: Contains information about parents, including parent ID, father's details (first name, last name, email, mobile, occupation), and mother's details (first name, last name, email, mobile, occupation).
4.teachers: Stores information about teachers, such as teacher ID, first name, last name, date of birth, email ID, contact details, registration date, and registration ID.
5.class_details: Manages class information, including class ID, class teacher (references teachers table), and class year.
6.student_details: Contains details about students, including student ID, first name, last name, date of birth, class ID (references class_details table), roll number, email ID, parent ID (references parent_details table), registration date, and registration ID.
7.subject: Stores information about subjects, including subject ID, subject name, class year, and subject head (references teachers table).
8.subject_tutors: Manages the association between subjects, teachers, and classes.

Table Relationships

1.The user_login table is related to the student_details and teachers tables, allowing for user authentication for students and teachers.
2.The parent_details table is linked to the student_details table through the parent ID.
3.The class_details table is associated with the teachers table, where the class teacher is a reference to a teacher.
4.The student_details table references the class_details and parent_details tables, providing details about the student's class and parent.
5.The subject table is related to the subject_tutors and teachers tables, establishing the connection between subjects, teachers, and classes.

Instructions

1.Execute the SQL statements in the given order to create the necessary database, schema, and tables.
2.Ensure that the foreign key relationships are maintained to preserve data integrity.
3.The system is designed to manage user logins, parent details, teacher information, class details, student details, subjects, and subject tutors.
4.Customize and extend the system as needed based on specific requirements.
