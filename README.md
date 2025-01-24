# Parikshan_Web_App
CROP DISEASE DETECTION SYSTEM IN AGRICULTURE THROGH AI/ML
Software Requirement of specification(SRS)
Crop Disease Detection System In Agriculture

1.Introduction
The Crop Disease Detection System in agriculture aims to help farmers identify and manage plants diseases quickly and accurately By using image processing and machine learning. the system analysis images of crops to detect disease symptoms and reduces the need for manual inspection speeds up diagnosis and provides timely recommendations for treatment leading to better crop health and productivity.

1.1 Purpose
This document specifies the software requirements for a Crop Disease Detection System in Agriculture. The system will provide farmers and agricultural specialists with a tool to automatically detect crop diseases using image processing and machine learning techniques, allowing them to take timely action to protect crop yield.

1.2 Scope
The system will use machine learning models to analysis images of crops, detect disease symptoms, and provide insights to farmers. It will also feature a database of known crop diseases for cross-referencing. The system will function on mobile devices as well as desktops and will be accessible to users through a web-based interface.

1.3 Definitions, Acronyms, and Abbreviations
•	ML: Machine Learning
•	AI: Artificial Intelligence
•	API: Application Programming Interface
•	CNN: Convolutional Neural Networks
•	UI: User Interface
•	SRS: Software Requirements Specification

1.4 Overview
This document outlines the functional and non-functional requirements for the Crop Disease Detection System. The subsequent sections will describe the product's features, its system interfaces, performance requirements, and more.

2.General Description
2.1 Product Perspective
The system will be part of an agricultural decision support system. It will function autonomously, taking inputs (crop images) from the users and providing disease diagnosis. It will also provide a list of recommended actions based on the detected disease.

2.2 Product Functions
•	Image-based disease detection in crops
•	Provide detailed information on identified diseases
•	Suggest treatments based on detected disease
•	Maintain a history of diagnoses for future analysis
•	Enable users to upload images via mobile or web applications

2.3 User Characteristics
•	Farmers with limited technical knowledge
•	Agricultural specialists and researchers
•	Mobile users for field use and desktop users for research purposes

2.4 General Constraints
•	The system will require an active internet connection to analyze crop images using cloud-based models.
•	Limited by the accuracy of image recognition models
•	The system will be accessible on mobile and desktop devices, and the UI must be simple enough for non-technical users to operate.

3 Specific Requirements
3.1 Functional Requirements
•	The system shall allow users to upload images of crops.
•	 The system shall process the uploaded images and identify any visible crop diseases.
•	 The system shall display the name of the disease, a description, and possible treatments.
•	The system shall store a history of all uploaded images and corresponding diagnoses.
•	 The system shall allow users to download reports in PDF format.
•	 The system shall provide push notifications for newly diagnosed diseases or system      updates.

3.2 External Interface Requirements
This section outlines the interaction between the Crop Disease Detection System and                external systems, hardware, software, and users. It also describes the constraints that govern these interfaces.

3.3	User Interfaces
•	The system shall provide a graphical user interface (GUI) accessible through web browsers and mobile apps.
o	Description: Users will upload images of crops via a responsive interface, available on mobile and desktop platforms. The UI will also display the results of crop disease detection and provide recommendations for treatments.
o	Constraints:
	The web application must be compatible with common browsers (Google Chrome, Mozilla Firefox, Microsoft Edge).
	The mobile application must be compatible with iOS and Android devices.
	The interface should follow usability guidelines, allowing farmers with limited technical knowledge to interact easily with the system.
•	The system shall allow users to log in and access their diagnostic history.
o	Description: Users will be required to authenticate with a username and password to access their profile, history, and any saved diagnostic results.
o	Constraints:
	The login system must comply with security standards (e.g., password encryption).
	The session timeout will be set to 15 minutes of inactivity.

3.4 Hardware Interfaces
•	 The system shall support image input from built-in or external cameras.
o	Description: The user will upload crop images either through a mobile phone's camera or by uploading from a desktop computer (via external cameras or file upload).
o	Constraints:
	Image resolution must be at least 1024x1024 pixels for accurate disease detection.
	The mobile app must access the camera hardware and function properly on devices with different camera specifications (e.g., varying megapixel counts).

3.5 Software Interfaces
•	 The system shall interface with a cloud-based machine learning model for image processing and disease detection.
o	Description: Once the user uploads an image, the system will send the image data to a machine learning model hosted on the cloud, which processes the image to detect crop diseases.
o	Constraints:
	The image must be in one of the following formats: JPEG, PNG.
	The machine learning model must return results within 10 seconds of image submission.
	The API handling the image analysis must follow resetful principles and handle up to 1000 image requests per minute.
     The system shall store historical data in a relational database.
•	Description: All user-uploaded images and diagnosis reports will be stored in a backend database to allow future analysis and review by the user.

3.6 Communication Interfaces
	The system shall interact with the cloud via a secure HTTP connection.
	Description: The system will send user-uploaded images and retrieve results using a secure REST API hosted in the cloud.
	Constraints:
	All communications must use HTTPS to ensure secure data transmission.
	Network latency should not exceed 200ms to maintain system responsiveness.
	The API must support JSON for data exchange.
	 The system shall send notifications to users via email or push notifications.
	Description: Once a diagnosis is completed, the system can notify users of the results via email or push notifications, depending on their preferences.
	Constraints:
	Email notifications must comply with SMTP protocols and support user-specified email addresses.
	Push notifications for mobile apps must be delivered through services like Google Firebase (for Android) and Apple Push Notification Service (for iOS).

3.7 Performance Requirements
•	 The system shall process and analysis images within 10 seconds.
