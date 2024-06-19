# Propositional-Logic-Knowledge-Base-

Task1:
Wumpus World (Knowledge base and Inference procedure)
Create a ‘wumpus_kb’ knowledge base for the Wumpus world with the sentences mentioned
in ‘section 7.4.3’ of your AI book, that stores the rules of the Wumpus world, i.e., pits, monsters,
breeze, and stench. The following symbols for each [x,y] location:
P(x,y) is true if there is a pit in [x,y]
W (x,y) is true if there is a wumpus in [x,y], dead or alive.
B (x,y) is true if there is a breeze in [x,y]
S (x,y) is true if there is a stench in [x,y]
L (x,y) is true if the agent is in location [x,y]
Secondly, use the Truth Table Enumeration to check if a sentence is entailed by the KB. You
can use the capabilities of logic.py library provided by AIMA repository
https://github.com/aimacode/aima-python/blob/master/logic.py
You may get the aid for implementation from following notebook.
https://notebook.community/SnShine/aima-python/logic

Note: For Simulation purpose you may use the following link.
https://thiagodnf.github.io/wumpus-world-simulator

![image](https://github.com/rohit546/Propositional-Logic-Knowledge-Base-/assets/100420859/f521a46b-bca5-46b6-bda2-2769c837d3f7)

Here are some sentences rules:
1. There is no pit in [1,1]:
R1 : ¬P1,1 .

2. A square is breezy if and only if there is a pit in a neighboring square
R2 : B1,1 ⇔ (P1,2 ∨P2,1) .
R3 : B2,1 ⇔ (P1,1 ∨P2,2 ∨P3,1) .
3. Now we include the breeze percepts for the first two squares visited in the specific
world
R4 : ¬B1,1 .
R5 : B2,1 .
Required conversions:
We can start conversation by checking what wumpus_kb tells us:
Is there is a pit a P1,1: $P_{1, 1}$.
Is the agent senses breeze in B2,1 $B_{2, 1}$
Task 2:
We have a logistics scenario where items need to be delivered from a warehouse to various
locations, and there are dependencies between certain items.
a.
1. The clause is: "If item A is to be delivered, then item B must be picked up first."
Let's represent this clause using propositional variables:
A: Delivery of item A
B: Pickup of item B
Now, we want to encode the constraint "If A is delivered, then B must be picked up first" into
CNF.
The statement "If A is delivered, then B must be picked up first" can be represented in
propositional logic as A → B
This CNF formula essentially says that either A is false or B is false, or both. In other words, if A is
true, B must also be true.
2. Second Clause: If item C is delivered, then item D must be picked up first.
3.Third Clause: If item B is picked up, then item C must be delivered before item A.

b. if item A is to be delivered, it necessitates that item B must be picked up first; similarly, the
delivery of item C mandates that item D is picked up beforehand, and additionally, if item B is
picked up, it requires that item C is delivered before item A. (Create logical form using
implication, conjunction, disjunction, negation operators)
Apply Resolution process on these examples.


Use the logic library from AIMA repository to perform the above proof by resolution.
Here is a simple example
