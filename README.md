
						Restaurant Menu Voter (RMV)
						
_______________________________________________________________________________________________
Initial task description:

Design and implement a JSON API using Hibernate/Spring/SpringMVC **without frontend**.

The task is:

Build a voting system for deciding where to have lunch.

 * 2 types of users: admin and regular users
 * Admin can input a restaurant and it's lunch menu of the day (2-5 items usually, just a dish name and price)
 * Menu changes each day (admins do the updates)
 * Users can vote on which restaurant they want to have lunch at
 * Only one vote counted per user
 * If user votes again the same day:
    - If it is before 11:00 we asume that he changed his mind.
    - If it is after 11:00 then it is too late, vote can't be changed

Each restaurant provides new menu each day.


Soultion and delivery bundles:

A solution is implemented using Java and MS SQL Server.

Deliveries:
	Design documents.zip	Design documentation including ER diagram for RVM database (in original SQLPowerArchitect format and also printed out as a pdf file).
	Source codes.zip:		RMV sql and java source files to review and standalone reuse. Principal source files are:
								Restaurant Menu Voter.sql					- SQL script to populate a MS SQL database by RMV tables and other objects. Also it populates Grade table by vote values and Report table by predefined reports. 
								org\largecode\rmvoting\RMV_Database.java 	- RMV implementation
								org\largecode\rmvoting\RMV_Exception.java 	- RMV-specific exception
								utils\JSON_Utils.java						- RMV-specific utils for JSON serialization/deserealization
								org\json\*.java								- 3-rd party JSOM library (see org.json);
	apache-tomcat wtpwebapps.zip 	Apache Tomcat distribution example 				- a demonstrational and testing web application for RMV (also includes a dedicated ReadMe.txt file and URL example).
	Eclipse projects.zip		Eclipse EE Mars projects being used for RMV testing purposes: 
									project "Restaurant Menu Voter" is a command-line application dedicated for unit testing purposes;
									project "RestaurantMenuVoter_JSP_test" is a web application used for unit and application testing purposes.
_______________________________________________________________________________________________

In case on any questions please contact Evgeny Lyulkov at
evgeny.lyulkov@gmail.com
Skype: Evgeny.Lyulkov 
