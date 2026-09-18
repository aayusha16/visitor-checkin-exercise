#Visitor Check In Test Cases

#TC 001: Verify Visitor Check In page loads

Category: Happy Path

Precondition

Application is running.

Steps

1 Confirm the application is running.
2 Check the Visitor Check In page.

Expected Result

Visitor Check In page is displayed with Register Visitor form and Active Visitors section.

Execution Result: [ Pass]



#TC 002: Verify all registration fields are displayed

Category: Happy Path

Precondition

Visitor Check In page is open.

Steps

1 Check the Register Visitor form.
2 Confirm Full Name field is displayed.
3 Confirm Company field is displayed.
4 Confirm Host field is displayed.
5 Confirm Purpose field is displayed.
6 Confirm Submit button is displayed.

Expected Result

Full Name, Company, Host, Purpose fields and Submit button are displayed.

Execution Result: [Pass ]


#TC 003: Verify visitor can be registered with valid information

Category: Happy Path

Precondition

Visitor Check In page is open.

Steps

1 Confirm a valid full name is entered.
2 Confirm a valid company name is entered.
3 Confirm a valid host is selected.
4 Confirm a valid purpose is entered.
5 Check that the Submit button is clicked.

Test Data

Full Name: Michael Scofield
Company: ABC Company
Host: Available Host
Purpose: Business Meeting

Expected Result

Visitor is registered successfully and appears in the Active Visitors list.

Execution Result: [Pass ]


#TC 004: Verify Full Name is required

Category:Negative

Precondition

Visitor Check In page is open.

Steps

1 Confirm Full Name is left empty.
2 Confirm valid Company is entered.
3 Confirm a valid Host is selected.
4 Confirm valid Purpose is entered.
5 Check that the Submit button is clicked.

Expected Result

Validation message is displayed and visitor is not registered.

Execution Result: [ Pass]

#TC 005: Verify Company is required

Category: Negative

Precondition

Visitor Check In page is open.

Steps

1 Confirm a valid Full Name is entered.
2 Confirm Company is left empty.
3 Confirm a valid Host is selected.
4 Confirm valid Purpose is entered.
5 Check that the Submit button is clicked.

Expected Result

Validation message is displayed and visitor is not registered.

Execution Result: [ Fail]


#TC 006: Verify Host is required

Category: Negative

Precondition

Visitor Check In page is open.

Steps

1 Confirm a valid Full Name is entered.
2 Confirm a valid Company is entered.
3 Confirm no Host is selected.
4 Confirm valid Purpose is entered.
5 Check that the Submit button is clicked.

Expected Result

Validation message is displayed and visitor is not registered.

Execution Result: [Pass ]


#TC 007: Verify Purpose is required

Category: Negative

Precondition

Visitor Check In page is open.

Steps

1 Confirm a valid Full Name is entered.
2 Confirm a valid Company is entered.
3 Confirm a valid Host is selected.
4 Confirm Purpose is left empty.
5 Check that the Submit button is clicked.

Expected Result

Validation message is displayed and visitor is not registered.

Execution Result: [ Fail]

#TC 008: Verify valid Full Name is accepted

Category: Happy Path

Precondition

Visitor Check In page is open.

Steps

1 Confirm `Michael Scofield' is entered in Full Name.
2 Confirm valid information is entered in the other fields.
3 Check that the Submit button is clicked.

Expected Result

Valid Full Name is accepted and visitor is registered.

Execution Result: [ Pass]


#TC 009: Verify single character Full Name

Category: Boundary

Precondition

Visitor Check In page is open.

Steps

1 Confirm `A' is entered in Full Name.
2 Confirm valid information is entered in the other fields.
3 Check that the Submit button is clicked.

Expected Result

Application should validate the Full Name according to the defined business rule.

Execution Result: [ Pass]


#TC 010: Verify numeric only Full Name

Category: Negative

Precondition

Visitor Check In page is open.

