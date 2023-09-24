# Class-ER-Diagram-
Pace Wise assignment 1 of drawing class ER diagrams
1st question:Suppose you are given the following requirements for a simple database for the National Hockey League (NHL): 
the NHL has many teams, 
each team has a name, a city, a coach, a captain, and a set of players, 
each player belongs to only one team, 
each player has a name, a position (such as left wing or goalie), a skill level, and a set of injury records, 
a team captain is also a player, 
a game is played between two teams (referred to as host_team and guest_team) and has a date (such as May 11th, 1999) and a score (such as 4 to 2). 
Construct a clean and concise ER diagram for the NHL database using the Chen notation as in your textbook. List your assumptions and clearly indicate the cardinality mappings as well as any role indicators in your ER diagram.

Team has N player and 1 player is part of only one team(1:N)
Game is played between two teams, has realtionship attributes of host team,guest team,score and date.
Injury records is a weak entity because it is dependent on player i.e., it's key is a player ID.
Each team has a captain(1:1) and captain is also a player(1:1)-not all players are captains.



2nd question:Construct an E-R diagram for a car-insurance company whose customers own one or more cars each. Each car has associated with it zero to any number of recorded accidents

Cars are owned by owners(1:N), Each car is owned by single owner. owner can have more than one car.
Car has attributes like carID,brand,color,mfg date.
car is associated with accident records which is a weak entity, defined by the relation associated with which has an entity attribute of date and place.
customer has attributes such as customerID,name,address,ph number.


3rd question:Construct an E-R diagram for a hospital with a set of patients and a set of medical doctors. Associate with each patient a log of the various tests and examinations conducted.

Patient is monitored by doctors.Doctors can monitor more than one patient and patients can be monitored by more than one doctors(N:M)
Pateient has log record.Each patient can have more than one log record(1:N).
Patient contains attributes such as PatientID,name,disease,DOB and age(derived attribute).
Doctor has doctoID,name,qualifiication.
Log has LogID,test,test date,report,description.

4th question:A university registrar’s office maintains data about the following entities: (a) courses, including number, title, credits, syllabus, and prerequisites; (b) course offerings, including course number, year, semester, section number, instructor(s), timings, and classroom; (c) students, including student-id, name, and program; and (d) instructors, including identification number, name, department, and title. Further, the enrollment of students in courses and grades awarded to students in each course they are enrolled for must be appropriately modeled. Construct an E-R diagram forthe registrar’s office. Document all assumptions that you make about the mapping constraints.

One course has many course offerings(1:N).
Student enrolls in in more than one course(N:M).
Instuctor can handle more than one course offering and one course offering can be take by many instuctors(N:M).
Enroll relation has relationship attribute grade, which monitors the students garde.

