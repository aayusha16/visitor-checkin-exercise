Visitor Check In Test Cases

TC 001: Verify Visitor Check In page loads

Precondition

Application is running

Steps

1. Open the Visitor Check In page
2. Check the page

Expected Result

Visitor Check In page is displayed with Register Visitor form and Active Visitors section

TC 002: Verify all registration fields are displayed

Precondition

Visitor Check In page is open

Steps

1. Check the Register Visitor form

Expected Result

Full Name field is displayed
Company field is displayed
Host field is displayed
Purpose field is displayed
Submit button is displayed

TC 003: Register visitor with valid information

Precondition

Visitor Check In page is open

Steps

1. Enter a valid full name
2. Enter a company name
3. Select a host
4. Enter a purpose
5. Click Submit

Test Data

Full Name: John Doe
Company: ABC Company
Host: Available Host
Purpose: Business Meeting

Expected Result

Visitor is registered successfully and appears in the Active Visitors list

TC 004: Verify Full Name is required

Precondition

Visitor Check In page is open

Steps

1. Leave Full Name empty
2. Enter valid Company
3. Select a valid Host
4. Enter valid Purpose
5. Click Submit

Expected Result

Validation message is displayed and visitor is not registered

TC 005: Verify Company is required

Precondition

Visitor Check In page is open

Steps

1. Enter a valid Full Name
2. Leave Company empty
3. Select a valid Host
4. Enter valid Purpose
5. Click Submit

Expected Result

Validation message is displayed and visitor is not registered

TC 006: Verify Host is required

Precondition

Visitor Check In page is open

Steps

1. Enter a valid Full Name
2. Enter a valid Company
3. Do not select a Host
4. Enter valid Purpose
5. Click Submit

Expected Result

Validation message is displayed and visitor is not registered

TC 007: Verify Purpose is required

Precondition

Visitor Check In page is open

Steps

1. Enter a valid Full Name
2. Enter a valid Company
3. Select a valid Host
4. Leave Purpose empty
5. Click Submit

Expected Result

Validation message is displayed and visitor is not registered

TC 008: Verify valid Full Name is accepted

Precondition

Visitor Check In page is open

Steps

1. Enter John Doe in Full Name
2. Enter valid information in the other fields
3. Click Submit

Expected Result

Valid Full Name is accepted and visitor is registered

TC 009: Verify single character Full Name

Precondition

Visitor Check In page is open

Steps

1. Enter A in Full Name
2. Enter valid information in the other fields
3. Click Submit

Expected Result

Application should validate the Full Name according to the defined business rule

TC 010: Verify numeric only Full Name

Precondition

Visitor Check In page is open

Steps

1. Enter 123456 in Full Name
2. Enter valid information in the other fields
3. Click Submit

Expected Result

Application should handle numeric only Full Name according to the defined business rule

TC 011: Verify special characters in Full Name

Precondition

Visitor Check In page is open

Steps

1. Enter special characters in Full Name
2. Enter valid information in the other fields
3. Click Submit

Expected Result

Application should handle special characters according to the defined business rule

TC 012: Verify Full Name with spaces

Precondition

Visitor Check In page is open

Steps

1. Enter a name with spaces before and after the name
2. Enter valid information in the other fields
3. Click Submit

Expected Result

Application handles the spaces correctly and does not create an invalid visitor record

TC 013: Verify long Full Name

Precondition

Visitor Check In page is open

Steps

1. Enter a very long name in Full Name
2. Enter valid information in the other fields
3. Click Submit

Expected Result

Application handles the long name correctly without breaking the form or page

TC 014: Verify Host dropdown

Precondition

Visitor Check In page is open

Steps

1. Click the Host dropdown

Expected Result

Available hosts are displayed in the dropdown

TC 015: Verify host can be selected

Precondition

Visitor Check In page is open

Steps

1. Click the Host dropdown
2. Select an available host

Expected Result

Selected host is displayed in the Host field

TC 016: Verify visitor information after registration

Precondition

Visitor was registered successfully

Steps

1. Check the Active Visitors list
2. Find the registered visitor

Expected Result

Visitor name, company, host and purpose are displayed correctly

TC 017: Verify check in time is displayed

Precondition

Visitor was registered successfully

Steps

1. Check the Active Visitors list
2. Check the Checked In column

Expected Result

Check in time is displayed for the visitor

TC 018: Verify check in time uses local timezone

Precondition

Visitor was registered successfully

Steps

1. Register a visitor
2. Check the displayed check in time
3. Compare it with the receptionist local time

Expected Result

Check in time is displayed according to the receptionist local timezone

TC 019: Verify new visitor appears in Active Visitors

Precondition

Visitor was registered successfully

Steps

1. Register a new visitor
2. Check the Active Visitors list

Expected Result

New visitor is displayed in the Active Visitors list

