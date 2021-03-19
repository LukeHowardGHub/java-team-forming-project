# java-team-forming-project
INSTRUCTIONS FOR RUNNING ADVANCED PROGRAMMING ASSIGNMENT

***General Information***
- students have had preferences and personalities etc pre-entered and are serialised, any entering of this information will override current forms 
- Student information was filled in by randomly selecting numbers of corresponding attributes, I acknowledge this is not true of a real world situation but I wanted to create students and teams with a random distribution of attributes and personalities, as such there is a larger amount of student conflicts than would normally occur

***Console Based User Input***
- To run this portion of the assignment, select the mainMenu class from the consoleDataEntry package
- options 1-3 will allow you to write company, owner and projects to txt file
- capture student personalities / student preferences will override already written students that were developed to test and run console/ GUI
- Shortlist projects will just re-shortlist the projects based on the already entered preferences 
- form teams will not show any projects to select as all teams have been formed already in order to develop GUI, serialised Teams are read in when the program starts. Commenting out
	line 35 will allow for the form teams option to be demoed
- team metrics can be viewed if pre-formed teams have been read in upon loading, otherwise user is not allowed to view team metrics until all teams are formed
- selecting quit option will cause all changes to students and teams to override existing objects, it is suggested to not do this so that pre-formed objects can be loaded into the GUI for demo

***GUI Version***
- to run GUI, select Main class from StudentSwap package and ensure JavaFX class path is loaded in and adjust run configurations as required
- GUI will load and suggestions will be made about student swaps to user on the console
- Each team metric thread is loaded with a collection of teams as formed from last use and will suggest swaps without the knowledge of swaps to improve other metrics
- Swaps under each metric must be implemented in order to achieve the potential stdev
- after each swap, teams are re-serialised so will be loaded in at the latest point if GUI is relaunched and new swaps will be suggested. Teams are also re-written to DB
- to look up student/ team, user must enter student id (s1,s12 etc for students, team1, team2 etc for teams) and select “get student” or hit enter
- to swap students, select the check box next to student ID and select swap, swapped student appear at the bottom of their new team
- undo will restore previous state of teams prior to swap, students still appear at bottom of teams and not in their original slot.
- error messages will occur if swap violates a hard constraint of team formation, user conflict message allows user to overrule swap despite conflict if they wish
- team metric graphs are updated after each swap and stdefv recalculated to reflect any changes
