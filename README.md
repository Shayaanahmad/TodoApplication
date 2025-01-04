
# Project Title

REST API service

# Description

Create a REST API service to manage a simple to-do list application in Eclipse Workspace.
## How To Run

If you're using Eclipse, right-click on TodoAppApplication.java and select Run As > Java Application.
Set Up Postman:

Download and install Postman.
Open Postman and create a new request.

* POST - Create a New Task
    * Method: POST
    * URL: http://localhost:8080/tasks
    * Headers:
        * Content-Type: application/json
    * Body:
    ```bash
    {
    "title": "Complete homework",
    "description": "Finish math and science homework"
    }
    ```
    * Expected Response (HTTP 201 Created):
    ```bash
    {
    "id": 1,
    "title": "Complete homework",
    "description": "Finish math and science homework",
    "status": "pending"
    }
    ```

* GET - Fetch All Tasks
    * Method: GET
    * URL: http://localhost:8080/tasks
    * Expected Response:
    ```bash
    {
    [
        {
            "id": 1,
            "title": "Complete homework",
            "description": "Finish math and science homework",
            "status": "pending"
        }
    ]

    ```

* GET - Fetch a Task by ID
    * Method: GET
    * URL: http://localhost:8080/tasks/1
    * Expected Response:
    ```bash
        {
        "id": 1,
        "title": "Complete homework",
        "description": "Finish math and science homework",
        "status": "pending"
        }
    ```
* PUT - Update Task Status
    * Method: PUT
    * URL: http://localhost:8080/tasks/1?status=in-progress
    * Headers:
        * Content-Type: application/json
    * Expected Response:
    ```bash
    {
        "id": 1,
        "title": "Complete homework",
        "description": "Finish math and science homework",
        "status": "in-progress"
    }

    ```
* DELETE - Delete a Task by ID
   * Method: DELETE
   * URL: http://localhost:8080/tasks/1
   * Expected Response (HTTP 204 No Content): No body.



## Release History

* 0.0.1
    * The First Release
