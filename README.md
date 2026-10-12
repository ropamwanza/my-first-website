Accessibility peer review

Issue identified

During the Thursday peer review, my peer identified that the contact form did not have clearly associated labels for all its input fields.This cou;d make the form more difficult to understand for users who rely on assistive technologies.

Fix Applied

I added "<label>" element for each form field and associated every label with its corresponding input using matching 'for' and 'id' attributes.

For Example

<HTML>
<label for email = "email">Email Addresss:</label>
<input type  ="email" id ="email" name ="email" required placeholder = "example@gmail.com">