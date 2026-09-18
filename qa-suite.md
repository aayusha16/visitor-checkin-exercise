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
