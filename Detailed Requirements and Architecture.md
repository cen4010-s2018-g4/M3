# Detailed Requirements and Architecture


## 1. Executive Summary

University students who reside on campus indulge in the various social activities and events the campus has to offer. However, they're 
also exposed to all of the issues that arise throughout the campus. The goal of this project is to create a centralized web application 
where students, as well as, faculty, staff and visitors can connect to post about any events taking place around campus. Our team will 
be developing the web application “Campus Snapshots” to serve this purpose. 

Campus Snapshots will be an application which could be accessed through a personal computer or mobile device using all major browsers 
like, Safari and Google Chrome. The main purpose of this application will be to serve as a place where individuals can report instant 
snapshots of any issues happening around campus such as, leakage in a classroom, broken A/C, etc. These real time snapshots will consist 
of images or videos along with a description and will appear instantly on our web page in order to alert university administrators of the 
problems that need fixing. Administrators will then be responsible for verifying if the claims are accurate and providing status updates 
for these claims until they are resolved. 

Due to the various social activities that take place around campus, our website will also serve as a means of sharing posts about fun 
events. People can interact by commenting on each other's posts and having the ability to share posts with friends. In order to ensure 
a safe online environment, we will require users to register for personal accounts to be able to add/delete their posts and chat with 
friends and/or administrators. Other features like checking for the weather and searching for specific events within the site will be 
implemented in order to create a better user experience. Ultimately, we plan to develop a user friendly and easy to navigate site that 
will aid in keeping our university in great shape while providing a means for everyone to communicate and engage with one another.


## 2. Competitive Analysis

*Site Comparison Table Image
  
Campus Snapshots will have the ability to upload instant images and videos like our competitors, Instagram and Snapchat. We will use a fluid chat system, implement content monitoring and use a system to block/ban false comments and contents similar to Facebook. Students will also be able to search for events and friends. However, we will add a weather system to alert students of major environmental threats which isn’t an option offered by any of our competitors.


## 3. Data Definitions

1. Event: Image or video posted by site users along with descriptions to report campus issues or social activities. <br>
&nbsp;&nbsp;&nbsp;&nbsp;-Images must be in .jpe or .png format with a maximum size of ______ MB <br>
&nbsp;&nbsp;&nbsp;&nbsp;-Videos must be in .mp4 format with a maximun size of ______ MB 
2. Power User: Administrative user in charge of keeping track of reports to update their status and monitoring overall site.
3. User: Student, professor, faculty, or other user able to create an account and post events/comments on site. <br>
&nbsp;&nbsp;&nbsp;&nbsp;-Must provide first and last name, email, username, password, nickname, date of birth, gender, major (if applicable), and security questions/answers for account recovery. <br>
&nbsp;&nbsp;&nbsp;&nbsp;-May add profile image with a maximum size of ______ MB
4. Role: Power vs Regular user
5. Verified: Posted event has been verified by power user as credile or appropriate.
6. Resolved: Posted event pertaining to an issue has been fixed and marked as solved by power user in order to notify all other users. 


## 4. Overview, Scenarios and Use Cases

User Stories:

1. I as Power user need verification service to be able to achieve the goal of verifying events 
    posted by users.
2. I as Power user need Push Events service to be able to achieve the goal of posting new events 
    as school’s events.
3. I as Power user need Post Managing service to be able to achieve the goal of deleting and 
    editing system events and force deleting fault events from users.
4. I as Power user need Blocking service to be able to achieve the goal of blocking fault users.
5. I as Registered user need Posting service to be able to achieve the goal of posting new events.
6. I as Registered user need Post Managing service to be able to achieve the goal of deleting and 
    editing my posted events.
7. I as Registered user need Post Sharing service to be able to achieve the goal of sharing 
    interested events.
8. I as Registered user need Post Commenting service to be able to achieve the goal of adding 
    comments in interested events.
9. I as Registered user need Post Searching service to be able to achieve the goal of browsing and 
    searching for events.