Steps

1 Confirm `123456' is entered in Full Name.
2 Confirm valid information is entered in the other fields.
3 Check that the Submit button is clicked.

Expected Result

Application should handle numeric-only Full Name according to the defined business rule.

Execution Result:[Pass ]


#TC 011: Verify special characters in Full Name

Category: Negative

Precondition

Visitor Check In page is open.

Steps

1 Confirm special characters are entered in Full Name.
2 Confirm valid information is entered in the other fields.
3 Check that the Submit button is clicked.

Expected Result

Application should handle special characters according to the defined business rule.

Execution Result:[ Pass]


#TC 012: Verify Full Name with spaces

Category: Boundary

Precondition

Visitor Check In page is open.

Steps

1 Confirm a name with spaces before and after the name is entered.
2 Confirm valid information is entered in the other fields.
3 Check that the Submit button is clicked.

Expected Result

Application handles the spaces correctly and does not create an invalid visitor record.

Execution Result: [ Pass]


#TC 013: Verify long Full Name

Category: Boundary

Precondition

Visitor Check In page is open.

Steps

1 Confirm a very long name is entered in Full Name.
2 Confirm valid information is entered in the other fields.
3 Check that the Submit button is clicked.

Expected Result

Application handles the long name correctly without breaking the form or page.

Execution Result: [ Fail]

#TC 014: Verify Host dropdown

Category: Happy Path

Precondition

Visitor Check In page is open.

Steps

1 Check the Host dropdown.
2 Confirm the dropdown can be opened.

Expected Result

Available hosts are displayed in the dropdown.

Execution Result: [ Pass]


#TC 015: Verify host can be selected

Category: Happy Path

Precondition

Visitor Check In page is open.

Steps

1 Check the Host dropdown.
2 Confirm an available host is selected.

Expected Result

Selected host is displayed in the Host field.

Execution Result: [ Pass]


#TC 016: Verify visitor information after registration

Category:Happy Path

Precondition

Visitor was registered successfully.

Steps

1 Check the Active Visitors list.
2 Confirm the registered visitor is displayed.
3 Check the visitor details.

Expected Result

Visitor name, company, host and purpose are displayed correctly.

Execution Result: [ Pass]


#TC 017: Verify check in time is displayed

Category: Happy Path

Precondition

Visitor was registered successfully.

Steps

1 Check the Active Visitors list.
2 Check the Checked In column.
3 Confirm a check-in time is displayed.

Expected Result

Check-in time is displayed for the visitor.

Execution Result: [ Pass]


#TC 018: Verify check in time uses local timezone

Category: Boundary

Precondition

Visitor was registered successfully.

Steps

1 Confirm a visitor is registered.
2 Check the displayed check-in time.
3 Check the receptionist's local time.
4 Confirm both times are compared.

Expected Result

Check-in time is displayed according to the receptionist's local timezone.

**Execution Result: [ Fail]


#TC 019: Verify new visitor appears in Active Visitors

Category: Happy Path

Precondition

Visitor Check In page is open.

Steps

1 Confirm valid visitor information is entered.
2 Check that the Submit button is clicked.
3 Check the Active Visitors list.
4 Confirm the new visitor is displayed.

Expected Result

New visitor is displayed in the Active Visitors list.

Execution Result: [Pass ]


#TC 020: Verify visitor can be checked out

Category:Happy Path

Precondition

At least one active visitor is available.

Steps

1 Check the Active Visitors list.
2 Confirm an active visitor is available.
3 Check that the checkout action is clicked.

Expected Result

Visitor is checked out successfully.

Execution Result: [ Pass]


#TC 021: Verify checked out visitor is removed from Active Visitors

Category: Happy Path

Precondition

Visitor was checked out.

Steps

1 Confirm the visitor has been checked out.
2 Check or refresh the Active Visitors list.
3 Confirm the checked-out visitor is not displayed.

Expected Result

Checked-out visitor is not displayed in the Active Visitors list.

Execution Result: [Pass ]

#TC 022: Verify active visitor information is correct

Category: Happy Path

Precondition

At least one visitor is active.

Steps

1 Check the Active Visitors table.
2 Confirm the visitor details are displayed.
3 Check the displayed details against the registered information.

Expected Result

Displayed visitor information matches the registered information.

Execution Result:[ Pass]


#TC 023: Verify deactivated visitor is not shown in Active Visitors

Category: Negative

Precondition

A visitor record is available and can be deactivated.

Steps

1 Confirm the visitor is deactivated.
2 Check or refresh the Visitor Check In page.
3 Check the Active Visitors list.

Expected Result

Deactivated visitor is not displayed in the Active Visitors list.

Execution Result: [ Fail]


#TC 024: Verify deactivated visitor cannot be selected for repeat visit

Category: Negative

Precondition

A visitor has been deactivated.

Steps

1 Confirm the visitor has been deactivated.
2 Check the available visitor records.
3 Confirm whether the deactivated visitor can be selected for a repeat visit.

Expected Result

Deactivated visitor cannot be selected for a repeat visit.

Execution Result: [Fail ]


#TC 025: Verify Active Visitors list is empty when there are no active visitors

Category: Boundary

Precondition

There are no active visitors.

Steps

1 Confirm there are no active visitor records.
2 Check the Visitor Check In page.
3 Check the Active Visitors section.

Expected Result

No active visitor records are displayed.

Execution Result: [ Pass]

#TC 026: Verify Active Visitors pagination

Category: Boundary

Precondition

More than 20 active visitors are available.

Steps

1 Confirm more than 20 active visitors are available.
2 Check the Active Visitors list.
3 Check the number of visitors displayed on the first page.

Expected Result

Maximum 20 active visitors are displayed on one page.

Execution Result: [ Pass]


TC 027: Verify Next button

Category: Happy Path

Precondition

More than 20 active visitors are available.

Steps

1 Confirm more than 20 active visitors are available.
2 Check the Active Visitors list.
3 Confirm the Next button is available.
4 Check that the Next button is clicked.

Expected Result

Next page of active visitors is displayed.

Execution Result: [ Pass]


#TC 028: Verify Previous button

Category: Happy Path

Precondition

More than 20 active visitors are available and the user is on a page after the first page.

Steps

1 Confirm the user is on a page after the first page.
2 Check the pagination controls.
3 Check that the Previous button is clicked.

Expected Result

Previous page of active visitors is displayed.

Execution Result: [ Pass]


#TC 029: Verify Previous button on first page

Category: Boundary

Precondition

Visitor Check In page is open and the Active Visitors list is on the first page.

Steps

1 Confirm the Active Visitors list is on the first page.
2 Check the pagination controls.
3 Check the Previous button.

Expected Result

Previous button is disabled because the user is already on the first page.

Execution Result:[ Pass]


#TC 030: Verify Next button on last page

Category:Boundary

Precondition

Active Visitors list is on the last page.

Steps

1 Confirm the Active Visitors list is on the last page.
2 Check the pagination controls.
3 Check the Next button.

Expected Result

Next button is disabled because there are no more pages.

Execution Result: [Pass ]


 API Test Cases

TC 031: Verify Visitors API returns visitor records

Category: Happy Path

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is GET.
3 Confirm the endpoint is `/api/visitors'.
4 Check the response.

