# Mulesoft_RestFullService-Database-
======================
**First Project:**
======================
- create a rest service.
- Read JSON fields from mule event JSON payload.
- Insert fields into database table.

**URL:** http://localhost:8081/emp-sapi/create-employee (POST)

**HTTP request body:**
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

**HTTP response header:** 200, success

**HTTP response body:**
{
	"status": 200,
	"message": "Success"
}
