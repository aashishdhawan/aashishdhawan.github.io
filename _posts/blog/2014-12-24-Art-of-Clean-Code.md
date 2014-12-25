---
layout: post
title: "Art of writing Beautiful Code"
categories: blog
share: true
comments: true

---

Last week i came across a book [**Clean Code** by Robert C. Martin](). This amazing book illustrates the art of writing beautiful and clean code. This post shares what i learned from this great piece of work.

Almost every experienced programmer understands how important a well written code is but what about starters? Is there any way for them to tell which code is good or which one is badly written. Is there a unit to measure that? Yes !!!

> You can measure code quality by a unit named `WTFs/minute` in code review session.

## 1. Characteristics of Clean code

* Written by someone who cares.
* Code reader says while reading it - Ah !!! Thats what i expected from this function.

> Leave the code cleaner if you are working on someone else's code.

## 2. Use Meaningful Names

* Variable, Function name should reveal its intention - why it exists, what it does, How it is used.
* If your name requires any comment to explain it then probably it is not a good name.

{% highlight java %}

// Example of bad naming practice.
int d;
public List<int[]> getThem() {
 List<int[]> list1 = new ArrayList<int[]>();
 for (int[] x : theList)
   if (x[0] == 4) list1.add(x);
   return list1; 
}

// Example of good naming practice.
int elapsedTimeInDays; int daysSinceCreation;

{% endhighlight %}

* Name should not convey disinformation.
* There should be meaningful distinction between similar looking names.
* It is always better to use pronounceable names.

{% highlight java %}

private Date mmddyyyy; // Avoid this kind of naming convention

{% endhighlight %}

* Better to use names which are easier to search using IDE search feature.
* Try to stick to Nouns while naming variables.
* Don't use pun or be cute. 
* Its better to use Computer Science terms, algorithmic terms, pattern names, math terms etc.

{% highlight java %}

// Notice that each of following function starts with 'get'. 
//You can use 'fetch' or 'retrieve', but try to use single word and make method names consistent.
String getParentName(int studentId){	
}

String getMotherName(int studentId){	
}

String getFatherName(int studentId){	
}
{% endhighlight %}

## 3. Functions.

* Should be small. If its length grows beyond 30 lines, rethink.

> Functions should do one thing. They should do it well. They should do it only.

* switch statement tends to make functions lengthy. It is better to minimize use of switch statements.

{% highlight java %}

// Use functions to minimize length of switch statement
Money calculatePay(Employee e) throws InvalidEmployeeType {
 switch (e.type) {
  case COMMISSIONED:
	return calculateCommissionedPay(e);
  case HOURLY:
	return calculateHourlyPay(e); 
  case SALARIED:
	return calculateSalariedPay(e);
  default:
	throw new InvalidEmployeeType(e.type); 
 }
}
{% endhighlight %}

* Never violate Single Responsibility Principal (SRP).
* Use descriptive names. Do not afraid to use lengthy names as long as it is meaningful.
* Function name should reflect value it is returning
* If number of argument in function are greater than three, rethink. 
* try-catch-finally statement makes function ugly. Do not mix logic and error handling part.
* Keep only one line in catch and finally block.
* Try to use polymorphism  instead of switch or if-else statements where ever you can.

{% highlight java %}

// Keep Error and logic part separate
public void delete(Page page){ 
 try{
  deletePageAndAllReferences(page); 
 }catch (Exception e){
  logError(e);
 }
}

private void deletePageAndAllReferences(Page page) throws Exception{
 deletePage(page);
 registry.deleteReference(page.name); 
 configKeys.deleteKey(page.name.makeKey());
}

private void logError(Exception e){ 
 logger.log(e.getMessage());
}
{% endhighlight %}

> Never ever repeat code. Make function out of it.

* Some programmers follow Edsger Dijkstra’s rules of structured programming.Dijkstra said that every function, and every block within a function, should have one entry and one exit. Following these rules means that there should only be one return statement in a function, no break or continue statements in a loop, and never, ever, any goto statements.

## 4. Comments

> Do not comment bad code. Re-write it.

* Nothing can be quite so helpful as a well-placed comment. Nothing can clutter up a module more than frivolous dogmatic comments. Nothing can be quite so damaging as an old cruft comment that propagates lies and misinformation.
* Consider comment as inability to express yourself in code.
* Inaccurate comments are far worse than no comment at all.

{% highlight java %}

// Examples when comments become useful.

//1. Legal comment 

//
//  AppDelegate.m
//  Opinion
//
//  Created by Aashish Dhawan on 23/12/14.
//  Copyright (c) 2014 Moldedbits. All rights reserved.
//

//2. Comment when they improve code readability

// format matched kk:mm:ss EEE, MMM dd, yyyy 
Pattern timeMatcher = Pattern.compile(
"\\d*:\\d*:\\d* \\w*, \\w* \\d*, \\d*");

//3. Clarification of some logic. 

assertTrue(a.compareTo(a) == 0);     // a == a
assertTrue(a.compareTo(b) != 0);     // a != b
assertTrue(ab.compareTo(ab) == 0);  // ab == ab 

