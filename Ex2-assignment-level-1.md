## BLOCK-readText

#### Timeline for the entire topic - 3 hours.

In this topic, you have to build a small web API from scratch for the following user stories.

*Note - This is not fullstack application, you only have to build the API using Node.js, Express.js and MongoDB. Please follow standard web practices.*

```
1. There are two kinds of users in our system 
  - students
  - mentors
2. A student should be able to signup using following information.
  - Name, Email Id, Password, Batch Number.
3. A student should be able to login using his/her email id and password.
4. Atleast 3 mentors should be automatically seeded into the database and so they don't have to signup. Mentor data should be seeded with the following information.
  - Name, Email Id, Password.
5. A mentor should be able to login using email and password.
6. The identification route for both the types of users has to be the same.
7. A mentor should be able to add a task in a resource called `Todo` with following info.
  - Name of todo, Whether its completed or not.
8. A mentor should be able to see all the tasks.
9. A student should be able to see all the tasks but should not be able to add a new task.
```

## BLOCK-writeTextAnswer

Here write the psuedo code you would follow to build the above API.

step 1 ) Decide the Models
	
	*Students
	*Mentors
	*Todos

step 2 ) Design the Schema

	*Students model will have the following fields

	1) Name :- type: String, required: True.
	2) Email-Id :- type: String, required: True, use email-validator module to validate the email.
	3) Password :- type: String, required: True, use pre-save hooks to hash password before saving. 
		       Also include password verification method to verify the password at login.
	4) Batch Number : type: Number, required: True.
	
	*Mentors model will have the following fields

	1) Name :- type: String, required: True.
	2) Email-Id :- type: String, required: True, use email-validator module to validate the email.
	3) Password :- type: String, required: True, use pre-save hooks to hash password before saving. 
		       Also include password verification method to verify the password at login.
	
	 3 mentors details pre-seeded into the database and so they don't have to signup.
	

	* To-do model will have the following fields

	1) title :- type: String, required: True.
	2) isCompleted :- type: Boolean, required: True.

step 3) Decide the routes

	*signup route for students.
	*login route for both students and mentors.
	*route for mentors only to add new tasks.
	*common route for both students and mentors to view the tasks uploaded.
	
	
