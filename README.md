Team Name:

 DotsTech
 

Proposed Level of Achievement:
  
Apollo 11
 
A web application that facilitates communication during Dots Forums.


Setting up of Dots Forum’s web application:

Clone the repo in this link https://github.com/WM71811/orbital.git
Install Node.js 
RUN “npm install” in termial
RUN “node app.js” to start the server, ensure not using “NUS_STU” wifi (Wireless@SG is a possible option)
Navigate to localhost:3000 to try out our prototype 


Motivation

Partnering with Dots Forum, which is a student start-up company based in Beijing, China, we aim to build a powerful online web application for the forum. We aspire to connect students from prestigious universities in China to promising Start-up companies and provide them with the most updated industry information. Dots Forum will serve multiple stakeholders and we will build its web application to facilitate the transmission of information. 

Our web application will provide venture capital with the information of promising startup companies; provide students and school alumni with social networking channels with industry experts and provide start-up companies with recruiting channels in top universities.
 

Aim
 
Our mission is to make an web application which include an online forum to share information that would facilitate the bonding and communication among students, alumnus and start-up companies of the related schools. 

The bonding will be facilitated by both online and offline channels. Our web application will serve as the online channel and the physical Dots Forum (planned to take place in July annually) will serve as the offline channel. The online forum will complement and disseminate information about the physical forum to ensure a large publicity outreach. 

Our application may also serve as a platform to gather question, feedback and advice from users as well as industrial experts if we are able to build and maintain these features.
 

User Stories
  
1.As a student who has insufficient information on employment opportunities especially in start-up companies, I want to be able to look at the good questions and answers and be aware of possible internships.
 
2.As a student who is seeking employment, I want to be able to connect with alumnus and start-ups through the forum by asking questions and communicating with them.
 
3.As an alumni, I want to be able to see what the startups are doing and gain insights on current trends, be it technological or business-related evolvements.
 
4.As a employee in a startup company, I want to be able to connect with students and alumnus who has an interest to cooperate or join our company.

5.As a venture capital associate, I would like to see which start-up companies are attracting the most number of top university graduates as it is a sign of good ability to generate quality products in demand.
 

Scope of Project

A Web-based forum, with token-based authentication, that will provide question-and-answer functionality and allow for posting of information including recruitment information. 

An About Page that introduce to users the basic functionality of our application and inform them of our mission and vision. An Promotion Page that inform the users of the offline forum and recruitment. 

A Contact Page listing all our partner companies/universities including all industries so that our users will be able to contact their interested companies. Users identified as "company" can add contacts in the contact page.

Front end design and UI interaction improvement. 


- Features completed in Milestone 1
     1. Login/Sign Up
         Users can register with their email account and set up their username and password. The "Introduction" field will require them to fill in whether they are of type "student" or "company." Only users identified as "company" can add contacts in the contact page, while users identified as "students" cannot. Users who does not repeat password correctly, or fill in repeated email addresses that have been registered will receive an error and need to go back to the previous page to try again.

         Users completed registration are logged in automatically. For users who need to login after registering an account previously, they can login by clicking the "Log In" button in the top bar and fill in their email address and password.


     2. Edit User Profile
          Users can edit their user profile by changing their email address, name and password. Due to authentication process, they need to input a different email address each time.


- Features completed in Milestone 2
     3. Create, show post and comment
          Users can create new posts and comments after logging in. After logging in, they can click the “Ask Question” button in the top bar. A form will appear as they click the button, and they can fill in the form to create a new post. 
Comments can be created by clicking an individual post in the index page, and then scroll down the individual post page to add a comment.


     4. About Page
         The About page introduces to users the people and story behind Dots Forum and our vision. It can be accessed by clicking the "About" button in the top bar.

     5. Contact Page
          The Contact page enables interested parties/individuals to reach the partner schools. It can be accessed by clicking the "Contact" button in the top bar.

     6. Promotion Page
           The Promotion page publicise the physical Dots Forum and to encourage more people to join. It can be accessed by clicking the "Promotion" button in the top bar.


     7. Home Page
           The home page allows the users to see all the posts and they are able to click into each post to check the post content and comments.s.






- Features completed in Milestone 3 and Bugs Squashed
     8. Delete, edit post and delete comment(bug squashed)
            This is a bug identified in Milestone 2 and is now completed in Milestone 3. The problem was with the edit and delete functions which cannot access the data due to some reasons. The bug is fixed as we work on the controller functions and the routes. 
The users can edit or delete a post after entering an individual post page, which is the page shown after clicking the name of a specific post in the home page. The “edit post” button redirects users to the page to edit the post, while the “delete post” button allows the user to delete a post. The comments can also be deleted by clicking the delete button.
            This is necessary as it ensures that users are able to edit posts to better suit their needs and delete them if they would like to.



     9. Showing only comments related to a single post in the individual post page(bug squashed)
	This problem is detected during Milestone 2 testing, and is thus listed in the developmental plan for Milestone 3. The problem was that the comments and posts are not related to each other previously, and thus in Milestone 3 we addressed the problem by creating new attributes in the schemas to relate the posts to comments and building additional functions. 
