# Requirement Documents

## Project Description
* Mobile app
* Specific sign up
* Students demographic information
* Their movements will be tracked inside a pre-configured classroom, like the chairs, tables etc. can be set in a classroom in the app.
* At the end of the class, they will be presented with a survey about their specific movements
* Most of the things should be customizable in this system, like chairs, tables, and survey questions.
* Contact: Gary Pavlechko

Title: Director of Interactive Learning Spaces and Faculty Learning Communities at Ball State University

Email: gpavlech@bsu.edu

## User classes and characteristics:
* Students in classroom 418 in TC shall use this application. The students are not required to have any technical background since the system will be straightforward and easy to use.
* Teachers in classroom 418 in TC shall use this application. The teachers are not required to have any technical background since the system will be straightforward and easy to use.
* Administrator will be the primary maintainer of the application. They will have to have a technical background.


## Technical constraints:
* MySQL database
* Operable on Linux Server
* Supports IOS and Android in one codebase
* Prefer python for server-side code
* Web interface based backed-end

## Use cases:
### Use case name: Take survey
* Primary Actor: Students
* Summary Description: Students specify the desire to explain their movement throughout class in the survey by pressing a button. The system either allows the student to take the survey or informs the student that the survey is not available.
* Trigger: Requester indicates they want to take survey
* Pre-Condition: The students have to attend class to take survey
* Post-Condition: The system records the students’ data from the survey
* Normal flow: Request to take survey
* Exception: Survey is not available
* Priority: High
* Frequency of use: Anytime class is in session which is about 2-3 times a week
* Assumption: Class is assumed to be in session

### Use case name: Reconfigured survey questions
* Primary Actor: Instructor
* Summary Description: Instructor specifies the desire to reconfigure survey questions by pressing a button. The system allows the instructor to reconfigure survey questions.
* Trigger: Requester indicates they want to reconfigured survey questions
* Pre-Condition: Class must be in session
* Post-Condition: The system records details of the changes made by the Instructor
* Normal flow: Reconfigured survey questions
* Exception: Classroom in not in session therefore no need for a survey
* Priority: High
* Frequency of use: Anytime class is in session which is about 2-3 times a week per class
Assumption: Class is assumed to be in session

### Use case name: Reconfigured classroom setting
* Primary Actor: Instructor -> Administrator
* Summary Description: Instructor specifies the desire to reconfigure the classroom. setting. The system allows the instructor to reconfigure the classroom setting.
* Trigger: Requester indicates they want to reconfigured classroom setting
* Pre-Condition: Class must be in session
* Post-Condition: The system records details of the changes made by the Instructor
* Normal flow: Reconfigured classroom setting
* Exception: Classroom in not in session therefore no need to reconfigured classroom
* Priority: High
* Frequency of use: Anytime class is in session which is about 2-3 times a week per class
* Assumption: Class is assumed to be in session

### Use case name: Search, delete, and add students to database 
* Primary Actor: Administrator
* Summary Description: Administrator specifies the desire to search, delete, and add students to database. The system either allows the administrator to search, delete, and add students to database or informs the administrator that there is no data available.
* Trigger: Requester indicates they want to search, delete, and add students to database
* Pre-Condition: There must be students to populate the database
* Post-Condition: The system records details of the changes made by the administrator
* Normal flow: Search, delete, and add students to database
* Exception: No data available in database to edit
* Priority: Medium
* Frequency of use: Anytime administrator wants to view data
* Assumption: Data is assumed to be available in database

### Use case name: Review room layout history 
* Primary Actor: Administrator
* Secondary Actor: Instructor
* Summary Description: Administrator and instructor specify the desire to be able to see the room layouts saved by the instructor. The system either allows the administrator and instructor to review room layout history or informs the administrator and instructor that there is no data saved in the database.
* Trigger: Requester indicates they want to review room layout history
* Pre-Condition: The teachers must save the room layout
* Post-Condition: The system records details of new data to alert administrator of changes
* Normal flow: Review room layout history
* Exception: No data available in database to review
* Priority: High
* Frequency of use: Anytime administrator wants to view data
** Assumption: Data is assumed to be available in database
### Use case name: Review demographics information
* Primary Actor: Students
* Secondary Actor: Administrator
* Summary Description: Students and Administrator specify the desire to be able to see review/edit demographics information. The system either allows the student and administrator to review demographics information or informs the student or administrator that there is no data saved in the database.  
* Trigger: Requester indicates they want to review demographics information
* Pre-Condition: The student must enter data
* Post-Condition: The system records details of new data
* Normal flow: Review demographics information
* Exception: No data available in database to review
* Priority: Medium
* Frequency of use: Anytime student or administrator want to review data
** Assumption: Data is assumed to be available in database

