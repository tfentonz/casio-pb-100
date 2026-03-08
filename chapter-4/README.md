# Chapter 4 Now Let's Learn BASIC

## 4.11 The ABC's of game

List16

```basic
10 PRINT ”ELECTRONIC DICE”
20 X=INT (RAN#*10) +1
30 IF X>6 THEN 20
40 PRINT ”PRESENT NUMBER:”; X
50 GOTO 20
```

## 4.12 Dice game

List17

```basic
 10 PRINT ”DICE GAME”
 20 GOSUB 200
 30 Y=X
 40 PRINT ”YOUR TURN:”; Y
 50 GOSUB 200
 60 Z=X
 70 PRINT ”MY TURN:”; Z
 80 IF Y>Z THEN 120
 90 IF Y=Z THEN 140
100 PRINT ”I WIN”
110 GOTO 10
120 PRINT ”YOU WIN”
130 GOTO 10
140 PRINT ”TIE”
150 GOTO 10
200 X=INT (10*RAN#) +1
210 IF X>6 THEN 200
220 RETURN
```

## 4.18 Roulette is also useful for mathematics!

List24

```basic
 10 GOTO 200
100 M=0
110 FOR C=1 TO N
120 X=2*RAN#-1                  ' Random number is doubled to obtain a random number between 0 and 2.
130 Y=2*RAN#-1
140 R=SQR(X*X+Y*Y)              ' Distance from the center of the circle.
150 IF R>1 THEN 170             ' Determines if the point is inside or outside the circle.
160 M=M+1
170 NEXT C
180 P=4*M/N
190 RETURN
200 PRINT ”SIMULATION PI”
210 INPUT ”N=”,N
220 GOSUB 100
230 SET F4
240 PRINT ”PI=”;P
250 GOTO 200
```
