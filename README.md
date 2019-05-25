# NaiveTicket

The second Objects lab, from the BlueJ book's second chapter.

Look for the [Chapter 2 file](./doc/BlueJ-objects-first-ch2.pdf) you need in the [doc](./doc) folder.
There is 35 pages of reading and exercises in the chapter.

Work through all these exercises. You edit this file with your answers for these exercises.

### Exercise 2.1
* Create a TicketMachine object on the object bench.
* Upon viewing its methods, `getBalance`, `getPrice`, `insertMoney`, `printTicket`.
* Use `getPrice` method to view the value of the price of the tickets that was set when this object was created.
* Use `insertMoney` method to simulate inserting an amount of money into the machine.
* Use `getBalance` to check that the machine has a record of the amount inserted.
	* You can insert several separate amounts of money into the machine, just like you might insert multiple coins or notes into a real machine. Try inserting the exact amount required for a ticket. As this is a simple machine, a ticket will not be issued automatically, so once you have inserted enough money, call the `printTicket` method. A facsimile ticket should be printed in the BlueJ terminal window.

### Exercise 2.2
* What value is returned if you check the machine’s balance after it has printed a ticket?

After buying a ticket the balance is 0, "zero" even if there had been more than required in the balance before.
*------------------------------------------------------



### Exercise 2.3
* Experiment with inserting different amounts of money before printing tickets.
	* Do you notice anything strange about the machine’s behavior?

The balance increases by the amount inserted.
*------------------------------------------------------



	* What happens if you insert too much money into the machine – do you receive any refund?

The machine takes all of the balance - no refund.
*------------------------------------------------------



* What happens if you do not insert enough and then try to print a ticket?

The machine prints a ticket and takes all the money in the balance, even if it is not enough.
*------------------------------------------------------



### Exercise 2.4
* Try to obtain a good understanding of a ticket machine’s behavior by interacting with it on the object bench before we start looking at how the `TicketMachine` class is implemented in the next section.

### Exercise 2.5
* Create another ticket machine for tickets of a different price.
	* Buy a ticket from that machine.
	* Does the printed ticket look different?


The price was lowered from 500 to 250.  With a balance of 300, a ticket was issued with a stsed price of 250 rather than 500.  The balance wes 0 even though their was 300 in the balance to start.
*------------------------------------------------------




### Exercise 2.6
* Write out what you think the outer wrappers of the `Student` and `LabClass` classes might look like – do not worry about the inner part.

public class Student
{   


}


public class LabClass
{



}

*------------------------------------------------------



### Exercise 2.7
Does it matter whether we write<br>
`public class TicketMachine`<br>
or<br>
`class public TicketMachine`<br>
in the outer wrapper of a class?

Yes, it matters.
*------------------------------------------------------


* Edit the source of the `TicketMachine` class to make the change and then close the editor window.
	* Do you notice a change in the class diagram?

I did not notice a change in the class diagram.
*------------------------------------------------------


	* What error message do you get when you now press the compile button?

1) Illegal method declaration.
2) < identifier > expected
3) the class is now named "public".
*------------------------------------------------------



	* Do you think this message clearly explains what is wrong?

No, it not the actual problem.
*------------------------------------------------------


### Exercise 2.8
* Check whether or not it is possible to leave out the word `public` from the outer wrapper of the `TicketMachine` class.

The Class compiles without the pubic declaration.
*------------------------------------------------------


### Exercise 2.9
* From your earlier experimentation with the ticket machine objects within BlueJ you can probably remember the names of some of the methods – `printTicket`, for instance.
	* Look at the class definition in Code 2.1 and use this knowledge, along with the additional information about ordering we have given you, to try to make a list of the names of the fields, constructors, and methods in the `TicketMachine` class.
	* Hint: There is only one constructor in the class.

Names of the fields
	price
	balance
	total
	ticketCost
	amount

Constructors
```java
public class TicketMachine
{
    public TicketMachine(int ticketCost)
    {

    }
}
```

Methods
	getPrice
	getBalance
	insertMoney
	printTicket
*------------------------------------------------------


### Exercise 2.10
* Do you notice any features of the constructor that make it significantly different from the other methods of the class?

"TicketMachine" appears twice
*------------------------------------------------------


### Exercise 2.11
* What do you think is the type of each of the following fields?

```java
private int count;
private Student representative;
private Server host;
```

count is a primative integer.
representitive is object.
host is an object.

*------------------------------------------------------


### Exercise 2.12
* What are the names of the following fields?

```java
private boolean alive;
private Person tutor;
private Game game;
```

alive is a primative boolean.
tutor is an object.
game is an object.

*------------------------------------------------------


### Exercise 2.13

In the following field declaration from the TicketMachine class<br>

```java
private int price;
```
does it matter which order the three words appear in?

Yes.
*------------------------------------------------------


* Edit the `TicketMachine` class to try different orderings. After each change, close the editor.
	* Does the appearance of the class diagram after each change give you a clue as to whether or not other orderings are possible?

Moving the type identifier makes the word "private" an int type. Other ordering are not possible
*------------------------------------------------------


	* Check by pressing the compile button to see if there is an error message.
	* Make sure that you reinstantiate the original version after your experiments!

There are compiler errors when the placement is changed.
*------------------------------------------------------


