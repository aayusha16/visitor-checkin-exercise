Defect 1

Summary: Missing checkout success message

Type: Usability

Description:
When a receptionist checks out a visitor, the system does not display a confirmation message. This may leave the receptionist uncertain whether the checkout action was completed successfully.

Steps to Reproduce:

Log in as a receptionist.
Register a visitor.
Click Check Out for the visitor.
Observe the page after checkout.

Expected Result:
A confirmation message such as Checkout successful should be displayed after the visitor is checked out.

Actual Result:
No confirmation message is displayed. The visitor list updates silently.

Defect 2

Summary: Missing registration success message

Type: Usability

Description:
After registering a visitor, the system does not display a confirmation message. This may leave the receptionist uncertain whether the registration was completed successfully.

Steps to Reproduce:

Log in as a receptionist.
Enter valid visitor details.
Submit the registration form.
Observe the page after registration.

Expected Result:
A confirmation message such as Registration successful should be displayed after the visitor is registered.

Actual Result:
No confirmation message is displayed. The visitor list updates silently.

Defect 3

Summary: Full Name field accepts invalid input

Type: Data

Description:
The Full Name field accepts invalid values such as numbers, special characters, whitespace only input, and excessively long names.

Steps to Reproduce:

Open the Visitor Check in page.
Enter an invalid value in the Full Name field, such as 1234 or special characters.
Alternatively, enter a whitespace only value or an excessively long name.
Submit the registration form.

Expected Result:
The system should validate the Full Name field and reject invalid input. Appropriate validation should be applied for characters, whitespace, and maximum length.

Actual Result:
The system accepts the invalid input and allows the registration to proceed.

Defect 4

Summary: Company Name field accepts invalid input

Type: Data

Description:
The Company Name field accepts invalid values such as special characters, numbers, whitespace only input, and excessively long company names.

Steps to Reproduce:

Open the Visitor Check in page.
Enter an invalid value in the Company Name field, such as %%%%.
Alternatively, enter a whitespace only value or an excessively long company name.
Submit the registration form.

Expected Result:
The system should validate the Company Name field and reject invalid input according to the required validation rules.

Actual Result:
The system accepts the invalid input and allows the registration to proceed.

Defect 5

Summary: Extremely long visitor name causes UI layout overflow

Type: Usability

Description:
The Full Name field accepts an extremely long value. When the field is interacted with again, the long value extends beyond the intended area and causes visual distortion in the registration form and Active Visitors section.

Steps to Reproduce:

Open the Visitor Check in page.
Locate the Full Name field.
Enter an extremely long string in the Full Name field.
Confirm that the value is accepted.
Click the Full Name field again.
Observe the registration form and Active Visitors section.

Expected Result:
The page layout should remain intact when an extremely long name is entered. The content should remain within the intended area without affecting other elements.

Actual Result:
The extremely long visitor name extends beyond the intended area and causes the page layout to become visually distorted.

Defect 6

Summary: Duplicate visitor registration is allowed

Type: Functional

Description:
The system allows the same visitor details to be registered multiple times while the previous visitor record is still active.

Steps to Reproduce:

Log in as a receptionist.
Register a visitor using valid details.
Do not check out the visitor.
Register another visitor using the same details.
Observe the Active Visitors list.

Expected Result:
The system should prevent duplicate active registrations or notify the receptionist that the visitor already has an active visit.

Actual Result:
The system allows the same visitor to be registered multiple times and creates duplicate active visitor records.

Defect 7

Summary: Check in time does not match the receptionist local timezone

Type: Data

Description:
The check in time displayed for a visitor does not match the receptionist local timezone.

Steps to Reproduce:

Open the Visitor Check in page.
Register a visitor.
Note the check in time displayed in the Active Visitors list.
Compare the displayed time with the receptionist local time in Kathmandu.

Expected Result:
The check in time should be displayed according to the receptionist local timezone.

Actual Result:
The displayed check in time does not match the receptionist local timezone.

Defect 8

Summary: Inconsistent required field validation

Type: Functional

Description:
Both Full Name and Host fields are marked as required. However, when both fields are left empty and the form is submitted, validation is displayed only for the Full Name field.

Steps to Reproduce:

Open the Visitor Check in page.
Leave the Full Name field empty.
Leave the Host field empty.
Submit the registration form.
Observe the validation messages.

Expected Result:
Both required fields should display appropriate validation when they are left empty.

Actual Result:
Only the Full Name field displays a required field validation message. The Host field does not display the expected validation message.

Defect 9

Summary: Deactivation is not restricted to administrators

Type: Functional