TC 020: Verify visitor can be checked out

Precondition

At least one active visitor is available

Steps

1. Find an active visitor
2. Click the checkout action

Expected Result

Visitor is checked out successfully

TC 021: Verify checked out visitor is removed from Active Visitors

Precondition

Visitor was checked out

Steps

1. Refresh the page
2. Check the Active Visitors list

Expected Result

Checked out visitor is not displayed in the Active Visitors list

TC 022: Verify active visitor information is correct

Precondition

At least one visitor is active

Steps

1. Check the Active Visitors table
2. Compare the visitor details with the registered information

Expected Result

Displayed visitor information matches the registered information

TC 023: Verify deactivated visitor is not shown in Active Visitors

Precondition

A visitor record is available and can be deactivated

Steps

1. Deactivate the visitor
2. Open or refresh the Visitor Check In page
3. Check the Active Visitors list

Expected Result

Deactivated visitor is not displayed in the Active Visitors list

TC 024: Verify deactivated visitor cannot be selected for repeat visit

Precondition

A visitor has been deactivated

Steps

1. Try to register the deactivated visitor again
2. Check the available visitor records

Expected Result

Deactivated visitor cannot be selected for a repeat visit

TC 025: Verify Active Visitors list is empty when there are no active visitors

Precondition

There are no active visitors

Steps

1. Open the Visitor Check In page
2. Check the Active Visitors section

Expected Result

No active visitor records are displayed

TC 026: Verify Active Visitors pagination

Precondition

More than 20 active visitors are available

Steps

1. Open the Active Visitors list
2. Check the number of visitors displayed on the first page

Expected Result

Maximum 20 active visitors are displayed on one page

TC 027: Verify Next button

Precondition

More than 20 active visitors are available

Steps

1. Open the Active Visitors list
2. Click Next

Expected Result

Next page of active visitors is displayed

TC 028: Verify Previous button

Precondition

More than 20 active visitors are available

Steps

1. Go to the next page
2. Click Previous

Expected Result

Previous page of active visitors is displayed

TC 029: Verify Previous button on first page

Precondition

Visitor Check In page is open

Steps

1. Check the pagination controls
2. Stay on the first page

Expected Result

Previous button is disabled because the user is already on the first page

TC 030: Verify Next button on last page

Precondition

More than 20 active visitors are available

Steps

1. Go to the last page of Active Visitors
2. Check the pagination controls

Expected Result

Next button is disabled because there are no more pages



#API Test Cases

TC 031: Verify Visitors API returns visitor records

Precondition

Application API is running

Steps

1 Open Postman
2 Send a GET request to `/api/visitors'

Expected Result

API returns a successful response and the visitor records are displayed


TC 032: Verify Visitors API response status code

Precondition

Application API is running

Steps

1. Open Postman
2. Send a GET request to `/api/visitors'
3. Check the response status code

Expected Result

API returns HTTP 200 status code


TC 033: Create visitor using valid information through API

Precondition

Application API is running

Steps

1. Open Postman
2. Create a POST request to `/api/visitors`
3. Add valid visitor information in the request body
4. Send the request

Expected Result

Visitor is created successfully and the API returns the created visitor information


TC 034: Verify visitor creation with missing Full Name

Precondition

Application API is running

Steps

1. Open Postman
2. Create a POST request to `/api/visitors`
3. Leave Full Name empty or omit the field
4. Provide valid values for the other required fields
5. Send the request

Expected Result

API rejects the request and returns an appropriate validation error


TC 035: Verify visitor creation with missing Company

Precondition

Application API is running

Steps

1 Open Postman
2 Create a POST request to `/api/visitors`
3 Leave Company empty or omit the field
4 Provide valid values for the other required fields
5 Send the request

Expected Result

API rejects the request and returns an appropriate validation error


TC 036: Verify visitor creation with missing Host

Precondition

Application API is running

Steps

1 Open Postman
2 Create a POST request to `/api/visitors'
3 Leave Host empty or omit the field
4 Provide valid values for the other required fields
5 Send the request

Expected Result

API rejects the request and returns an appropriate validation error


TC 037: Verify visitor creation with missing Purpose

Precondition

Application API is running

Steps

1 Open Postman
2 Create a POST request to `/api/visitors'
3 Leave Purpose empty or omit the field   
4 Provide valid values for the other required fields
5 Send the request

Expected Result

API rejects the request and returns an appropriate validation error


TC 038: Verify single character Full Name through API

Precondition

Application API is running

Steps

1 Open Postman
2 Create a POST request to `/api/visitors'
3 Enter `A' as the Full Name
4 Provide valid values for the other fields
5 Send the request

Expected Result

API validates the Full Name according to the defined business rule


TC 039: Verify whitespace-only Full Name through API

Precondition

Application API is running

Steps