Expected Result

API returns a successful response and visitor records are displayed.

Execution Result: [ ]


#TC 032: Verify Visitors API response status code

Category: Happy Path

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is GET.
3 Confirm the endpoint is `/api/visitors'.
4 Send the request.
5 Check the response status code.

Expected Result

API returns HTTP 200 status code.

Execution Result: [ Pass]


 TC 033: Verify visitor can be created using valid information through API

Category: Happy Path

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm valid visitor information is included in the request body.
5 Send the request.
6 Check the response.

Expected Result

Visitor is created successfully and the API returns the created visitor information.

Execution Result: [ Pass]


#TC 034: Verify visitor creation with missing Full Name

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm Full Name is empty or omitted.
5 Confirm valid values are provided for the other required fields.
6 Send the request.
7 Check the response.

Expected Result

API rejects the request and returns an appropriate validation error.

Execution Result: [ Fail]


#TC 035: Verify visitor creation with missing Company

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm Company is empty or omitted.
5 Confirm valid values are provided for the other required fields.
6 Send the request.
7 Check the response.

Expected Result

API rejects the request and returns an appropriate validation error.

Execution Result: [ Fail]


#TC 036: Verify visitor creation with missing Host

Category:Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm Host is empty or omitted.
5 Confirm valid values are provided for the other required fields.
6 Send the request.
7 Check the response.

Expected Result

API rejects the request and returns an appropriate validation error.

Execution Result: [ Fail]


#TC 037: Verify visitor creation with missing Purpose

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm Purpose is empty or omitted.
5 Confirm valid values are provided for the other required fields.
6 Send the request.
7 Check the response.

Expected Result

API rejects the request and returns an appropriate validation error.

Execution Result: [ Fail]


#TC 038: Verify single character Full Name through API

Category: Boundary

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm `A' is entered as the Full Name.
5 Confirm valid values are provided for the other fields.
6 Send the request.
7 Check the response.

