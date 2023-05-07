Download Link: https://assignmentchef.com/product/solved-polish-hp-style-calculator-part-1-and-2
<br>
<p class="ui header product-top-header" title="Reverse Polish (HP) Style Calculator - Part 1 and 2 Solution">Reverse Polish (HP) Style Calculator – Part 1

The purpose of this assignment is to use array as stack to begin constructing a business calculator.

Throughout the remainder of the course, you will complete a series of programming functions that will allow you to develop an emulator for a Hewlett-Packard business calculator that uses the Reverse Polish Notation (RPN) discussed in the Topic Materials.

Reverse Polish Notation is also the basis for a computer programming language for embedded applications called Forth, which you read about in the Topic Materials. As part of this project, you will develop a simplified Forth interpreter.

The heart of a RPN calculator is a data structure called a stack. Review the Topic Materials video tutorials and textbook sections 14.3 and 14.5 and study the examples related to stack prior to completing the programming steps below.

·         Implement a stack class named ArrayStack that “has-a” private array of double.

·         Implement the methods:

o   public ArrayClass(int size) – constructor that creates an ArrayClass instance containing an array of the specified size. Remember that in Java, arrays are indexed from 0!

o   public push(double item) – standard stack action; throws an exception if the array bounds are exceeded.

o   public double pop() – standard stack action; throws an exception if the array bounds are exceeded.

o   public boolean isEmpty() – returns true if the stack is empty, and false otherwise.

o   public double peek(int n) – returns the value of the item located at the specified position on the stack; throws an exception if the array bounds are exceeded or if a nonexistent element is requested; peek(0) will return the top element of the stack.

o   public int count() – returns the number of items currently pushed onto the stack.

·         Implement a console application class named TestArrayStack containing a main method that tests each of the above methods of the ArrayStack by creating an instance of ArrayStack and calling each of the methods to test that each functions normally as described and fails with exceptions as described.

·         When a failure occurs, print a descriptive error message to the console and stop.

·         Keep adding tests and correcting bugs until all tests pass and you have “covered” all aspects of the specification. When this happens, print out “SUCCESS” and stop.

Note: The details of the methods specified above may be somewhat different from the discussion in the text and the videos. You will have to think about adapting the ideas in these sources, as is usual in programming. Available examples are only “good approximations” of what you need to do. You need to add the creative energy to make the adaptations.

·         Use the debugging features of Eclipse to step though the program to find and correct bugs.

·         After thoroughly testing the program, submit the ArrayStack.java and TestArrayStack.java files to the instructor.

<strong>Reverse Polish (HP) Style Calculator – Part 2</strong>

The purpose of this assignment is to incorporate an abstract class and inheritance and add it to the interface of the business calculator created in Topic 4.

·         Implement a pure abstract stack class named AbstractStack that has no implementation. It will not have a private array of double, because that is an implementation detail of ArrayStack that would not be found in other implementations such as LinkedStack. Nor will it have the constructor public AbstractClass(int size), or methods public double peek(int n) or public int count(), since these methods are convenience features that are easily implemented for ArrayStack, but not other implementations of stack.

·         Include the method public double peek(), and add the method public void clear(), resulting in the following abstract methods.

o   public abstract void push(double item) –  Standard stack action; Throws an exception if the stack is full.

o   public abstract double pop() – Standard stack action; Throws an exception if the stack is empty.

o   public abstract boolean isEmpty() – Returns true if the stack is empty and false otherwise.

o   public abstract double peek() – returns the value of the item located at the specified position on the stack; throws an exception if the array bounds are exceeded or if a nonexistent element is requested.

o   public abstract void clear() – empties the stack if it is not already empty.

·         Do not specify a constructor. Depend on the default constructor.

·         Modify the existing ArrayStack.java file to include the phrase “extends AbstractStack.”

·         Add an implementation for the methods void clear() and double peek(), which overloads the existing double peek(int n). Provide a default constructor that creates an array that will hold three elements.

o   public ArrayClass(int size) – constructor that creates an ArrayClass instance containing an array of the specified size. Remember that in Java, arrays are indexed from 0!

o   public push(double item) – standard stack action; throws an exception if the array bounds are exceeded.

o   public double pop() – standard stack action; throws an exception if the array bounds are exceeded.

o   public boolean isEmpty() – returns true if the stack is empty and false otherwise.

o   public double peek(int n) – returns the value of the item located at the specified position on the stack; throws an exception if the array bounds are exceeded or if a nonexistent element is requested; peek(0) will return the top element of the stack.

o   public int count() – returns the number of items currently pushed onto the stack.

·         Modify the existing TestArrayStack.java file to include tests for void clear() and double peek(). Note that it is easiest to do “incremental testing” in which you code a little then test a little.

·         Create an interface with additional methods.

·         Create a new file called Forth.java. Make this a public interface file. Add the following methods to the interface.

o   public add() – pops two values from the stack, adds them together, and pushes the result back onto the stack. Throws an exception if there are not at least 2 items on the stack.

o   public sub() – pops two values from the stack, subtracts the second number popped from the first number popped, and pushes the result back onto the stack. Throws an exception if there are not at least 2 items on the stack.

o   public mult() – pops two values from the stack, multiplies them together, and pushes the result back onto the stack. Throws an exception if there are not at least 2 items on the stack.

o   public div() – pops two values from the stack, divides the second number popped by the first number popped, and pushes the result back onto the stack. Throws an exception if there are not at least 2 items on the stack.

o   public dup() – peeks at the top value on the stack and pushes a copy of that value onto the stack. Throws an exception if the stack is empty or full.

o   public twoDup() – peeks at the top two values on the stack and pushes a copy of both values onto the stack (in the same order). Throws an exception if the stack does not have at least 2 items or room for 2 additional items.

·         Create another file called ForthStack.java. Make this file extend ArrayStack and implement Forth. Code concrete implementations of each of the methods in the interface.

·         Test by making a copy of the file TestArrayStack.java and name it TestForth. Change the name of the class inside the file. Add tests for add, sub, mult, div, dup, and twoDup.

·         After thoroughly testing the program, submit the AbstractStack.java, ArrayStack.java, Forth.java, ForthStack.java, and TestForthStack.java files to the instructor.

5/5 - (1 vote)