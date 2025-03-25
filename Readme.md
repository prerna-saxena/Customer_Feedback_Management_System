Business Requirements Document
Home Assignment
(Software Tester - Web Applications)
Customer Feedback Management System (CFMS)
=============================================1. Edge/Test Cases
Write at least 10 test cases covering the following types:
● Functional Testing
● Integration Testing
● Security Testing
Each test case should follow this format:
● Test Case ID: (e.g., TC001)
● Test Scenario: (e.g., Submitting feedback without an email)
● Test Steps: (e.g., 1. Open feedback form, 2. Enter details except email, 3. Submit)
● Expected Result: (e.g., System should display an error message "Email is required")
=============================================
10 test cases covering functional, integration, and security testing for the Customer Feedback Management System (CFMS):
=============================================
Functional Testing
TC001: Submitting feedback without an email
•	Test Steps:
1.	Open the feedback submission form.
2.	Enter a name, rating, and comments but leave the email field empty.
3.	Complete CAPTCHA verification and submit the form.
•	Expected Result: The system should display an error message: "Email is required."
TC002: Submitting feedback with an invalid email format
•	Test Steps:
1.	Open the feedback submission form.
2.	Enter a name, invalid email (e.g., "invalid-email"), rating, and comments.
3.	Complete CAPTCHA verification and submit the form.
•	Expected Result: The system should display an error message: "Enter a valid email address."
TC003: Submitting feedback with a comment shorter than 10 characters
•	Test Steps:
1.	Open the feedback submission form.
2.	Enter a valid email, rating, and a comment with fewer than 10 characters.
3.	Complete CAPTCHA verification and submit the form.
•	Expected Result: The system should display an error message: "Comments must be at least 10 characters long."
________________________________________
Integration Testing
TC004: Admin receives an email when new feedback is submitted
•	Test Steps:
1.	Submit a valid feedback form as a customer.
2.	Check the admin's email inbox.
•	Expected Result: The admin should receive an email notification about the new feedback.
TC005: Customer receives an email when admin responds to feedback
•	Test Steps:
1.	Submit feedback as a customer.
2.	Log in as an admin and respond to the submitted feedback.
3.	Check the customer's email inbox.
•	Expected Result: The customer should receive an email notification containing the admin's response.
TC006: Searching feedback by customer email
•	Test Steps:
1.	Log in as an admin.
2.	Enter a customer's email in the search field.
3.	Click the search button.
•	Expected Result: The system should display all feedback entries associated with the provided email.
________________________________________
Security Testing
TC007: Preventing SQL Injection in feedback submission
•	Test Steps:
1.	Open the feedback submission form.
2.	Enter SQL injection payload (' OR 1=1; --) in the comments field.
3.	Submit the form.
•	Expected Result: The system should reject the input and display a validation error without executing SQL commands.
TC008: Preventing XSS in feedback comments
•	Test Steps:
1.	Open the feedback submission form.
2.	Enter a valid email and rating.
3.	Enter a script tag (<script>alert('XSS');</script>) in the comments field.
4.	Submit the form.
•	Expected Result: The system should sanitize the input and prevent script execution.
TC009: Unauthorized access to the admin panel
•	Test Steps:
1.	Try accessing the admin panel URL directly without logging in.
•	Expected Result: The system should redirect to the login page or display an "Access Denied" message.
TC010: Preventing spam feedback submissions
•	Test Steps:
1.	Submit multiple feedback entries in quick succession using an automated script.
•	Expected Result: The system should detect spam-like behavior and block submissions after a threshold.
=============================================










2. Acceptance Criteria
Define the acceptance criteria for at least 5 key features from the BRD. Acceptance criteria should clearly define the expected behavior that needs to be met for the feature to be considered successfully implemented.
=============================================
1. Feedback Submission Form
Acceptance Criteria:
✔ The system must allow customers to submit feedback through a structured form.
✔ The feedback form must contain the following fields:
•	Name (optional)
•	Email (mandatory, must be in a valid email format)
•	Rating (1-5 stars)
•	Comments (must be between 10 and 500 characters)
•	CAPTCHA verification (to prevent spam submissions)
✔ If the email field is empty or invalid, an appropriate error message should be displayed.
✔ If the comment is below 10 characters or exceeds 500, an appropriate error message should be displayed.
✔ CAPTCHA verification must be mandatory before submission.
✔ Upon successful submission, the customer should see a confirmation message: "Your feedback has been submitted successfully."
________________________________________
2. Admin Panel - Feedback Management
Acceptance Criteria:
•	Only authenticated admins should be able to access the admin panel.
•	The admin panel should display all submitted feedback with sorting and filtering options (e.g., by date, rating).
•	Admins should be able to search feedback by customer email or keyword.
•	Admins should be able to respond to feedback, and the response should be visible to the respective customer.
•	Admins should have the option to delete inappropriate feedback after confirmation.
•	Deleted feedback should be permanently removed and should not be retrievable.
________________________________________
3. Email Notifications
•	Acceptance Criteria:
•	The system must send an email notification to the admin when new feedback is submitted.
•	The system must send an email notification to the customer when an admin responds to their feedback.
•	Emails should include relevant details such as customer name, feedback rating, and comments (for admin emails) and admin response (for customer emails).
•	Emails should be sent within 10 seconds of the triggering event.
•	the email format must be clear and well-structured, avoiding spam-like behavior.
________________________________________
4. Security & Compliance
•	Acceptance Criteria:
•	The admin panel should be accessible only by authorized admin users (authentication required).
•	All user inputs should be validated and sanitized to prevent SQL Injection and XSS attacks.
•	 CAPTCHA verification should be required to prevent automated spam submissions.
•	Feedback data should be stored securely and not be accessible without proper authentication.
•	 The system should log any unauthorized access attempts and block multiple failed login attempts.
________________________________________
5. Performance & Compatibility
•	Acceptance Criteria:
•	The web application should be fully responsive, functioning properly on desktops, tablets, and mobile devices.
•	The system should be able to handle up to 10,000 feedback entries without performance degradation.
•	Page load time should not exceed 3 seconds under normal load.
•	Sorting and searching feedback should be completed within 2 seconds.
•	The application should be compatible with all major web browsers (Chrome, Firefox, Edge, Safari).
This document provides a structured and logical approach to testing and acceptance criteria for the CFMS. The defined test cases ensure that functional, integration, and security aspects of the system are covered, while the acceptance criteria ensure the system meets business and technical requirements effectively.

]
