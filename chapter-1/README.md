# Chapter 1 What Is the PB-100 Menu Used for?

## 1.3 I want to master BASIC !

Program to obtain the total of number from 1 through N

```basic
P0
  10 INPUT ”N= ”,N
  20 S=0
  30 FOR I=1 TO N
  40 S=S+I
  50 NEXT I
  60 PRINT S
  70 GOTO 10
```

## 1.4 I want to play a game !

HI-LO Game program

```basic
P0
  10 PRINT ”HI-LO”
  20 K=0:INPUT ”KEY IN LENGTH ”,L
  30 R=INT (RAN$*10↑L)
  40 INPUT ”KEY IN NO.”,A:K=K+1:H$=”HI”
  50 IF A=R THEN 80
  60 IF A<R;H$=”LO”
  70 PRINT H$;”:K=”;K:GOTO 40
  80 PRINT ”GOOD:ANS=”;R:PRINT ”K=”;K:GOTO 20
```

## 1.5 I want to use it for accounting or business calculation!

Program for monthly load payment

```basic
P0
  10 INPUT ”PRICE”,A
  20 INPUT ”ANNUAL INTEREST(%)”,I
  30 I=I/1200
  40 INPUT ”NUMBER OF PAYMENTS”,N
  50 INPUT ”DOWN PAYMENT”,R
  60 X=(A-R)*I
  70 Y=1-1/(1+I)↑N
  80 K=INT(X/Y+.99)
  90 PRINT ”MONTHLY PAYMENT=”;K
 100 GOTO 50
```

## 1.6 I want to use it for statistics or prediction calculation!

Program to obtain the moving average

```basic
P0
  10 VAC
  20 INPUT ”NUMBER OF MOVES=”,A
  30 B=B+1
  40 PRINT ”DATA”;B+A*C
  50 INPUT F(B)
  60 IF C=0;IF B<A THEN 30
  70 D=0
  80 FOR E=1 TO A
  90 D=D+F(E)
 100 NEXT E
 110 PRINT ”AVERAGE=”;D/A
 120 IF B=A;B=0:C=C+1
 130 GOTO 30
```

## 1.7 I want to use if for data management or arrangement!

Sales ranking program

```basic
P0
  10 VAC
  20 A=A+1
  30 INPUT ”ITEM”,E$(A)
  40 IF E$(A)=”0” THEN 70
  50 INPUT ”UNIT PRICE=”,Z(A),”AMOUNT”,Z(A+13)
  60 GOTO 20
  70 B=0
  80 FOR C=1 TO A-2
  90 IF Z(C)*Z(C+13)≥Z(C+1)*Z(C+14) THEN 130
 100 D$=E$(C):E$(C)=E$(C+1):E$(C+1)=D$
 110 D=Z(C):Z(C)=Z(C+1):Z(C+1)=D
 120 D=Z(C+13):Z(C+13)=Z(C+14):Z(C+14)=D:B=1
 130 NEXT C
 140 IF B=1 THEN 70
 150 FOR C=1 TO A-1
 160 IF E$(C)=”0”;END
 170 PRINT E$(C),”AMOUNT=”;Z(C+13)
 180 PRINT ”$”;Z(C)*Z(C+13)
 190 NEXT C
```

## 1.8 I want to use it as a notebook!

Program for items and prices

```basic
P0
  10 INPUT ”ITEM”,C$
  20 FOR B=1 TO 23
  30 IF C$=D$(B) THEN 60
  40 NEXT B
  50 PRINT ”NO NAME”:GOTO 10
  60 PRINT ”PRICE=”;Z(B)
  70 INPUT Z(B)
  80 GOTO 10
P1
  10 C=0
  20 FOR B=1 TO 23
  30 C=C+Z(B)
  40 NEXT B
  50 PRINT ”TOTAL=”;C
P9
  10 VAC
  20 FOR B=1 TO 23
  30 INPUT ”ITEM”,D$(B)
  40 INPUT ”PRICE”,Z(B)
  50 NEXT B
```
