QA Notes

#Highest-Risk Area

The highest-risk area is the visitor registration flow.

Visitor registration is the main entry point for creating a visitor record. The data entered in the registration form is used to create the visitor record and display it in the Active Visitors list.

A problem in this flow could result in invalid visitor data, incomplete records, duplicate registrations, or a visitor not appearing correctly after registration.

The registration flow is therefore given higher test coverage, especially around required fields, host selection, successful submission, and the data displayed after registration.



#Product Owner Question

Question:

Should the system allow the same visitor to have more than one active visit at the same time?

Reason:

The expected behavior for duplicate active visitor registration is not clearly defined. This needs to be clarified before sign-off so the team knows whether multiple active visits for the same visitor are allowed.

#Regression Subset

#Change Being Tested

A minor UI update is made to the visitor registration form. The layout of the fields and the Submit button has been changed, but there is no intended change to the registration business logic or API.

#Regression Tests

TC 001 – Verify Visitor Check In page loads

Include: Yes

Reason:The registration form is part of the page. The page should still load correctly after the UI change.


TC 002 – Verify all registration fields are displayed

Include:Yes

Reason: The registration form layout has changed, so all required fields and the Submit button must still be present and usable.


TC 003 – Verify visitor can be registered with valid information

Include:Yes

Reason: This is the main registration flow. It confirms that the UI change has not affected form submission or successful visitor registration.



TC 004 – Verify Full Name is required

Include: Yes

Reason: Full Name is part of the updated form. The required-field validation should still work after the UI change.


TC 005 – Verify Company is required**

Include: Yes

Reason: Company is part of the registration form and its required validation should remain functional after the update.


TC 006 – Verify Host is required

Include: Yes

Reason: Host is part of the registration form. This confirms that the Host field and its required validation still work correctly.



TC 007 – Verify Purpose is required

Include: Yes

Reason: Purpose is part of the registration form, so its required validation should be checked after the form update.


TC 014 – Verify Host dropdown

Include: Yes

Reason: The Host field is part of the registration form and could be affected by changes to the form layout or field structure.


TC 015 – Verify host can be selected

Include: Yes

Reason: Confirms that the user can still interact with the Host field and select a host after the UI update.


TC 016 – Verify visitor information after registration

Include: Yes

Reason: Confirms that information entered through the updated form is saved and displayed correctly after registration.


TC 019 – Verify new visitor appears in Active Visitors

Include:Yes

Reason: Confirms that the updated registration form still creates a visitor record that appears in the Active Visitors list.

#Tests Not Included

TC 009–013 – Full Name boundary and invalid-input cases

Reason: These cases focus on specific Full Name validation rules. The assumed change is only a UI/layout update and does not change Full Name validation logic.


TC 018 – Verify check in time uses local timezone

Reason: Timezone handling is unrelated to the UI changes being tested.


TC 020–024 – Checkout and deactivation

Reason: These workflows happen after registration and are not affected by the assumed registration form UI change.


TC 025–030 – Active Visitors empty state and pagination

Reason: These cases cover the Active Visitors list and pagination behavior, which are separate from the registration form UI.


TC 031–055 – API test cases

Reason:The change does not modify the API, request payload, or backend registration logic. Therefore, API regression is not included in this focused regression subset.