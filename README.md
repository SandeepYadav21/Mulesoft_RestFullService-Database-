# Mulesoft_RestFullService-Database-

**First Project:** **(create-employee.xml)**
- create a rest service.
- Read JSON fields from mule event JSON payload.
- Insert fields into database table.

URL: http://localhost:8081/emp-sapi/create-employee (POST)

HTTP request body:
[
	{
	  "employeeID": 100,
	  "employeeName": "Chinna",
	  "employeeStatus": "A"
	},
	{
	  "employeeID": 101,
	  "employeeName": "John",
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

URL: http://localhost:8091/emp-sapi/update-employee (PUT)

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