10. I as Registered user need Profile managing service to be able to achieve the goal of editing 
      my profile.
11. I as Registered user need Friend service to be able to achieve the goal of browsing, searching 
      and adding my friends.
12. I as Registered user need Message/Chat service to be able to achieve the goal of talking to 
      my friends and online admins.
13. I as Non-registered user need Register service to be able to achieve the goal of register and   
      become a member.
14. I as Non-registered user need Post Searching service to be able to achieve the goal of 
      browsing and searching for events.
15. I as Non-registered user need Message/Chat service to be able to achieve the goal of talking 
      online admins for help.


*Use Case Diagram Image
  
  
## 5. High-Level Functional Requirements

1.	Registration:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.1.	A user shall be able to make an account. [1]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1.2.	A power user shall be able to make an account not by the registration page but by letting whoever responsible for the website put them in the database. [1]<br>
2.	Recover Access: <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.1.	A user shall be able to answer security questions while register for an account in case of forgot access information such as username and/or password. [1]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.2.	A user shall be able to find his/her account in the recovery page with input information. [1]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2.3.	A user shall be able to reset password after answer correctly the security question. [1]<br>
3.	Access: A user shall be able to login and logout after registered. [1]
4.	Post Event and Write Comment: A user shall be able to post event and write comment. [1]
5.	Delete Event: A user shall be able to delete his/her own post. [1]
6.	Edit: A user shall be able to edit his or her post, comment, and profile. [2]
7.	Verifying Event: A power user shall be able to label a post verified or not verified. [1]
8.	Event Status: A power user shall be able to update the status of a report submitted by user. [1]
9.	Force Remove Event: A power user shall be able to delete anyone’s post if it is wrong or untruthful. [2]
10.	Block User: A power user shall be able to block/ban a user if necessary. [2]
11.	Search for Event: A user shall be able to search for posted events. [2]
12.	Video Event: A user should be able to post a video event. [3]
13.	Friend: A user should be able to make friends and have a friends list. [3]
14.	Sharing: A user should be able to share a post event to his/her friends. [3]
15.	Chat: A user should be able to chat with his or her friends and admins. [3]
16.	Weather: A user should be able to check for the weather within the web page. [3]
17. Calendar: A user should be able to check for the date in the calendar section. [3] 




## 6. List of Non-Functional Requirements

1. The website shall run on at least 3 major web browsers.
2. The user password shall be at least 8 characters including 1 uppercase, 1 number, 1 special 
    character, and no spaces. 
3. The system shall send an email to the user to verify the email address after registration. This 
    email address is for the user to recover their account if necessary. 
4. The system shall have 3 security questions for the user to answer during the registration 
    process. 
5. A user shall be able to access his/her own account right after email verification.
6. A user shall be able to use all the website functions without prior training.
7. User data shall be stored in 1 database. 
8. The language in the website shall be English.
9. The website shall be rich in content.
10. The user’s post shall be shown within 3 seconds. 
11. A user shall be able to see status of submitted reports.
12. A user shall be able to scroll through webpage and see general content without logging in.
13. User password shall never viewable at any point
14. The system shall achieve 99% up time.
15. The system shall not be shut down for maintenance more than once in 2 days. 
16. The time zone shall be obvious to the user on each post.  

Note to proofreader: I added a few number quantity to our previous requirements and added #13-16. 

## 7. High-Level System Architecture and Database Organization

Software products and Tools: Brackets, Notepad++, Putty, WinSCP, FileZilla, GitHub, etc <br>
Languages and Systems: English, HTML, PHP, MySQL, Linux, Windows, MacOS, Mobiles , etc<br>
APIs: Calendar, Weather<br>
Supported Browsers: Chrome, Firefox, Opera, Safari, Microsoft Edge, Internet Explorer<br>
Frameworks: HTML, PHP, CSS<br>

Database Organization<br>

*Add new information based on M3 instructions


## 8. High-Level UML Diagrams



## 9. Identify Key Risks and Actions


