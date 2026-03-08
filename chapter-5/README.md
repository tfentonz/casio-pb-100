# Chapter 5 Program Library

Casette tape recording plan

```basic
P0
  10 VAC
  20 PRINT ”CT-TIME”:SET N
  30 INPUT ”TAPE LENGTH”,A
  40 I=1
  50 PRINT ”NO:”;I
  60 INPUT ”TIME:M.S ”,B
  70 C=C+INT B
  80 D=D+FRAC B/.6
  90 IF A≤C+D THEN 200
 100 E=C+D
 110 I=I+1
 120 GOTO 50
 200 PRINT ”FULL NO.”;I-1
 210 F=INT (A-E)+FRAC (A-E)*.6
 220 SET F2
 230 PRINT F:GOTO 10
```

| **Memory contents** | |
| ---- | ---- |
| A | Tape length (minutes) |
| B | Length of 1 selection (minutes, seconds) |
| C | Accumlation of minutes portion |
| D | Accumlation to convert seconds into minutes |
| E | Accumlated time for each selection (minutes) |
| F | Remaining time (minutes, seconds) |
| I | Selection number counter |

