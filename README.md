# neo4j-CRUD
Implemented CRUD operations using neo4j graph DB

Steps to SetUp and Run the App:-

Step1:-  Install Neo4j for database usuage.
Step2:-  Create a School database containing table studens which has name, age, grade and is as column as following

          "CREATE (s:Student {id: $id, name: $name, age: $age, grade: $grade}) RETURN s",
                id=student_id, name=name, age=age, grade=grade"

Step3:- Insert some data to check whether we are able to fetch it using query.
Step4:- Implement utility function for connecting to a database and executing the query.
Step5:- Implement CRUD function to create update read and delete student.
Step6:- Implement Endpoint for each operations having different usuage.
Step7:- To run the application in IDE go to the terminal containing the file and apply below command to the
        app will run as a localhost connected to DB.
        Command:- uvicorn main:app --reload
Step8:- Install Postman as a tool to run the endpoints and check whether we are able to implement CRUD operations and url and body
        for the request are as follows:-
        GET ALL API:- 
            URL:- http://localhost:8000/students/
        GET BY ID API:- 
            URL:- http://localhost:8000/students/1
        POST API:- 
            URL:- http://localhost:8000/students/
            BODY:- {
                        "name": "Dikshant",
                        "age": 24,
                        "grade": "A"
                    }
        PUT API:-
            URL:- http://localhost:8000/students/1
            BODY:- {
                        "name": "Dikshant P",
                        "age": 23,
                        "grade": "A+"
                    }
        DELETE API:-
            URL:- http://localhost:8000/students/1
