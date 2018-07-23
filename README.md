# Milestone 3: More Detailed Requirements, Architecture and a Vertical Software Prototype

## Instruction:<br>
Milestone 3 consists of two parts:<br>
1)	Milestone 3 document – an expanded version of Milestone 1<br>
2)	A vertical software prototype <br>
###### Part 1: Milestone 3 document:<br>
Milestone 3 has to be reasonably consistent with Milestone 1 and instructors’ feedback but it can also differ from Milestone 1 based on what you discover and develop in your design process in spirit of iterative software engineering process and based on the feedback you get. 
The difference between M1 and M3 DO NOT need to be edited in Milestone 1 document which remains frozen. You should start with Milestone 3 only after you have incorporated instructors’ feedback on Milestone 1. Milestone 3 document is a separate document from Milestone 1.<br>
###### Part2: Vertical software prototype<br>
In addition to the Milestone 3 document, the team will create a “vertical software prototype” to test the infrastructure and chosen frameworks and to jumpstart the coding effort.  The vertical prototype is the code that exercises full deployment stack from browser, via middleware, to DB and back-end, including your chosen framework. It has to be deployed from team account, in the same way that the final product will be deployed. For example, it shall allow one to enter a search term in the browser, then get a response form the DB and render it back on the browser. GUI for this can be simple one field entry and DB can have only a few items. The items in your DB shall be encoded with full schema as it is defined by now. The purpose of vertical prototype is to early and quickly test basic software components and deployment infrastructure and frameworks as well as the key architecture patterns and thus to serve as a basic “scaffolding” for final product. It also serves as “teaching and training” tool to bring the rest of the team up to speed on development, frameworks etc. We recommend that back-end team be assigned the task of constructing this vertical prototype.<br>


## 1.	Title page<br>
See Milestone 1 instruction<br>

## 2.	Executive Summary<br>
Modify based on Milestone 1. Add or change as you see necessary.<br>

## 3.	Competitive analysis<br>
Modify based on Milestone 1. Add or change as you see necessary.<br>

## 4.	Data definition<br>
This should be reasonably consistent with Milestone 1 but should be expanded as needed and refined as per feedback. Major data items that comprise of sub-data items have to be defined in full (list all its sub-data items, and for images/video list formats, max size etc.). You must use all the data definitions and names consistently in all documents, including GUI text. Focus on data items unique and important to your application and avoid explaining obvious things like Internet,, Browser, Cloud, etc. Be sure to cover ALL items critical to your project and especially those providing a competitive advantage. At this stage data describing user privileges, registration info and main info (raw data, metadata, supporting data) have to be fully defined (as much as it is possible at this stage)<br>

## 5.	Overview, scenarios and use cases<br>
Modify based on Milestone 1. Add or change as you see necessary.<br>

## 6.	Initial list of High-level functional requirements<br>
Expand functional requirements from Milestone 1 into Milestone 3, with more details as necessary. Keep the same reference numbers with respect to Milestone 1 (i.e. if high level requirement was number 3 in Milestone 1, then in Milestone 3 more detailed requirements are 3.1, 3.2 etc.).  Be sure to cover ALL and especially unique features of your product. OK to add new or delete previous functional requirements from Milestone 1, if you can justify it. <br>
Prioritize each requirement/spec with 1, 2, 3. (1-must have; 2 – desired; 3 – opportunistic as defined in the class). To develop these priorities think of the user, use cases, and making your application complete from usability, marketing and business aspects. Base this also on your skills, resources and schedules. Instructors will check final priorities. The priorities you set later in Milestone 4 will constitute your commitment (especially priorities of 1), so be very careful. <br>

## 7.	List of non-functional requirements<br>
Reference to your final high-level functional requirements, modify based on Milestone 1. Add or change as you see necessary.<br>

