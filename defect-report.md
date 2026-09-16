DEF-001: Full Name Field Accepts Single-Letter Names

Summary: Full Name field accepts a single letter as a valid visitor name.

Type:Data Validation

Description:
The Full Name field accepts a single alphabetic character as a valid name. Although the field also accepts normal full names, it does not enforce a minimum length or require a meaningful full name.

Steps to Reproduce:

1. Open the visitor registration form.
2. Enter a single letter, such as `A`, in the Full Name field.
3. Fill in the remaining required fields with valid information.
4. Submit the registration form.
5. Check the visitor record in the active visitor list.

Expected Result:
The system should reject a single-letter value as an invalid full name and display an appropriate validation message. A valid visitor name should contain an appropriate minimum number of characters.

Actual Result:
The system accepts a single letter as the visitor's full name and allows the registration to proceed successfully.