Expected Result

API validates the Full Name according to the defined business rule.

Execution Result:[ Fail]


#TC 039: Verify whitespace-only Full Name through API

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm only spaces are entered in the Full Name field.
5 Confirm valid values are provided for the other fields.
6 Send the request.
7 Check the response.

Expected Result

API rejects the whitespace-only Full Name and returns an appropriate validation error.

Execution Result: [ Fail]


#TC 040: Verify numeric-only Full Name through API

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm `123456' is entered as the Full Name.
5 Confirm valid values are provided for the other fields.
6 Send the request.
7 Check the response.

Expected Result

API handles the numeric-only Full Name according to the defined business rule.

Execution Result: [ Pass]


#TC 041: Verify extremely long Full Name through API

Category: Boundary

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm an extremely long value is entered in the Full Name field.
5 Confirm valid values are provided for the other fields.
6 Send the request.
7 Check the response.

Expected Result

API handles the long input safely without a server error or malformed response.

Execution Result: [ Pass]


#TC 042: Verify duplicate visitor registration through API

Category: Negative

Precondition

A visitor with the same information already exists.

Steps

1 Open Postman.
2 Confirm the request method is POST.
3 Confirm the endpoint is `/api/visitors'.
4 Confirm the same visitor information is included in the request body.
5 Send the request.
6 Check the response.

Expected Result

API handles duplicate visitor registration according to the defined business rule.

Execution Result: [Fail ]

#TC 043: Verify visitor search API

Category: Happy Path

Precondition

Application API is running and visitor records are available.

Steps

1 Open Postman.
2 Confirm the request method is GET.
3 Confirm the endpoint is `/api/visitors/search'.
4 Confirm a valid search query is provided.
5 Send the request.
6 Check the response.

Expected Result

API returns visitor records matching the search criteria.

Execution Result: [Pass ]


#TC 044: Verify search for non-existing visitor

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is GET.
3 Confirm the endpoint is `/api/visitors/search'.
4 Confirm a search value that does not exist is provided.
5 Send the request.
6 Check the response.

Expected Result

API returns an empty result or appropriate response indicating that no matching visitor was found.

Execution Result:[Pass ]


#TC 045: Verify visitor check out through API

Category: Happy Path

Precondition

An active visitor exists.

Steps

1 Open Postman.
2 Confirm an active visitor ID is available.
3 Confirm the request method is PATCH.
4 Confirm the endpoint is `/api/visitors/:id/check_out'.
5 Replace `:id' with the active visitor ID.
6 Send the request.
7 Check the response.

