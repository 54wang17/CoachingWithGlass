Coaching with Glass
===================

Introduction

The goal is to develop software applications for a website and Google glass to administer generic templates to execute tasks and activities in different contexts. In spite of the generic nature of the solution proposed, in order to exploit and learn about  wearable computing main features, it is mostly intended to support activities in environments where users would require both hands and to be moving.

These models can be used to defined tasks in areas such as education, training (how-to, installation-setup, etc.) , technical support, gaming, cooking, and others contexts where the user will required a free-hand device to operate.

The framework is a simple architecture that supports five main concepts: users, tasks, activities, Assignments and runs (on Glasses).  The content of these tasks and activities is somehow out of the scope of this project, as the main goal is to define a generic template for different scopes. Software and data Interfaces with other software applications  (content management) can be specified to feed the target system and populate the templates maintained in the application.

A task has a purpose, a description, a list of components, prerequisites and a number of activities that should be all executed sequentially to complete the task.

An activity is each step within a task; it has a name, an objective and a description of how to achieve the purpose of the activity. The content of each activity could be an image, short video, audio, text, or a combination of these.

Users are individuals using Google Glasses to complete tasks assigned to them.

Assignments are tasks assigned to users that should be completed within a period of time.

Runs are records of users executing tasks and the feedback collected from them. 

The user can just play the content of the activities in the glasses, as in a demo mode; or enter in execution mode, where the glassware will require some feedback when each activity is completed. The feedback can be photos or a piece of video and/or audio taken with the glasses, or plain text, that can be generated using ASR, automatic speech recognition. All these feedback will be sent back to the application server for analysis and storage. 

Object Model - Overview

(to be expanded and detailed, will use UML notation)


Main use cases and scenarios

(to be specified) 

Define Tasks and Activities (website)
Create and Maintain users (website)
Generate Content for Tasks (website)
Define assignments, assign and schedule tasks to users. (website)
Browse scheduled assignments by user. (website + glass)
Execute task in “demo” or “simulation” mode. (glass)
Execute task in “production” mode. (glass)
Collect and assignment execution feedback (website)


Packages 

(to be specified, to divide the work and organize team development) 

Users Administrator
Task Content and Interfaces Manager
Assignment Coordinator
Glassware Controller
	Glass content handler
	Glass task handler
	Glass user feedback handler
	Glass coordinator


Proposed  action plan: Project Phases 

Due to the size of the proposed target application, the project would be very difficult to be completed within the estimated time frame with the available resources. So the project is divided in phases.  I think that if the team manages to accomplished the goals of phase 3; a nice, operational application would be functional, and a significant amount of experience and usable code will be produced in GDK.



Phase 1: Glass: Task Demo Execution 

Build a simple application in glassware that displays a sequence a steps (activities) simulating a task defined in the system. There will be one task and a number of activities displaying their content. Implement controls like stop, pause/resume, play again. Use a reference the game “Charades” available in the samples from Google GDK package.

Manually upload a set of files in the Glass device to test the sequencing of activities and displaying the content of the different file types: text, audio, pictures and video, and combinations.   

Phase 2: Glass: Task user feedback process 

Add user actions to each activity. After playing the content of an activity, Glass will allow the user to perform one or several actions: record audio, with the option of generating text using ASR features, take pictures or record a video. 

Phase 3: Glass / website: basic communication: data sharing 

Setup a site with basic web services (html) to submit the files to be processed in Glass. Send the user actions recorded in Glass back to the website. 

Evaluate the options of playing tasks/activities in Glass in on-line mode: connected to the Internet and downloading/playing/uploading files “real time”; or consider an off-line solution, having the files stored in the Glass external storage, execute them without an internet connection, and providing features to receive/submit the files when an internet connection is established. 

Phase 4: Website: database deployment: users, tasks, activities, assignments

Implement a database behind the website (using MySQL?) to manage the application. Provide some data entry tools to populate the tables. Explore using Google Mirror API to generate a static card in the Glass device when a new assignment is created for a user. 

Phase 5: Glass: UX refinement    

Workout the layout of cards and user interactions in Glass, look into Google Glass design principles, guidelines and best practices to improve the quality of the user experience running the application.

Phase 6: Glass / website: complete data sharing interfaces and sync mechanisms.

Configure the website to check the schedule of assignments and send messages to users, generate Static Cards in Glass and allow users to launch the application to execute tasks. Submit data from Glass website with the user feedback files and display the content in the website to modify the status of the assignment as “completed”

Phase 7: Website: layout, user interfaces, access control.
Phase 8: Glass: user management, timeline updates, card generation. 
Phase 9: Website: content management, interfaces with other sourcing apps.
Phase 10: Testing in different scenarios.   


Further development 

Interacting with other glass users while running a task. 
Streaming live video on demand
Geo-location features. 



Challenges:
how to display generic text
how to display generic pictures (like video and audio plugins do)
be able to pose question and accept head shake (YES/NO).
