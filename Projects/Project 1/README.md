# Project 1 : Boolean Logic

## About

Built 15 basic chips from NAND gates using boolean algebra.

## How

Firstly I built the 

- NOT
- AND
- OR

gates using NAND gates because with these gates you can build every other gate.


Then I checked the implementation for the other gates and built a basic boolean expression using NOT AND OR for its truth table. For example I built the MUX like this:

![truth table](/Extras/MUX.png)

From this truth table you write the expressions for the outputs with 1 and or between them (c -> sel, + -> or, mutliplication -> and, ! -> not):

**!ABC + A!B!C + AB!C + ABC**

We could implement this as is but it is better to simplify using boolean algebra with these rules:

![boolean algebra rules](/Extras/boolean-algebra-table.png)

**BC(!A+A) + A!B!C + AB!C**

**BC + A!B!C + AB!C**

**A!C(B!+B) + BC**

**A!C + BC**

Then I wrote this expression using HDL.