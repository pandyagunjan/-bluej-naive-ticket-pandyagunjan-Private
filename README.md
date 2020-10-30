# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

First you need to FORK this repo into your account, then you need to CLONE that foreked repo, the one in your account. 
When you are finished with your code, be sure to ADD/COMMIT and PUSH your code to your repo.

Use the URL from your repo as the submission to the portal. 

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1 - Done
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2 - Done
* What value is returned if you check the machine’s balance after it has printed a ticket?
[Answer] The balance is reset to 0 once the ticket is printed.

### Exercise 2.3 - Done
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior? [Answer] It adds up to 'balance' and 'total' and never refunds.We can buy ticket on not matching to price.
	* What happens if you insert too much money into the machine – do you receive any refund? [Answer]  No
	* What happens if you do not insert enough and then try to print a ticket? [Answer]  It displays "Ticker price : 500 cents. Your total is 0" and we can still get the ticket.

### Exercise 2.4 - Done
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5 - Done
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?
[Answer] : Based on the price we enter during the instance creation , the printed ticket displays the corresponding price .

### Exercise 2.6 - Done
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.
[Answer] : 
public class Student 
{
//inner part of class
}

public class LabClass
{
//inner part of class
}

### Exercise 2.7 - Done
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

[Answer] No, it throws 'Identifier expected' if we swtich the words.

* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram? [Answer] Yes , there are slant lines on class representing there are errors.
	* What error message do you get when you now press the compile button? [Answer] It displays 4 errors 
	1) <Identifier> expected (displayed twice)
	2) illegal start of expression
	3) illegal method declaration , return type required - Error on constructor.

	* Do you think this message clearly explains what is wrong? [Answer] Yes, the first one as it expects the reserved word 'class' next to the className {} .

### Exercise 2.8 - Done
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.
[Answer] Yes, its fine to leave the word public.No error is displayed.

### Exercise 2.9 - Done
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.
	[Answer]
	Fields : Price , balance , total ,ticketNumber (All declared as 'private Integer')
	Constructor : public TicketMachine(Integer ticketCost) { //Initlations of the fields done here}
	Methods : getTotal(),getTickerNumber(),getBalance(),insertMoney(),calculateTotal(),incrementTicketNumber(),showPrice(),printTicket(),getPrice(),

### Exercise 2.10 - Done
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?
[Answer] Yes, the constructor has same name as the Class.
### Exercise 2.11 - Done 
* What do you think is the type of each of the following fields?

```java
private int count; [Answer] : int data type
private Student representative; [Answer] : Instance of class 'Student'
private Server host; [Answer] : Instance of class 'Server'
```

### Exercise 2.12 - Done
* What are the names of the following fields?

```java
private boolean alive; [Answer] : alive
private Person tutor; [Answer] : tutor 
private Game game; [Answer] : game
```
### Exercise 2.13 - Done

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?
* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are possible? [Answer] : Yes, visually it shows slant line on class diagram indicating possible errors.
	* Check by pressing the compile button to see if there is an error message. [Answer] : <Identifier> expected .error is displayed
	* Make sure that you reinstantiate the original version after your experiments! -OK

### Exercise 2.14 - Done
* Is it always necessary to have a semicolon at the end of a field declaration? [Answer] : Yes
* Once again, experiment via the editor.[Answer] : Throws error ';' expected
* The rule you will learn here is an important one, so be sure to remember it.-Ok


### Exercise 2.15 - Done
* Write in full the declaration for a field of type `int` whose name is `status`.
[Answer] : private Integer status;

### Exercise 2.16 - Done
* To what class does the following constructor belong?
```
public Student(String name)
```
[Answer] : It belongs to class 'Student'
### Exercise 2.17 - Done
* How many parameters does the following constructor have and what are their types?
```
public Book(String title, double price)
```
[Answer] : It has 2 parameters , String for title and double for price.

### Exercise 2.18 - Done
* Can you guess what types some of the `Book` class’s fields might be?
* Can you assume anything about the names of its fields?
[Answer] :
class Book
{
	private String authorOfTheBook; //Author of the book
	private String titleOfTheBook; //Title of the book
	private Integer price; //Price of the book
	private Integer barCode; //Barcode information
	private boolean fictionFlag ; //Fiction Or Non-Fiction flag
}
READ upto and INCLUDING section 2.15 of this chapter.
