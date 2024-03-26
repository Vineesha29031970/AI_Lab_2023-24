# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE:  23/03/2024                                                                          
### REGISTER NUMBER : 212221040180
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br>

### Program:

```
food(apples).
food(chicken).
food(peanuts).
likes(john, X) :-
food(X).
eats(bill, X) :-
food(X).
eats(sue, X) :-
eats(bill, X).
```


### Output:
<img width="225" alt="image" src="https://github.com/Vineesha29031970/AI_Lab_2023-24/assets/133136880/75f33a13-0d1e-4d94-b5fe-a68d0f98b214">


### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:

```
likes(steve, X) :-
easy_course(X).
hard_course(science).
easy_course(X) :-
in_department(X, have_fun).
in_department(bk301, have_fun).
```

### Output:
<img width="424" alt="image" src="https://github.com/Vineesha29031970/AI_Lab_2023-24/assets/133136880/277f61ce-cc46-405a-a901-2414cad29091">


### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 

### Program:

```
criminal(X):-
american(X),
weapon(Y),
hostile(Z),
sells(X,Y,Z).
weapon(Y):-
missile(Y).
hostile(Z):-
enemy(Z,america).
sells(west,Y,nano):-
missile(Y),
Thus the prolog programs were executed successfully and the answer of query was found.
owns(nano,Y).
missile(m).
owns(nano,m).
enemy(nano,america).
american(west).
```


### Output:

<img width="103" alt="image" src="https://github.com/Vineesha29031970/AI_Lab_2023-24/assets/133136880/ce90dfcd-294c-4b52-808e-ff81e94bcc71">


### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