1 Open Postman
2 Create a POST request to `/api/visitors'
3 Enter only spaces in the Full Name field
4 Provide valid values for the other fields
5 Send the request

Expected Result

API rejects the whitespace-only Full Name and returns an appropriate validation error


TC 040: Verify numeric-only Full Name through API

Precondition

Application API is running

Steps

1 Open Postman
2 Create a POST request to `/api/visitors'
3 Enter `123456' as the Full Name
4 Provide valid values for the other fields
5 Send the request

Expected Result

API handles the numeric-only Full Name according to the defined business rule


TC 041: Verify extremely long Full Name through API

Precondition

Application API is running

Steps

1 Open Postman
2 Create a POST request to `/api/visitors'
3 Enter an extremely long value in the Full Name field
4 Provide valid values for the other fields
5 Send the request

Expected Result

API handles the long input safely without a server error or malformed response


TC 042: Verify duplicate visitor registration through API

Precondition

A visitor with the same information already exists

Steps

1 Open Postman
2 Create a POST request to `/api/visitors'
3 Submit the same visitor information again
4 Send the request

Expected Result

API handles duplicate visitor registration according to the defined business rule


TC 043: Verify visitor search API

Precondition

Application API is running and visitor records are available

Steps

1 Open Postman
2 Send a GET request to `/api/visitors/search'
3 Provide a valid search query
4 Send the request

Expected Result

API returns visitor records matching the search criteria


TC 044: Verify search for non-existing visitor

Precondition

Application API is running

Steps

1 Open Postman
2 Send a GET request to `/api/visitors/search'
3 Provide a search value that does not exist
4 Send the request

Expected Result

API returns an empty result or appropriate response indicating that no matching visitor was found


TC 045: Verify visitor check out through API

Precondition

An active visitor exists

Steps

1 Open Postman
2 Identify the visitor ID
3 Send a PATCH request to `/api/visitors/:id/check_out'
4 Replace `:id' with the visitor ID
5 Send the request

Expected Result

Visitor is successfully checked out and the API returns an appropriate response


TC 046: Verify check out of non-existing visitor

Precondition

Application API is running

Steps

1 Open Postman
2 Send a PATCH request to `/api/visitors/:id/check_out'
3 Use a non-existing visitor ID
4 Send the request

Expected Result

API returns an appropriate 4xx error response


TC 047: Verify already checked out visitor

Precondition

A visitor has already been checked out

Steps

1 Open Postman
2 Send a PATCH request to `/api/visitors/:id/check_out'
3 Use the ID of the already checked out visitor
4 Send the request

Expected Result

API handles the request appropriately and does not create an invalid visitor state


TC 048: Verify visitor deactivation through API

Precondition

An active visitor exists

Steps

1 Open Postman
2 Identify the visitor ID
3 Send a PATCH request to `/api/visitors/:id/deactivate'
4 Replace `:id' with the visitor ID
5 Send the request

Expected Result

Visitor is successfully deactivated and the API returns an appropriate response


TC 049: Verify deactivation of non-existing visitor

Precondition

Application API is running

Steps

1 Open Postman
2 Send a PATCH request to `/api/visitors/:id/deactivate'
3 Use a non-existing visitor ID
4 Send the request

Expected Result

API returns an appropriate 4xx error response


TC 050: Verify already deactivated visitor

Precondition

A visitor has already been deactivated

Steps

1 Open Postman
2 Send a PATCH request to `/api/visitors/:id/deactivate'
3 Use the ID of the already deactivated visitor
4 Send the request

Expected Result

API handles the request appropriately and does not create an invalid visitor state


TC 051: Verify Hosts API

Precondition

Application API is running

Steps

1 Open Postman
2 Send a GET request to `/api/hosts'

Expected Result

API returns a successful response containing the available hosts


TC 052: Verify Hosts API response status code

Precondition

Application API is running

Steps

1 Open Postman
2 Send a GET request to `/api/hosts'
3 Check the response status code

Expected Result

API returns HTTP 200 status code


TC 053: Verify invalid visitor endpoint

Precondition

Application API is running

Steps

1 Open Postman
2 Send a GET request to an invalid visitor endpoint
3 Send the request

Expected Result

API returns an appropriate 4xx error response


TC 054: Verify invalid visitor ID during check out

Precondition

Application API is running

Steps

1 Open Postman
2 Send a PATCH request to `/api/visitors/:id/check_out'
3 Use an invalid visitor ID
4 Send the request

Expected Result

API handles the invalid ID appropriately and does not return an unexpected server error


TC 055: Verify invalid visitor ID during deactivation

Precondition

Application API is running

Steps

1 Open Postman
2 Send a PATCH request to `/api/visitors/:id/deactivate'
3 Use an invalid visitor ID
4 Send the request

Expected Result

API handles the invalid ID appropriately and does not return an unexpected server error