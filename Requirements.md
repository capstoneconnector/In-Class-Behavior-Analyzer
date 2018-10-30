# Requirements Documents

 - [Google Documents notes](https://docs.google.com/document/d/19V_oVq57zbx2RUjroK89Ok1RTQhPDSYNuMSrUVdH1W0/edit#heading=h.fh7zabgwix36)

## Project Description
Gary wants a mobile app to be installed by students in a specific classroom. They will sign up and give their demographic information. 
Their movements will be tracked inside a pre-configured classroom, like the chairs, tables etc can be set in a classroom in the app.

At the end of the class, they will be presented with a survey about their specific movements, e.g. Why did you move from this table 
to that chair etc. Most of the things should be customizable in this system, like chairs, tables, survey questions.

Contact: Gary Pavlechko

Title: Director of Interactive Learning Spaces and Faculty Learning Communities at Ball State University

Email: gpavlech@bsu.edu


## User classes and characteristics:
- Students in classroom 418 in TC shall use this application. The students are not required to have any technical background since the system will be straightforward and easy to use.
- Teachers in classroom 418 in TC shall use this application. The teachers are not required to have any technical background since the system will be straightforward and easy to use.
- Administrator will be the primary maintainer of the application. They will have to have a technical background.

## Technical constraints:
- MySQL database
- Operable on Linux Server
- Supports IOS and Android in one codebase
- Prefer python for server-side code
- Web interface based backed-end

## Use cases:
- Use case name: Take survey
  Actor(s): Students
  Summary Description: Allows students to explain their movement throughout class
  Priority: High
  Pre-Condition: The students have to attend class to take survey
  Post-Condition: The system records the students’ data from the survey
- Use case name: Reconfigured survey questions
  Actor(s): Teachers
  Summary Description: Allows teachers to reconfigure survey questions
  Priority: Medium
  Pre-Condition: Class must be in session
  Post-Condition: The system records details of the changes made by the teacher
- Use case name: Reconfigured classroom setting
  Actor(s): Teachers
  Summary Description: Allows teachers to reconfigure the classroom's furniture
  Priority: High
  Pre-Condition: Class must be in session
  Post-Condition: The system records details of the changes made by the teacher
- Use case name: Search, delete, and add students to database 
  Actor(s): Administrator
  Summary Description: Allows administrator to search, delete, and add students to database 
  Priority: Medium
  Pre-Condition: There must be students to populate the database
  Post-Condition: The system records details of the changes made by the administrator
- Use case name: Review room layout history 
  Actor(s): Administrator
  Summary Description: Allows administrator to be able to see the room layouts saved by the teachers 
  Priority: Medium
  Pre-Condition: The teachers must save the room layout
  Post-Condition: The system records details of new data to alert administrator of changes

## Functional requirements:
- Reconfigure classroom layout
  Priority: High
- Store and update data
  Priority: High

## Non-functional requirements:
- Request student login
  Priority: Medium
- Must be accessible in IOS and Android devices
  Priority: Medium

## Assumptions:
- Mobile app so needs to be compatible with IOS and Android
  Confirmed by client
- Database to retain Students logins and demographic information
  Confirmed by client
  Prefer we use Ball State students’ login
- Admin account to search, delete, and possibly add students to/from database
  Confirmed by client 