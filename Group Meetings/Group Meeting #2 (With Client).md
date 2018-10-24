# Weekly Team meeting #2 (With Client)
## What we know we need:
 - Preconfigured room (so one map).
 - There needs to be a signup with demographic information for each student.
 - Room needs to be able to be changed.
 - Needs to be a post class survey with certain questions.
 - Questions need to be customizable.
 - Mobile app

## Assumptions:
 - Mobile app so needs to be compatible with IOS and Android
 - Database to retain Students logins and demographic information
 - Admin account to search, delete, and possibly add students to/from database   <- talk about        											admin access on a future meeting
 - Students may need a “forgot password” option  <- use emails or id#s,
 - Possibly a “retake survey” option for students  <- future meeting

## Possible layouts:
 - Map layout: could possibly be a grid system, (room is possibly a TC or WB building so that is possible, will need more details) with circles for chairs and rectangles for tables
                                                 
 - Admin account: Allows the room and questions to be reconfigured, similar to that of a blackboard or google survey situation

 - Student account: Basic application that allows 1 of 2 options, survey questions (which should be locked until after the class) and location in the room. 

## What needs asked:
 - Location: Does it need to be automatic or manual? *Automatic will need extensive work around* See client notes
 - What kind of questions are being looked for during the demographic student questions? Gender? Major? Hometown? Age? Etc? 
   - Major
   - Year
   - Age
   - Gender
   - Race/Ethnicity
   - Drop down to select Course
   - Parent/disability?? <- future client meeting
   - Sliders 1 -> 10 to see levels of students

 - Unique user IDs
   - Basically like logging in with email and whatnot, Each class would be its own entity.

 - What kind of Survey questions other than “why you moved there” are going to be looked for? 
 - Why did you sit in the spot you chose?
 - Things they noticed in the room.


## Any specific technologies that must be used?
 - MySQL
 - Linux Server
 - Support iOS and Android in one codebase
 - Prefer python for server-side code
 - Do you need to be able to change a classroom setup?
   - Yes
 - Multiple rooms?
   - No

## Side notes
 - Will students act differently if they are a minority/stereotype?
 - How does this affect social networking?
 - Get swipe card access to the room.
 - Might have access to a budget. Work with Wayne.