//4. Expressing warning

public static SimpleDateFormat makeStandardHttpDateFormat() {
 //SimpleDateFormat is not thread safe,
 //so we need to create each instance independently.
 SimpleDateFormat df = new SimpleDateFormat("EEE, dd MMM yyyy HH:mm:ss z"); df.setTimeZone(TimeZone.getTimeZone("GMT"));
 return df;
}

{% endhighlight %}

* Things to consider before adding comment.

   1. Is this comment is to justify your hack?
   2. Is this comment redundant?
   3. Does this comment make code more readable?
   4. Is this a misleading comment?

> TODO comment - Never push this in production.

* Never show frustration or use pun in comments. See such an example below.

{% highlight java %}

private void startSending() {
 try {
   doSending(); 
 } catch(SocketException e) {
 // normal. someone stopped the request.
 } catch(Exception e) {
   try {
   response.add(ErrorResponder.makeExceptionString(e));
   response.closeAll(); 
   } catch(Exception e1) {
      //Give me a break!
   } 
 }
}

{% endhighlight %}

* Remove comment noise. Following are some example of unnecessary comments.

{% highlight java %}

/** *
* @param title The title of the CD
* @param author The author of the CD
* @param tracks The number of tracks on the CD
* @param durationInMinutes The duration of the CD in minutes */
public void addCD(String title, String author, int tracks, int durationInMinutes) {
 CD cd = new CD();
 cd.title = title;
 cd.author = author; 
 cd.tracks = tracks; 
 cd.duration = duration; 
 cdList.add(cd);
}

/*** Default constructor. */
protected AnnualDateRule(){
}

// No, really? Or how about this:
/** The day of the month. */
private int dayOfMonth;

//And then there’s this paragon of redundancy:
/**
* Returns the day of the month. *
* @return the day of the month. */
public int getDayOfMonth() { 
 return dayOfMonth;
}

/** The name. */ 
private String name;
/** The version. */ 
private String version;
/** The licenceName. */ 
private String licenceName;
/** The version. */ 
private String info;

// Notice cut and paste error in comment. This is a general problem.

////// This is a banner comment. Minimize its use. ///////////////////////

{% endhighlight %}

> Never leave commented out code because other programmers do not have courage to delete this.

## 5. Code Formatting.

* When working in a team make sure all team members agree to common set of formatting rules.
* Use tool which can automatically detect formatting errors.

### 5.1 Horizontal Formatting 

* Lines should not be too long so that you have to scroll.
* Proper indentation is necessary.
* For if-else statements if body is one liner please include in braces.

### 5.2 Vertical Formatting

* File size or class size should be small. If number of lines goes above 500, rethink about restructuring.
* Follow top down approach while adding functions in class. Most important functions should be at top and so on.
* Functions which are related to each other should be close.
* Local variables should be declared close to their usages. In functions define them on top.
* Instance variables should be at top in class or bottom (no other place).
* If function A calls B then A and B should be close to each other, preferably B should be  below A.
* Functions which perform same basic task, having same schema should be close together.

## 6. Data Access and structure.

* Give a thought about whether to make variables private or public. Same goes for functions.
* Hide data objects behind functions.

## 7. Error Handling.

* Code in catch-finally body should be minimum. Create a function and use that in catch-finally body.
* Error message should be informative. It must define error clearly Network failure, Device failure or Programming error. 
* Do not mix business logic and error code.
* Avoid passing null as parameter in functions.
* Avoid returning null from function.

## 8. Test Driven Development (TDD)

> Writing test cases requires skill too.

* Learn how to write good tests. Which aspects of code to check. You should not write test to check every nook and cranny of code.
* There is always a temptation to write quick and dirty code which is not at par with your production code. Avoid that.
* Code keeps evolving therefore it is natural that some test fails and over time test code becomes liability. So plan accordingly.

> Management of test code is as important as management of production code.

> Without test cases every change in production is possible bug.

* Keep test small. Only one assert statement per test.
* Check on concept per test.
* Code test should follow F.I.R.S.T rule which means
	1. F -> Fast = Test should be fast. If they are slow you are not going to run them frequently.
	2. I -> Independent = They should be independent. If they are not one failed test will create a chain of failed tests.
	3. R -> Repeatable = Tests should be runnable in QA, production and your laptop.
	4. S -> Self-validating = They should return true of false. Pass or fail. You should not have to read log file to determine result.
	5. T -> Timely = Test should be written just before the code which needs to be checked.

## 9. Classes.

* Define variable at top in a class.
* Use Encapsulation effectively. 
* Classes should be small. Functions can be kept small by limiting number of lines while classes can be kept small by limiting responsibility.
* Class name should reflect its responsibility.
* Always follow Single Responsibility principal (SRP).
* Minimize coupling and dependencies between classes.
* Minimize entry points.

## 10. Code refactoring 

* Eliminate duplication.
* Increase code expressiveness.
* Proper Indentation.
* Comments should be up to date.
* Code should pass all tests.
* Break too long method or classes.








































