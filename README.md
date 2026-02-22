# Mulesoft_RestFullService-Database-

**First Project:** **(create-employee.xml)**
- create a rest service.
- Read JSON fields from mule event JSON payload.
- Insert fields into database table.

METHOD: POST
URL: http://localhost:8091/emp-sapi/create-employee (POST)

HTTP request body:
[
	{
	  "employeeID": 100,
	  "employeeName": "Sandeep",
	  "employeeStatus": "A"
	},
	{
	  "employeeID": 101,
	  "employeeName": "Sanjeev",
	  "employeeStatus": "A"
	}
]

HTTP response header: 200, success

HTTP response body:
{
	"status": 200,
	"message": "Success"
}

**Second Project: (update-employee.xml)**
- create a Mule rest service to update to database.
- Read XML fields from mule event XML payload.
- Update fields into database table.

METHOD: PUT
URL: http://localhost:8091/emp-sapi/update-employee

HTTP Request Body:
<?xml version="1.0" encoding="UTF-8"?>
<employee>
    <employeeID>100</employeeID>
    <employeeStatus>I</employeeStatus>
</employee>

HTTP Response Body: Http response header: 200, OK
<?xml version='1.0' encoding='UTF-8'?>
<response>
    <status>200</status>
    <message>Success</message>
</response>

**Third Project: (get-employee-by-id.xml)**

- Mule rest service to fetch from database.
- Read query param from mule event.
- Fetch data from database table.

METHOD: GET
URL: http://localhost:8091/emp-sapi/get-employee?employeeID=100 

Http response header: 200, OK

HTTP Response Body:
{
	"employeeID": 100,
	"employeeName": "Sandeep",
	"employeeStatus": "A"
}

**Fourth Project: (get-employees.xml)**

- Mule rest service to fetch from database.
- Read employees from mule event.
- Fetch all data from database table.

METHOD: GET
URL: http://localhost:8091/emp-sapi/get-employees

Http response header: 200, OK

HTTP Response Body:
[
	{
	  "employeeID": 100,
	  "employeeName": "Sandeep",
	  "employeeStatus": "A"
	},
	{
	  "employeeID": 101,
	  "employeeName": "Sanjeev",
	  "employeeStatus": "A"
	}
]

**Fifth Project: (delete-employee.xml)**

- Mule rest service to delete from database.
- Read URI params from mule event
- Delete records from database table.

METHOD: DELETE
URL: http://localhost:8091/emp-sapi/delete-employee/101/Sanjeev 

Http response header: 200, OK

HTTP response body:
{
	"status": 200,
	"message": "Success"
}