By implementing the one-to-many relationship between post and comments, we make sure that comments created in a particular post page are only shown in that post page, but not in other post pages.
            This is necessary as it allows for better communication between users who questioned and users who answered the question, since they could know which comment is related to which post.

     10. Search posts function(Bug Squashed)
           The search function is debugged in Milestone 3 so that it could now work properly. The bug is due to the fact that the search function does not use optimal methods, and is thus rebuilt with regex.
 The search bar allows users to search the titles of the posts. If users input "1", for example, then if the title of the posts are "1", "13", "2", then the search result would be "1" and "13". This is done by implementing regex. The search results can be clicked to be redirected to the individual post pages.
            This is necessary as when the number of posts is large, searching allows for efficiency in finding the posts that users have interests in.

     11. Ability to add contacts by part of the users only
            The contacts can be added by users who are identified as "company", but not those who are identified as "student". This ensures that only the users belonging to certain companies can edit the contact page. The contacts can be added by clicking the "add a contact" button which redirects the users to a form to add a new contact. 


     12. Show and delete contacts
             The contact page shows all the contacts added. The added contacts can be clicked, which redirects users to individual contact pages to see more information, in which page users can also delete the contact.


     13. Ask Organizers function
             The ask organizers function allows users to ask organizers in case they have any questions. They can click the button at the sidebar which redirects them to a new form page, and the questions they submitted will be addressed by the organizers later.


     14. Only users who created the post can edit or delete the post/delete the contact
             This function allows users who created the particular post to edit or delete the post/delete the contact. This ensures that the post would not be deleted or edited by other users. Similarly, the contact will not be deleted by other users.

Problems Encountered 
 
We were not able to connect to MongoDB Atlas for quite some time and could not find the problem. The error is one of connection failure and despite we tried different ways such as connecting through Mongoose and Mongo Shell. After extensive searching, we found that the error is due to the embedded firewall property of the nusstu Wi-Fi, and resolved the problem by connecting to another data source (Wireless @ SG).(Milestone 2)
 
During the transfer of MySQL to MongoDB, as we were unfamiliar with the cloud server, we were not able to build our server and obtain the correct URL. We resolved this issue by learning about mongoDB using online resources and then built our cluster and database.(Milestone 2)
 
During the construction and instantiation of double CRUD functionality of the Forum page, we faced bugs such as not being able to see a comment posted and not being able to go to the correct pages (Promotion, About etc) . We debugged our app by carefully reviewing the controllers and routes and make necessary changes to fix the bugs.(Milestone 2)

It takes much time to create the Delete/Edit function, since firstly, the routes does not support “delete” but only “get”/”post”, and secondly req.params were empty. We tried multiple ways to see where the problem comes from and got it solved.(Milestone 3)

The relationship between posts and comments, the rule that only the user who created the post/contact can delete the post/contact, and also, for contact, the requirement that only users identified as “company” can create new contacts took quite some time to complete. The schemas for the data were edited multiple times to establish the relationships between the different types of data. We worked on the functions in the controller for quite much time to ensure that the functions could work properly, especially we took much time to discover that the structure of the function is very important in order to work properly.(Milestone 3)

The search function was not working at first, and we try to rebuild the search function using regex. Thus we learnt about regex and how to integrate it with Mongoose and Node js to enable search to work properly.(Milestone 3)


Things Removed
We removed the name section when creating a post or a contact, and user’s registered username would be inputted as the “name” attribute of the post or the contact. This is to ensure that users will not be confused if they forget which name they use when they create a post or a contact.


User Testing
We tested the application on our own by registering different accounts to see how each function works and if they work fine.
We invited our friends to test the application on their own computers and received feedback, which have led us to develop some of the features in Milestone 3 as mentioned above.
We invited our seniors to test the application on their laptops and received feedback as well.



Developmental Plan

S/N
Task
Expected Completion Date By:
By Milestone:
1
Creation of Login page
-   	Username Input
-   	Password Input
-   	Sign-up button
03/06/20

Completed
1
2
Creation of Sign-up feature
-   	Set user profile
06/06/20

Completed
1
3
Creation of Forum page
-   	Basic instruction on how to participate in the Q&A process
09/06/20


Completed
2
4
Creation of About page
-   	Description on what the Dots Forum and the web application is about
11/06/20

Completed
2
5
Creation of Contact page
-   	Order in terms of contact type
-   	Description


13/06/20

Completed
2
6
Creation of Promotion page
-   	Description on when the Dots Forum will be held and information regarding recruitment
15/06/20

Completed
2
7
Instantiation of Forum page
-   	Read a question and the answers
-     Create posts and comments   
--        List of questions
-     Search operations
18/06/20

Completed (Search functionality to be developed)
2
8
Connect current features
-   	Link the different pages through buttons
-   	Quality check
22/06/20

Completed
2
9
Build user profile
-   	Features including user’s credentials and past experience, based on feedback from the peers.
-    Update user’s login credentials using the page 
23/06/20

Completed
2
10
Build Interactive System
 -   	Enable users to provide feedback and consult organisers regarding the Dots Forum 
25/06/20


Completed
2
11
Continue to develop the edit and delete functions 
-   	Enable owner of a post to update its content
            -       Enable owner to delete a post for personal reasons
           -  Enable users to delete comments     
08/07/20

Completed
3
12
Resolve the one-to-many relationship between a post and comment 

Hide unrelated     comments when one is viewing a certain post
           
16/07/20

Completed
3
13
Allow “ask organizers” function to work
Create new schema, pages and functions to make the function complete

18/07/20

Completed
3
14
Enable only users registered as “company” to add contacts in the contact page
 Also allow the user who created the contact to delete the contact if they want to

20/07/20

Completed
3
15
Develop search function for post titles
 Allow users to search for posts they may have interest in using Regex

21/07/20

Completed
3
16
Ensure only users who created the post can edit/delete the post
22/07/20

Completed
3
17
Improve user design
design pages to signal error messages and redirect users to home pages

23/07/20

Completed
3
 
