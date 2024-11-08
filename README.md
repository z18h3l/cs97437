java c
CMPSC 431W
Database Management System
Assignment 4
Conceptual  Logical Database Design
Assigned: Oct 9, 2024
Due: Oct 25, 2024. 11:59:59PM
ObjectivesThe purpose of this assignment is to go through some exercise of conceptual database design (ER modeling), logical base design and schema refinement driven by database design theory.  Specifically, this assignment will help you practice your knowledge on the following points:
•  How to draw a ER diagram for general applications
•  How to apply different constraints in ER diagram.
•  How to translate and ER diagram into a relational database schema.
•  How to find and process functional dependencies (FDs).
•  How to decompose a relational schema so that it can fit into BCNF.
Part I. ER Modeling  Relation Translation [60pts]1.  [24pts] You have been hired by Wizards of the Coast to create a database mapping rules and concepts from Dungeons and Dragons.   You will be given some situations concerning different rules, and for each you should draw an ER diagram for it using the notation taught in our class (assuming no further constraints hold).
For each, you can introduce additional entity sets and relationships as necessary.  Note that you should be able to enforce all the constraints in the ER diagram directly without any text description.
(1)  Every Player must belong to some Species.
(2)  Each Player can join multiple Classes. Each Class the Player joins has an associated level.
(3)  Each Love Interest is romanced by exactly one Player. Players may romance multiple Love Interests
(4)  Each Player must have one Boss who they rival. A Boss can rival exactly one Player.
(5)  A Dungeon Master may host the same Campaign for multiple games on different days.  Each game must be hosted by exactly one Dungeon Master and run on exactly one Campaign. All games with its date must be recorded.
(6)  Same as (5) but some games may be hosted by a group of Dungeon Masters rather than one. Besides, we only record the latest date of a game for a particular group of Dungeon Masters hosting a specific Campaign. That is, if the same group of Dungeon Masters (DM1 and DM2) host the same Campaign (C1) twice, only the latest game date will be recorded. Meanwhile, we need another record for another group of Dungeon Masters (DM3 and DM4) hosting the same Campaign (C1).
2. [36pts] Assume you are helping design a database for the fictional world for a film studio. This database will include information about basic information of the locations, people,
•  Information about Character includes their name, their ID, and their favorite food.  Each Character must be either CGI or a Human (but not both). Each CGI character should have a type (such as Dragon or Zombie). Each Human should have a hair style.
•  Information about Actors includes their employee ID, name, salary, and address. An Actor can play at most one Human Character.  An Actor can pla代 写CMPSC 431W Database Management System Assignment 4 Conceptual & Logical Database DesignProlog
代做程序编程语言y multiple CGI Characters.  (For example, an Actor can play 3 CGI Characters, and 1 Human). Each CGI character must be associated with some actor, while multiple actors can play the same CGI Character. Each human character must have exactly one associated actor.
•  A Credit is an instance where a pair of CGI Character and Actor are associated together, representing the instance of an actor playing a particular CGI character.  A credit also stores the role of the credit (such as “Voice” or “Puppeteer”).  Each unique pair of CGI character and Actor can only have one credit. That is, you cannot have the same actor taking credits of a CGI character as different roles.
•  A Episode consists of multiple credits.  A credit may appear in more than one episode. An episode also contains a set of Human Characters which appear in the episode. A Human character may appear in more than one episode.
(1)  Draw an ER diagram of the database you designed fulfill all the requirements above.  You should capture all constraints without any text in the diagram, except for covering/overlap constraints for class hierarchy (if necessary).
(2)  Translate your ER diagram into a relational database schema. Specifically, you should write down the DDL statement to create each table capturing all information and constraints given in the diagram. You can decide data types for different attributes as long as they are reasonable.  For foreign key constraints, you do NOT need to specify referential actions (e.g., ON DELETE, ON UPDATE).
Part II: Logical Database Design  Schema Refinement [40pts]
1. [15pts] Consider a table instance with schema R(A,B, C,D, E) as below:
A
B
C
D
E
1
2
3
4
1
4
2
3
2
1
5
3
3
5
3
1
2
4
4
2
3
4
4
1
5(1)  Which of the following dependencies can you infer that does not hold over schema R. Justify your answer for each FD using data from the given instance.
(a) A → C; (b) CD → A; (c) ABD → E
(2)  Find all the non-trivial functional dependencies that does hold on the given instance and only one attribute on the left hand side.2. [10pts] Consider a relational schema R(A,B, C,D, E , F) and a set ofFDs: A → C, BD → A, and EF → D. Decompose R into BCNF. Show all of your work and explain, at each step, which dependency violations you are correcting. You have to write down a description of your decomposition steps.3.  [15pts] A set of attribute X is called closed (with respect to a given set ofFDs) if X+  = X.  Consider a relation with schema R(A, B, C, D) and an unknown set of FDs.  For each close attribute set constraint below, find a set of non-trivial FDs over R that is consistent with it.
(1)  All sets of attributes are closed.
(2)  The only closed sets of attributes are {}, {A,B, C,D}.
(3)  The only closed sets of attributes are {}, {A,D} and {A,B, C,D}







         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