## Functional requirements:
### If the class is in session the instructor can reconfigure classroom layout.
* Priority: High
* Availability: The system should be available to use anytime especially after classroom times.
* Instability: The user should be able to easily download the application.
* Integrity: The system should protect against unauthorized addition, deletion, or modification of data.
* Interoperability: The system should be able to export classroom setting data.
* Performance: The system should update the data entered frequently.
* Reliability: The system should be able to run without failure for some time.
* Robustness: The system should be able to gracefully accept erroneous input from the instructor without crashing.
* Security: The system should restrict unauthorized access to the instructors account.  
* Usability: The system should be easy to use.

### If the system receives new information to store and needs to update data
* Priority: High   
* Availability: The system should be available to update and store new information at anytime, especially during/after classroom times.
* Instability: The system should be able to be easily installed into the server.
* Integrity: The system should protect against unauthorized addition, deletion, or modification of data.
* Interoperability: The system should be able to store information into a SQL Query for easy data retrieval 
* Performance: The system should update the data entered frequently.
* Reliability: The system should be able to run without failure for some time.
* Robustness: The system should be able to gracefully accept erroneous input from an outside source without crashing.
* Security: The system should restrict unauthorized access to the system
* Usability: The system should be easy to use.

### If the class is in session the student has the option to take a survey. The student will be informed if the survey is available.
* Priority: High
* Availability: The system should provide a notice for the student to be able to take the survey only at specific times designated by the instructor/administrator.
* Instability: The system should be able to be easily installed onto a user’s personal device.
* Integrity: The system should protect against unauthorized access to the system through a user’s personal device.
* Interoperability: The system should be able to send information from the user’s personal device to the database for easy data organization.
* Performance: The system should be able to retrieve and send information to the server provided by the user.
* Reliability: The system should be able to run without failure for some time. 
* Robustness: The system should be able to gracefully accept erroneous input from the user without crashing.
* Security: The system should be able to prevent unauthorized access to the system from the user’s personal device.
* Usability: The system should be simple with a linear layout.

### If the class is in session the instructor can reconfigure survey questions. The instructor will be able to delete, add, and change survey questions.
* Priority: High   
* Availability: The system should be available to the instructor at all times, especially during class times.
* Instability: The system should be easily installed onto the instructor’s personal device.
* Integrity: The system should be able to protect against unauthorized access to the instructor’s capabilities.
* Interoperability: The system should be able to send information from the instructor’s personal device to create a database for the student’s information.
* Performance: The system should be able to retrieve and send information to the server provided by the user.
* Reliability: The system should be able to run without failure for some time. 
* Robustness: The system should be able to gracefully accept erroneous input from the instructor without crashing
* Security: The system should prevent unauthorized access from the instructor’s personal device.
* Usability: The system should be simple with a linear layout.

### If the room layout data is available in database the administrator has the option to review and make changes to data. The administrator will be informed if there is no room layout data available.
* Priority: High   
* Availability: The system should be available to the administrator at all times. 
* Instability: The system should be easily accessed by an administrator’s device.
* Integrity: The system should be able to protect against unauthorized access to the administrator’s capabilities and only be available for the administrator.
* Interoperability: The system should be able to send information to the administrative device to edit a rooms layout for a specific day/event
* Performance: The system should be able to retrieve a previously saved map layout for a specific event, or report that there is no map and one can be created.
* Reliability: The system should be able to run without failure for some time. 
* Robustness: The system should be able to gracefully accept erroneous input from the administrator without crashing
* Security: The system should prevent unauthorized access from the instructor’s personal device
* Usability: The system should be simple with a linear layout

### If student information is available in database the administrator has the option to review and make changes to data. The administrator will be informed if there is no student information available.
* Priority: High  
* Availability: The student’s information within the database should be accessible by an administrator at all times.
* Instability: The administrator should be able to log onto a device with the system database and pull a student’s information from it.
* Integrity: The system should be able to protect against unauthorized access to the administrator’s capabilities and only be available for the administrator.
* Interoperability: The administrator’s device should be able to connect to the server the system is running on.
* Performance: The administrator should be able to request students information whenever they wish to and be able to make edits at will.
* Reliability: The system should be able to run without failure for some time. 
* Robustness: The system should be able to gracefully accept erroneous input from the administrator without crashing.
* Security: The system should only allow authorized users (administrators) to access the information from the database.
* Usability: The system should allow an ease of access to the data due to the SQL Query that will be its format.

