
## Overview

This project is a comprehensive learning exercise that covers the entire database design process. It begins with the idea phase, moves through creating an Entity Relationship Diagram (ERD), designing the database schema, and finally implements it in PostgreSQL. The system simulates a professional networking platform where three types of users—Job Seekers, Employers, and Recruiters—interact with features like job events, applications, messaging, job postings, and interviews.
## Goals

The goal of this project was to:
- Learn and practice database design from the ground up.
- Understand the relationships between different entities in a complex system.
- Implement a PostgreSQL database based on the schema and design.
- Demonstrate role-based access control (RBAC) to ensure that each type of user has appropriate access to system data.
- Learn about functions, procedures, triggers and jobs in PostgreSQL.
- Explored the process of migrating the PostgreSQL database to MySQL, addressing differences in syntax, functions, and database features to ensure seamless data transfer and system compatibility.
## Design process

1. Idea and Conceptualization:
	- The platform is designed to handle three types of users: Job Seekers, Employers, and Recruiters.
	- Each user type has unique privileges and can access data only using views or functions.
2. Entity Relationship Diagram (ERD):
	- The first step in the design was to create an ERD that visually represents the entities and relationships within the system.
3. Implementation in PostgreSQL:
	- Next step was to create: Tables, views, roles, indexes, functions, procedures, triggers, jobs.
4. Testing:
	- Indexes, Roles, privliges, UDF
5. PostgreSQL to MySQL Migration.
###  Database Schema Overview

**The database schema consists of several interrelated tables that support the core functionalities of the job portal:**

- **Users**: Stores information about job seekers, recruiters, and employers.
- **Employers**: Contains employer details, including company name and password.
- **Job** **Offers**: Contains information about job offers, including title, description, salary, and location.
- **Applications**: Tracks job applications submitted by users to specific job offers.
- **Messages**: Stores messages between users (job seekers, employers, recruiters).
- **Interview** **Scheduler**: Manages interview schedules between job seekers and employers.
- **Profiles**: Allows job seekers to create and manage their professional profiles.
- **Portfolio**: Stores links to portfolios and additional information for job seekers.
- **Status**: Tracks the current employment status of job seekers.
- **Job** **Events**: Manages events related to jobs, such as job fairs, recruitment events, etc.
- **Education**: Stores educational background for job seekers.

### User Roles and Permissions

**Three main types of users interact with the system:**

- **Recruiter**: Can view user profiles, portfolios, job offers, and manage applications. Cannot delete or add new users.
- **Employer**: Can view applications, profiles, and portfolios, and manage job offers and interview schedules.
- **Job Seeker**: Can create and manage profiles, portfolios, apply for jobs, view job offers, and check application statuses and interview schedules.
Permissions for each user role are tested to ensure the correct access levels are granted to sensitive data and actions.

### Key Features

- **SQL Queries**: Several SQL queries have been created to retrieve data, such as finding the user with the most applications or checking rejected applications for specific job offers.

- **Views** : Different views for each user role, such as:

	- Recruiters can view user and job offer details.
	
	- Employers can view applicant stats and job offers.
	
	- Job seekers can view job offers with the highest application counts.

- **Indexes**: Various indexes have been implemented for optimization, such as unique indexes on usernames and employer names, and composite indexes on job offer details like location and salary range.



 
