ASPURIA, CHARLES ANDREI L. 4-B

# JSON POST with Database Integration

The "JSON POST with Database Integration" API allows for the submission of data in JSON format through HTTP POST requests, seamlessly integrating this data into a database for storage or retrieval. It's a vital tool for building modern, data-driven applications that require efficient data transmission and database interaction.

## API Description

The "JSON POST with Database Integration" API is a web service that allows users to send data to a server using the JSON (JavaScript Object Notation) format through HTTP POST requests. This data is typically in the form of structured information, such as user input or application data.

The API's primary function is to receive JSON data from users, extract relevant information, and then integrate it into a database system. This integration process involves storing, updating, or retrieving data in a structured manner within a database.

Key features of this API may include validation of incoming JSON data, handling database connections and queries, and responding to users with relevant status codes or data confirmation.

This API is commonly used in web and mobile applications to enable data transmission and storage in a structured and efficient manner, making it a fundamental tool for building modern, data-driven software systems.

## API Endpoints

### postName (add) Endpoint:

Function: The postName (add) endpoint is used to add new data or records to the database. users send a POST request to this endpoint with data in JSON format, and the API stores this new data in the database.

Required Parameters:

Data Payload: users are required to provide the data to be added in JSON format. This JSON payload contains the information for the new record that needs to be created.

### postPrint Endpoint:

Function: The postPrint endpoint is used to retrieve and display data from the database. users can send a POST request to this endpoint, specifying the data they want to retrieve using parameters, and the API responds with the requested data in JSON format.

Required Parameters:

Query Parameters: users may need to provide specific query parameters to define the criteria for data selection. These parameters could include filters, search terms, or other conditions.

### postUpdate Endpoint:

Function: The postUpdate endpoint is responsible for updating existing records or data entries in the database. users send a POST request with updated data in JSON format to modify specific records.

Required Parameters:

Data ID: users must provide a unique identifier (e.g., data ID) to specify which record should be updated.
Updated Data: users must include the updated data in JSON format, specifying the changes to be made to the existing record.

### postDelete Endpoint:

Function: The postDelete endpoint is used for removing specific records or data entries from the database. users send a POST request with the identifier(s) of the data to be deleted.

Required Parameters:

Data ID: users must provide a unique identifier (e.g., data ID) to identify which record(s) should be deleted. Depending on your implementation, users may be able to provide multiple IDs for batch deletion.

## Request Payload

### JSON Payload postName (Add):

Request Payload:
{
"lname":"hortizuela",
"fname":"manny"
}
Required Fields:
"lname": Represents the last name of the person to be added to the database.
"fname": Represents the first name of the person to be added to the database.

### JSON Payload printName (Retrieve):

Request Payload:

This payload does not include any request parameters or data fields because request to retrieve data from the database without specifying any particular filtering criteria.

### JSON Payload updateName (Update):

Request Payload:
{
"id":1,
"lname":"wick",
"fname":"john"
}
Required Fields:
"id": Represents the unique identifier of the record to be updated.
"lname": Represents the updated last name.
"fname": Represents the updated first name.

### JSON Payload deleteName (Delete):

Request Payload:
{
"id":1
}
Required Fields:
"id": Represents the unique identifier of the record to be deleted.

## Response

### JSON Payload postName (Add):

Response Payload:
"status" (Required): Indicates the status of the operation. In this case, it is set to "success" to indicate that the data addition operation was successful.
"data" (Optional): Represents the response data. In this case, it is set to null, indicating that no specific data is returned in response to the addition of a new record.

### JSON Payload printName (Retrieve):

Response Payload:
"status" (Required): Indicates the status of the operation. It is set to "success" to indicate that the data retrieval operation was successful.
"data" (Required): Represents the response data. It is an array containing multiple objects, each representing a person's last name ("lname") and first name ("fname"). This field contains the retrieved data from the database.

### JSON Payload updateName (Update):

Response Payload:
"status" (Required): Indicates the status of the operation. In this case, it is set to "success" to indicate that the data update operation was successful.
"data" (Optional): Represents the response data. In this case, it is set to null, indicating that no specific data is returned in response to the update.

### JSON Payload deleteName (Delete):

Response Payload:
"status" (Required): Indicates the status of the operation. In this case, it is set to "success" to indicate that the data deletion operation was successful.
"data" (Optional): Represents the response data. It is set to null, indicating that no specific data is returned in response to the deletion.

## Usage

### Here's how you can use Postman to interact with this API:

### Create a New Request:

Open Postman and create a new request by clicking the "New" button and selecting "Request."

Set Request Type and URL:

Choose the HTTP method (POST, GET, PUT, DELETE) based on the operation you want to perform.
Enter the API URL, including the endpoint you want to access (e.g., http://localhost/api/postName).
Add Headers (if required):

### add Request Payload:

If you're making a POST or PUT request to add or update data, go to the "Body" tab.
Select "raw" and choose the data format (usually JSON).
Enter the JSON payload in the request body.

### Send the Request:

Click the "Send" button to execute the API request.

### View the Response:

Postman will display the API's response in the lower part of the window. You can see the HTTP status code, response headers, and the response body, which typically contains the API's response data.

### Test Other Endpoints:

You can repeat the above steps with different endpoints (postPrint, postUpdate, postDelete) and payloads as needed.

## License

No license.
For educational Purposes Only

## Contributor/s

### Sir Manny Hortizuela

provided:

- some codes
- database structure
- payloads
- etc.

## Contact Information

information for inquiries or support.

### Charles Andrei Aspuria - 4B

charlesandrei.aspuria@student.dmmmsu.edu.ph