### If student wants to review demographics information they have the option to edit and view their information. The system will inform the student if there is no demographics information available, otherwise it will allow the student to edit the information.
* Priority: High
* Availability: The student should be able to access and change their demographic information at all times, regardless of an open survey or not.
* Instability: The students should be able to pull up the system on their personal device from the application.
* Integrity: The system should be able to allow students direct access to their demographics while preventing outside sources from tampering with it.
* Interoperability: The system should be able to transfer a student’s demographic information from the server and then save any and all changes that student made on their personal device.
* Performance: The student should be able to edit their demographic information on the server and have any changes saved and overwriting any previous information
* Reliability: The system should be able to run without failure for some time. 
* Robustness: The system should be able to gracefully accept erroneous input from the administrator without crashing.
* Security: The system should be able to prevent unauthorized users from accessing the student’s information without proper identification.
* Usability: The student should be able to find, see, and change their demographic information in a linear format.

### If administrator wants to review demographics information they have the option to edit and view the information. The system will inform the administrator if there is no demographics information available, otherwise it will allow the administrator to edit the information.
* Priority: High   
* Availability: The system should allow an administrator to review and edit an account at any time.
* Instability: The system should be able to easily search for specific students or groups of them to check demographic information from the database
* Integrity: The system should be able to report information requested by the administrator without losing valuable information. Should also be able to report if no information is found.
* Interoperability: The system should be able to connect to an administrator’s device and provide information from the database to that device
* Performance: The system should report the requested information in a timely manner.
* Reliability: The system should be able to run without failure for some time. 
* Robustness: The system should allow multiple groupings of information to be made available without crashing.
* Security: The system should only allow administrators access to all accounts and only allow a student to access their account. 
* Usability: The system should be able to provide a search option that an administrator can utilize to find students easily within the database.

### The system must be able to store and update data. Students, instructors, and administrator must have access to update data.
* Priority: High   
* Availability: The system should be able to store and update data at all times
* Instability: The system should be able to connect to applications on all the user’s personal devices and receive any information implanted from the application. 
* Integrity: The system should constantly update data to prevent loss and enforce changes as they are made to prevent conflicts.
* Interoperability: The system should be able to connect to a user’s device and give/receive information to update data.
* Performance: The system should report to a user when a change is made or the risk of losing a change occurs.
* Reliability: The system should be able to run without failure for some time. 
* Robustness: The system should be able to gracefully accept erroneous input from any user without crashing.
* Security: The system should only allow students, instructors, and administrators within the system.
* Usability: The system should be able to automatically update data as a user submits without much need from administrator assistance.
            
# Non-functional requirements:
### Request student and instructor login.
* Priority: Medium
* Availability: The system should allow students and instructors to be able to login to application anytime, especially during classroom hours.  
* Instability: The application should be easy to download, login, and uninstall.
* Integrity: The system should update frequently to prevent data loss.
* Interoperability: The system should be able to exchange date with other systems in order for the administrator to access the data.
* Performance: The system should respond to user inputs at a reasonable time.
* Reliability: The system should be able to run without failure for a long period of time.
* Robustness: The system should be able to function even if user entered erroneous input. It should be able to inform the user if the input they entered in the login is not the correct.
* Security: The system should protect against unauthorized access by requesting password. 
* Usability: The system’s login should be easy to use.

### Must be accessible in IOS and Android devices
* Priority: Medium
* Availability: The system should be available in IOS and Android devices.
* Instability: The system should be easy to install and uninstall in both IOS and Android devices.
* Integrity: The system should update frequently to prevent data loss.
* Interoperability: The system should be able to exchange date with other systems.
* Performance: The system should respond to user inputs at a reasonable time in both IOS and Android devices.
* Reliability: The system should be able to run without failure for a long period of time in both IOS and Android devices.
* Robustness: The system should be able to function even if user entered erroneous input in both IOS and Android devices.
* Security: The system should protect against unauthorized access.
* Usability: The application should be easy to use in both IOS and Android devices.

# Assumptions:
* Mobile app so needs to be compatible with IOS and Android
  * Confirmed by client
* Database to retain Students logins and demographic information
  * Confirmed by client
  * Prefer we use Ball State students’ login
* Admin account to search, delete, and possibly add students to/from database
        	** Confirmed by client
        	
 

