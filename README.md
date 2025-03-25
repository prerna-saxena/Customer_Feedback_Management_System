# Customer_Feedback_Management_System
Customer_Feedback_Management_System_Software_Tester_Solution


Objective: The CFMS is a web application that enables businesses to collect and manage
customer feedback through a structured form. The system will allow customers to submit
feedback, and business administrators to review, respond, and analyze feedback trends.
Features & Requirements:
○ User Roles:
i. Customer (Can submit feedback, view past feedback submissions)
ii. Admin (Can view, respond to, and manage feedback)
○ Feedback Submission Form:
i. Customers must provide the following information:
1. Name (optional)
2. Email (mandatory, must be a valid email format)
3. Rating (1-5 stars)
4. Comments (minimum 10 characters, maximum 500
characters)
5. CAPTCHA verification before submission

○ Feedback Management (Admin Panel):
i. View all submitted feedback with sorting/filtering options (e.g., by
rating, date)
ii. Search feedback by customer email or keyword
iii. Respond to feedback (admin response will be visible to the
customer)
iv. Delete inappropriate feedback
○ Security & Compliance:
i. Only admins should have access to the admin panel
ii. Input validation and sanitization for all fields to prevent SQL
Injection and XSS attacks
iii. CAPTCHA verification to prevent spam submissions
iv. Feedback should be stored securely and should not be publicly
accessible without login
○ Notifications & Alerts:
i. Email notification to admin when new feedback is submitted
ii. Email notification to customer when admin responds to their
feedback

○ Device Compatibility & Performance:
i. The web application should be fully responsive and accessible across
desktops, tablets, and mobile devices
ii. The system should handle up to 10,000 feedback entries without
performance degradation

Mahakaya Technologies Pvt. Ltd.
Plot No-8, Block-C, Janakpuri, West Delhi, India - 110058
www.mahakayatechnologies.in

Your Tasks

1. Edge/Test Cases
Write at least 10 test cases covering the following types:
● Functional Testing
● Integration Testing
● Security Testing
Each test case should follow this format:
● Test Case ID: (e.g., TC001)
● Test Scenario: (e.g., Submitting feedback without an email)
● Test Steps: (e.g., 1. Open feedback form, 2. Enter details except email, 3. Submit)
● Expected Result: (e.g., System should display an error message "Email is required")
2. Acceptance Criteria
Define the acceptance criteria for at least 5 key features from the BRD. Acceptance
criteria should clearly define the expected behavior that needs to be met for the feature to
be considered successfully implemented.

Submission Guidelines
1. Submit your response in PDF or DOCX format.
2. Ensure clarity, proper formatting, and completeness in your test cases and
acceptance criteria.
3. Submit your assignment within 48 hours.
Evaluation Criteria:
1. Understanding of functional, integration, and security testing
2. Ability to identify edge cases and write clear test cases
3. Clarity and completeness of acceptance criteria
4. Logical approach and structured documentation