Expected Result

Visitor is successfully checked out and the API returns an appropriate response.

Execution Result:[ Pass]


#TC 046: Verify check out of non-existing visitor

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is PATCH.
3 Confirm the endpoint is `/api/visitors/:id/check_out'.
4 Confirm a non-existing visitor ID is used.
5 Send the request.
6 Check the response status code.

Expected Result

API returns an appropriate 4xx error response.

Execution Result: [Pass ]


#TC 047: Verify already checked out visitor

Category: Negative

Precondition

A visitor has already been checked out.

Steps

1 Open Postman.
2 Confirm the visitor has already been checked out.
3 Confirm the request method is PATCH.
4 Confirm the endpoint is `/api/visitors/:id/check_out'.
5 Confirm the ID of the already checked-out visitor is used.
6 Send the request.
7 Check the response.

Expected Result

API handles the request appropriately and does not create an invalid visitor state.

Execution Result: [ Pass]


#TC 048: Verify visitor deactivation through API

Category: Happy Path

Precondition

An active visitor exists.

Steps

1 Open Postman.
2 Confirm an active visitor ID is available.
3 Confirm the request method is PATCH.
4 Confirm the endpoint is `/api/visitors/:id/deactivate'.
5 Replace `:id' with the visitor ID.
6 Send the request.
7 Check the response.

Expected Result

Visitor is successfully deactivated and the API returns an appropriate response.

Execution Result: [Fail ]


#TC 049: Verify deactivation of non-existing visitor

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is PATCH.
3 Confirm the endpoint is `/api/visitors/:id/deactivate'.
4 Confirm a non-existing visitor ID is used.
5 Send the request.
6 Check the response status code.

Expected Result

API returns an appropriate 4xx error response.

Execution Result: [ Fail]


#TC 050: Verify already deactivated visitor

Category: Negative

Precondition

A visitor has already been deactivated.

Steps

1 Open Postman.
2 Confirm the visitor has already been deactivated.
3 Confirm the request method is PATCH.
4 Confirm the endpoint is `/api/visitors/:id/deactivate'.
5 Confirm the ID of the already deactivated visitor is used.
6 Send the request.
7 Check the response.

Expected Result

API handles the request appropriately and does not create an invalid visitor state.

Execution Result:[ Fail]


#TC 051: Verify Hosts API

Category: Happy Path

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is GET.
3 Confirm the endpoint is `/api/hosts'.
4 Send the request.
5 Check the response.

Expected Result

API returns a successful response containing the available hosts.

Execution Result:[ Pass]


#TC 052: Verify Hosts API response status code

Category:Happy Path

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is GET.
3 Confirm the endpoint is `/api/hosts'.
4 Send the request.
5 Check the response status code.

Expected Result

API returns HTTP 200 status code.

Execution Result: [ Pass]


#TC 053: Verify invalid visitor endpoint

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm an invalid visitor endpoint is entered.
3 Confirm the request is sent.
4 Check the response status code.

Expected Result

API returns an appropriate 4xx error response.

Execution Result: [ Pass]


#TC 054: Verify invalid visitor ID during check out

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is PATCH.
3 Confirm the endpoint is `/api/visitors/:id/check_out'.
4 Confirm an invalid visitor ID is used.
5 Send the request.
6 Check the response.

Expected Result

API handles the invalid ID appropriately and does not return an unexpected server error.

Execution Result: [ ]


#TC 055: Verify invalid visitor ID during deactivation

Category: Negative

Precondition

Application API is running.

Steps

1 Open Postman.
2 Confirm the request method is PATCH.
3 Confirm the endpoint is `/api/visitors/:id/deactivate'.
4 Confirm an invalid visitor ID is used.
5 Send the request.
6 Check the response.
Expected Result

API handles the invalid ID appropriately and does not return an unexpected server error.

Execution Result: [ Pass]
