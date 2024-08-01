# Feeds
#### Distinctiveness and Complexity
In CS50's Web Programming with Python and JavaScript, we have learned how to make web applications with the Python Django Back-End Web Framework and JavaScript Front-End Web Framework; however, to gain experience with these technologies, Projects 0 through 4 required distinct and complex feature of these frameworks to be used to achieve interesting applications that are ubiquitous to modern society in the 21st century. With respect to the themes of CS50's Introduction to Computer Science and Web Programming with Python and JavaScript of computer science and society, I have taken Projects 0 through 4 and created a web application that integrates some features of these applications ported to the context of addressing a fundamental issue that arises in the infomation age. The Internet contains zetabytes of infomation; however, the human capacity to parse infomation remains fixed. Therefore, the Final Project is a perfect opportunity to create a simplified web feed reader application, allowing people to subscribe to many web feeds of websites and gathers the infomation of these websites for a simple viewing experience. If the Internet made possible for Wikipedia, Commerce, Mail, Networking Applications, then Feed Readers are the next great abstraction that makes the Infomation Age more accessible to many more people. In particular, my application enables users to make profiles about themselves, feeds to subscribe to web feeds, and randomly check out other feeds of different users. The implementation of these features borrows from the concepts introduced in Projects 0 through 4; however, designed to solve ultimately different problems. The purpose of the Feeds application is to bring infomation from the Internet to the user; however, this requires a complex system that makes interfaces and databases to store data on users and their profiles, feeds and their methods of interaction, and items to populate feeds over the Internet.
#### Description
In CS50's Introduction to Computer Science, we learned how to program software; however, introduced many computer science technologies that are used in modern software workflows such C, Arrays, Algorithms, Memory, and Data Structures. These are abstractions that provide more machinery to solve problems; hence, choosing a web application that utilizes the tools of Python and JavaScript are important. CS50 Feeds can be simply viewed with the Python Django Models, Views, Templates (MVT) Framework for the Back-End Server and JavaScript Event-Driven Framework for the Front-End Client with BootStrap providing third-party styling for the HTML structure of the application.

With respect to the Python Django Framework, the workflow of the application is as follows: User, Profile, Feed, and Item Models serve to store infomation on our users, their profiles, feeds, and its items in general. AbstractUser serves to instantiate a User model with hashed passwords though the Index route of the application that features dynamic registration and log in / out with JavaScript modals. Profile are rendered in the Profile route to display the user's profile. Feeds are made dynamically with JavaScript modals and automatically populates each feed with the items after creation as a Feed model instance. Items store the items of every feed that is created. I engineered a util.py file that uses the Python feedparser, schedule, threading libraries to get the items of the requested feeds and updates the feeds in the Feed model everyday at 07:30 using a separate thread. We define many views for each model that enables dynamic editing of the features of the application in the models per user. Specifically, we define views that will make and edit / delete Profiles, Feeds, and Items model instances. I associate a template to render for Index, Profile, Feed, Item per user that loads the content required in each view in the views.py file.

With respect to the JavaScript Framework, the scripting language defines event-driven logic that will provide interactive components for user experience, I designed thescripts to be included per template since each function was designed per specific tags in general. The biggest element for user experience is the inclusion of JavaScript BootStrap modals to collect infomation to modify Python Django modal instances dynamically with including extra routes. To streamline design, the index page incorporated a single-page application schemas given that the size of the content is relatively small compared to the rest of the application.

With respect to Python Schedule and Threading Libraries, the feeds that are created have the items automatically loaded as Item instances via the utils.py and use the schedule and multi-threading features to make seperate threads to update feeds on a schedule of 07:30 everyday.

With respect to the features of the application, Feeds offers a clean user interface that enables many to figure out the features in an accessible way with the design influenced by the layout of Project 4. I hope to add more features to give users more seemless usage to gather the infomation they want from a web feed with more interactivity such as adding a messaging feature that enables alerts for user to inform errors that occur, instead of using the JavaScript alert function to do so.

With regards to the HTML structure, the use of layouts incorporated a navigation bar at the top of the viewport and dynamically-generated the content via the views.py file with modal tags to incoperate that dynamic creation / editing of model instances throughout the application. The pages also links to the entries in each respect web feed items to view it on the site for the full experience.

With respect to the Profile models, I have designed descriptions field to enumerate a social networking profile page, but the purpose is to enable customization of the user, and allow other users to potentially understand why they subscribe to certain web feeds to get infomation, and learn from others when on their feeds.

With regards to the public and active fields of the Profile and Feed instances, user can private their instance from public view via the random view, which allows people to view their own feeds or others at random.

Many users will find that the design and implentation is minimal, but the vision of the application is to grow to include more interactivity per user in the future with new features that may incorperate AI technologies.

#### Run
In order to use CS50 Feeds, we just need to run the application as a standard Python Django project.
