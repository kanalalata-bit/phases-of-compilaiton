**1. Facts**



Facts are statements that are always true.

Ex:

male(ram)

female(sita)



**2.Rules**



Rules define relationships using facts.

ex: father(X, Y) :-

&#x20;   male(X),

&#x20;   parent(X, Y).



This means:



X is the father of Y if X is male and X is a parent of Y.



**3. Queries**



Queries ask Prolog to find or verify information.



Example:



?- father(ram, shyam).



Prolog checks:



Is male(ram) true? ✔

Is parent(ram, shyam) true? ✔



Both are true, so the answer is:



true.



\--------------------------------------------

1.prolog

&#x20;male(ram).

female(sita).



parent(ram, shyam).

parent(sita, shyam).



father(X, Y) :-

&#x20;   male(X),

&#x20;   parent(X, Y).

&#x20;

query:?- father(ram, shyam).    o/p: ture



&#x09;father(sita, shyam).	o/p false

&#x09;

\--------------------------------------------------

2\. prolog

/\* ---------- FACTS ---------- \*/



male(ram).

male(shyam).



female(sita).

female(gita).



parent(ram, shyam).

parent(sita, shyam).



parent(ram, gita).

parent(sita, gita).



/\* ---------- RULES ---------- \*/



father(X, Y) :-

&#x20;   male(X),

&#x20;   parent(X, Y).





mother(X, Y) :-

&#x20;   female(X),

&#x20;   parent(X, Y).



sibling(X, Y) :-

&#x20;   parent(P, X),

&#x20;   parent(P, Y),

&#x20;   X \\= Y.



query:	father(X, shyam).	o/p ram

&#x09;mother(X, shyam).	o/p sita

&#x09;sibling(shyam, gita).	o/p true

&#x09;sibling(shyam, X).	o/p gita

\-------------------------------------------

3\. % Rule to calculate sum



&#x20; sum(X, Y, Z) :-

&#x20;   Z is X + Y.



Query 1

?- sum(10, 20, Z).



Output

Z = 30.



Query 2

?- sum(15, 25, Result).

Output

Result = 40.



Query 3

?- sum(100, 250, X).

Output

X = 350.



**Explanation:**

sum(X, Y, Z) :-

&#x20;   Z is X + Y.

X → First number

Y → Second number

Z → Sum of X and Y

is → Arithmetic operator used to evaluate expressions in Prolog



\-------------------------------------------------------------



4\. prolog ( odd or even)

Theory:



mod gives the remainder after division.

If a number divided by 2 leaves remainder 0, it is even.

Otherwise, it is odd.



/\* Rule to check Even Number \*/



even(X) :-

&#x20;   0 is X mod 2.



/\* Rule to check Odd Number \*/



odd(X) :-

&#x20;   1 is X mod 2.

Query 1 : ?- even(10).



Output:  true.



Query 2: ?- even(15).



Output: false.



Query 3: ?- odd(15).



Output : true.



Query 4: ?- odd(20).



Output: false.

\---

**Explanation:**

Rule 1:



even(X) :-

&#x20;   0 is X mod 2.



Meaning:



Divide X by 2.

If the remainder is 0, the number is even.



Example:



10 ÷ 2 = 5

Remainder = 0

Therefore, 10 is Even.



Rule 2:



odd(X) :-

&#x20;   1 is X mod 2.



Meaning:



Divide X by 2.

If the remainder is 1, the number is odd.



Example:



15 ÷ 2 = 7

Remainder = 1

Therefore, 15 is Odd.