## 8.	High-level system architecture and database organization<br>
Software products and Tools<br>
Brackets, Notepad++, Putty, WinSCP, FileZilla, GitHub, etc<br>
Languages and Systems<br>
English, HTML, PHP, MySQL, Linux, Windows, MacOS, Mobiles , etc<br>
APIs<br>
Calendar, Weather<br>
PHPMailer<br>
Supported Browsers<br>
Chrome, Firefox, Opera, Safari, Microsoft Edge, Internet Explorer<br>
Frameworks<br>
HTML, PHP, CSS<br>

DB Organization:<br>
The database get divide into multiple tables. With the UserID from the User table you can get access to the User_Info, Event, User_Comments, and Security_Answers tables. In addition, from Security_Answers you get data from Security_Questions using the QuestionID and both the Event and User_Comment tables get connected with not only UserID but EventID as well. In other words, as long as you have the UserID, you can get information in all the tables that belong to a specific person. <br>
List of DB Tables:<br><br>
User: UserID, UserName,Password, Salt, Role, Status<br>
User_Info: UserID, FirstName, LastName, NickName, DoB, Gender, Email, Telephone, Major<br><br>
Event: EventID, UserID, Location, Description, Date/Time, Media, Verify, Path. <br>
User_Comments: C_ID, UserID, EventID, Comment.<br>
Security_Answers: UserID, QuestionID, Answers<br>
Security_Questions: QuestionID, Questions<br>

Media Storage:<br>
The images and video/audio will be kept in file system. The database only stores the path to the files (Event table).<br>
Search/filter architecture and implementation:<br>
The execution of a “select” statement to the database will be used for searching, where the condition for the statement can be any of the element in a collection of  fields used for searching.<br>
Term will be used for searching:<br>
Username: a String stored in User table. Once the Username is found, the system will get the UserID and find corresponding Nickname and display the Nickname back to UI.<br>
Nickname: a String stored in User_Info table. Once the Nickname is found, the system will return and display the Nickname back to UI.
First Name/Last Name: two Strings stored in User_Info table. Once either one or both First Name Last Name is found, the system will return and display the corresponding Nickname back to UI.<br>
Event Description (partial also works): a String stored in Event table. Once found, the system will return everything about that event back and display in UI.<br>
Location: a String stored in Event table. Once found, the system will return every event in that location back and display in UI.
Term will be filtered/sorted:<br>
Location: a String stored in Event table. By applying this filter, the system will execute a search on the selected location.<br>
Date/Time: a DateTime field in Event table, entered by the system when an event is posted, and will be sorted from newest to oldest.<br>
Verify: a Boolean field in in Event table. By applying this filter, the system will show only events that were verified by Power User.<br>
Your own APIs:<br>
We will not create any API of our own.<br>
Describe any significant non-trivial algorithm or process:<br>
The order of the event post will be shown in order (newest first):  have to read the event bottom up according to datetime. Before output each post, the Event table (store all of the event post from user) will get descending (DESC) sort by the Date/Time before output to the Home Screen.<br>
Verifying is the process where power user verify whether a post is legit. In Event table there’s a verify field which all post will be masked as false at first. Then Power User can check the event physically and indicate whether the post is legit. From there the Power User can decide whether the post can stay in the system by click on verified or delete. <br>



## 9.	High-Level UML diagrams<br>
Familiarize yourself with Unified Modeling Language (UML). Find your favorite UML tutorials from the Internet. One good one is http://edn.embarcadero.com/article/31863<br>
At minimum provide:<br>
1)	High-level UML class diagrams for implementation classes of core functionality, i.e. functionality with provided interfaces. Focus on main high-level classes only (one or at most two levels deep). This must reflect an OO approach to implementing your site.<br>
2)	UML Component and deployment diagrams
Use data terms and names consistently with Glossary/Data Dictionary.<br>


## 10.	Identify actual key risks for your project at this time<br>
Skills risks: Some of the development team members lack the database skills<br>
Schedule risks: Some of the team members are too busy, but other members are trying to make up for that. We’re trying our best to make it in time.<br>
Technical risks: None<br>
Teamwork risks: Lack of communication. Each member will have to review the idea for the project and communicate with each other more. Especially ask questions on things that is unclear for verification and agreement instead of just assuming and spend more time to fix later on.<br>
Legal/content risks: None<br>