### Exercise 2.14
* Is it always necessary to have a semicolon at the end of a field declaration?

yes.
*------------------------------------------------------


* Once again, experiment via the editor.
* The rule you will learn here is an important one, so be sure to remember it.


### Exercise 2.15
* Write in full the declaration for a field of type `int` whose name is `status`.

private int status;

*------------------------------------------------------


### Exercise 2.16
* To what class does the following constructor belong?
```java
public Student(String name)
```
It belongs to the Student class.

*------------------------------------------------------


### Exercise 2.17
* How many parameters does the following constructor have and what are their types?
```java
public Book(String title, double price)
```
Two, title is a String and price is a Double.

*------------------------------------------------------


### Exercise 2.18
* Can you guess what types some of the `Book` class’s fields might be?

```java
private String title;
private String author;
private String publisher;
private Integer chapters;
private Integer pages;
```

*------------------------------------------------------


* Can you assume anything about the names of its fields?

See above.

*------------------------------------------------------



Work all Exercises from 2.19 to 2.58 that are **NOT** marked *Challenge exercise*.
READ upto and INCLUDING section 2.15 of this chapter.

### Exercise 2.19

 public Pet(String petsName)
  {
  	name = petsName;
  }


### Exercise 2.20
*Challenge exercise*


### Exercise 2.21

There is a difference in their names and the variables they return to the caller.


### Exercise 2.22

What is the current blance of the current traveler.


### Exercise 2.23

No, the method should still return the balance.


### Exercise 2.24

getTotal() is an accessor, also known as a getter, which returns the value of the Total field to the caller.


### Exercise 2.25

A MISSING RETURN error is issued.


### Exercise 2.26

getPrice() simply returns the price of a ticket.  printTicket() prints a ticket, increases the total by the traveler's balance and emptys the traveler's balance.


### Exercise 2.27

insertMoney() and printTicket() do not have return statements.  The type in their headers is void indicating that nothing is returned.  the two methods perform actions modeled on the physical world.


### Exercise 2.28

THe original balance was 0.  After inserting 100, the balance was 100.


### Exercise 2.29

The header has void as the return type.


### Exercise 2.30
```java
 /**
 * Return the price of a ticket.
 */
 public int setPrice(int newPrice)
    {
        price = newPrice;
        return;
    }
```


### Exercise 2.31
```java
  /**
  * Increase score by the given number of points.
  */
  public void increase(int points)
  {

  score =score + points;

}
```


### Exercise 2.32

```java
/**
* Reduce price by the given amount.
*/
public void discount(int amount)
  {

price = price - amount;

}
```


### Exercise 2.33

```java

public void prompt()
  {

System.out.println("Please insert the correct amount of money.");

}
```


### Exercise 2.34

```java

public void showPrice()
  {

System.out.println("The price of a ticket is " + price + " cents.");

}
```


### Exercise 2.35

The prices are different because there are 2 distinct instances of the tickeyMachine.



### Exercise 2.36

# price cents. 
would be printed.



### Exercise 2.37

# price cents. 
would be printed.



### Exercise 2.38

No.


### Exercise 2.39

The object does not ask for the ticket price.


### Exercise 2.40

```java

public void empty()
  {

total = 0;

}
```

No parameters are needed.
It is a mutator (setter).

### Exercise 2.41


```java

public void setPrice(int newPrice)
  {

price = newPrice;

}
```
This is a mutator.


### Exercise 2.42

Two different prices.



### Exercise 2.43

If an amout less than 0 is inserted an error message is printed and the balance is unchanged.


### Exercise 2.44

An error message will be issued if 0 is entered.



### Exercise 2.45

A boolean was used to determine if the shape was visible or not.



### Exercise 2.46

We checked the balance to make sure there was enough money to buy a ticket.  If so, we subtracted the ticket price from the balance and added it to total.


### Exercise 2.47

The balance could not go below 0 because balance was checked beforehand.


### Exercise 2.48

Many.


### Exercise 2.49

Integer saving = price * discount;



### Exercise 2.50

Integer mean = total / count;


### Exercise 2.51

if (price > budget) {
	System.out.println("Too expensive.");
}
else {
	
	System.out.println("Just right.");
}


### Exercise 2.52

if (price > budget) {
	System.out.println("Too expensive. I only have " + budget + " to spend.");
}
else {
	
	System.out.println("Just right.");
}



### Exercise 2.53

It zero's out the balance before making a refund.




### Exercise 2.54

balance = 0; does not execute.




### Exercise 2.55

public Integer emptyMachine()
{

Integer temp = total;
total = 0;
return temp;


}




### Exercise 2.56

Both.



### Exercise 2.57
```java
 public void printTicket()
    {

Integer amountLeftToPay = price - balance;

if ( amountToPay < 0) {

        // Simulate the printing of a ticket.
        System.out.println("##################");
        System.out.println("# The BlueJ Line");
        System.out.println("# Ticket");
        System.out.println("# " + price + " cents.");
        System.out.println("##################");
        System.out.println();

        // Update the total collected with the balance.
        total = total + balance;
        // Clear the balance.
        balance = balance - price;
}
else {
Integer tempMore = price - balance;

System.out.print("Insert " + tempMore + " into the machine")

}


}
```




### Exercise 2.58

Challenge exercise*




