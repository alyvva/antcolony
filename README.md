# antcolony
#Below is pseudocode I created for an Ant Colony I created.

Class 1: Main

•	New object to link Tester class with Main class

•	startingColony.variablename(); to interact with Tester class

•	JOptionPane.showMessageDialog(); to show user what they input for each question asked

"Your starting size colony is _____."

"Your name is _____."

•	startingColony.lifespanMethod(); so lifespan method will show in the main

•	startingColony.expansionMethod(); so expansion method will show in the main

•	Final # of Ants

o	JOptionPane.showMessage(); startingColony.getSize (final population size)

Class 2: AntColonyTester

•	Import javax.swing.JOptionPane & import java.util.Random 

•	String Variables

o	First declaration of what variables I will need

o	Queen’s name, colony name, caretaker’s name, starting size of colony, days fed, number of queens bred, lifespan method, expansion method

Getter/Setters

o	Allows me to manipulate user’s input and give them results based on their initial responses

•	Lifespan Method

o	Relevant variables are days fed, number of queens bred and starting size

o	Use Integer.parseInt(); to convert String variables into manipulative integers

o	2 if statements

	First if statement: If user gives colony food for more than 10 days, one queen will die and population will be cut in half 
	int lifespan = bred – 1; //minus one queen
	int population = size / 2; //50% of colony dies
	Second if statement: if user gives colony food for less than 10 days, queen amount stays the same but the population triples in size
	int queen = bred; //queen stays the same
	int population = size * 3; //population triples

o	JOptionPane.showMessageDialog();

	Depending on user’s input, use JOptionPane to reveal new amount of queens and new population size.

•	Random number generator

o	To help with expansion method
o	(If user chose yes to expand) 50% chance a new queen with the name the user chose + 2.0 – So I used a generator from 1-10, with the first 5 numbers representing no new queen to be born and the last 5 numbers to represent a queen 2.0 to be born. 
o	(If user chose no to expand) Only 10% chance of a new queen being born. If user received the number 1, then a new queen 2.0 is born. If not, then no new queen is born. 

•	Expansion Method

o	Have user’s input (yes, no) from JOptionPane.inputMessageDialog();
o	If they choose yes, 50% chance a new queen will be born
o	If they choose no, only 10% chance a new queen will be born, along with the new queen being named the original user’s input for a queen name with “2.0” added
o	Use if else statement and random number generator to show either scenario