Description:
The visitor deactivation functionality can be accessed by a receptionist through the API even though the functionality should be restricted to administrators.

Steps to Reproduce:

Log in or authenticate as a receptionist.
Check the available routes using the Rails routes command.
Identify the visitor deactivation route.
Using Postman, send a PATCH request to the visitor deactivation endpoint.
Observe the response.

Expected Result:
Only administrators should be authorized to deactivate visitors. A receptionist should receive a Forbidden response.

Actual Result:
A receptionist can successfully deactivate a visitor through the API.

Defect 10

Summary: Deactivated visitors remain in the active visitor list

Type: Functional

Description:
After a visitor is deactivated through the API, the visitor remains visible in the active visitor list even though the visitor active status is set to false.

Steps to Reproduce:

Using Postman, send a GET request to retrieve the active visitor list.
Select an active visitor and note the visitor ID.
Send a PATCH request to the visitor deactivation endpoint using the visitor ID.
Confirm that the response shows the active status as false.
Send another GET request to retrieve the active visitor list.
Check whether the deactivated visitor is still included.

Expected Result:
Deactivated visitors should be excluded from the active visitor list.

Actual Result:
The deactivated visitor remains visible in the active visitor list even though the active status is false.

Defect 11

Summary: Next page button becomes disabled while additional visitors exist

Type: Functional

Description:
The Active Visitors list is paginated at 20 records per page. After checking out multiple visitors, the Next page button becomes disabled even though additional active visitor records are still available.

Steps to Reproduce:

Open the Visitor Check in page.
Ensure that more than 20 active visitor records are available.
Navigate to the first page of the Active Visitors list.
Confirm that the Next page button is available.
Check out multiple active visitors.
Observe the pagination controls.
Check the Next page button while additional active visitor records still exist.

Expected Result:
The Next page button should remain enabled when additional active visitor records are available. It should become disabled only when the last page is reached.

Actual Result:
The Next page button becomes disabled even though additional active visitor records are still available.

#Defect 11

Summary: API allows visitor creation with missing required fields

Type: Functional

Description:

The visitor creation API allows a visitor to be created even when the required Full Name and Host fields are empty. The API returns a `201 Created' response instead of rejecting the request.

Steps to Reproduce:

1 Open Postman.
2 Send a `POST' request to the visitor creation endpoint.
3 Use the following request body:


{
  "company_name": "",
  "full_name": "",
  "host_id": "",
  "purpose": ""
}

4 Send the request.
5 Observe the response.

Expected Result:

The API should reject the request because Full Name and Host are required fields. A validation error response should be returned, such as `400 Bad Request'.

Actual Result:

The API returns `201 Created' and allows the visitor record to be created even though the required Full Name and Host fields are empty.



Open Questions
Open Question 1

Summary: Minimum length for Full Name

Type: Data

Description:
The Full Name field accepts a single alphabetic character such as A.

Steps to Reproduce:

Open the Visitor Check in page.
Enter a single alphabetic character in the Full Name field.
Submit the registration form.

Expected Result:
The expected minimum length should be defined in the requirements or specification.

Actual Result:
The system accepts a single character as a visitor name.

Question:
Should the Full Name field have a minimum character limit or require more than one character?

Reason:
The assessment specification does not define a minimum length for visitor names, so this behavior is recorded as an open question rather than a confirmed defect.

Open Question 2

Summary: Duplicate active visitor registration

Type: Functional

Description:
The application allows the same visitor details to be submitted multiple times while the previous visitor record is still active.

Steps to Reproduce:

Register a visitor using valid details.
Do not check out the visitor.
Register another visitor using the same details.
Observe the Active Visitors list.

Expected Result:
The expected behavior for duplicate active visitor registration should be defined in the requirements or specification.

Actual Result:
The system allows the same visitor details to be registered again.

Question:
Should an already active visitor be allowed to register for another visit before being checked out?

Reason:
The assessment specification does not clearly state whether duplicate active visitor registrations are allowed, so this behavior is recorded as an open question rather than a confirmed defect.

Open Question 3

Summary: Whitespace only Full Name

Type: Data

Description:
The Full Name field accepts whitespace only input during visitor registration.

Steps to Reproduce:

Open the Visitor Check in page.
Enter only spaces in the Full Name field.
Submit the registration form.
Observe the result.

Expected Result:
The expected behavior for whitespace only names should be defined in the requirements or specification.

Actual Result:
The system accepts whitespace only input.

Question:
Should whitespace only input be rejected as an invalid visitor name?

Reason:
The assessment specification does not define validation rules for whitespace only names, so this behavior is recorded as an open question rather than a confirmed defect.