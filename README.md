<div align="center">

## Fading background to reveal hidden text


</div>

### Description

This code starts with a plain background and when a button is pressed the background fades to another colour revealing text that was the same color as the origional background.

Easily adaptable by unexperienced users, passwords can be added easily.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Dazfish](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dazfish.md)
**Level**          |Beginner
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |HTML, VbScript \(browser/client side\)

**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__4-1.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dazfish-fading-background-to-reveal-hidden-text__4-6310/archive/master.zip)





### Source Code

```
<HTML>
<HEAD>
<SCRIPT language="vbs">
<!--
Dim redstart, redend, redcount, redcounthex
Dim greenstart, greenend, greencount, greencounthex
Dim bluestart, blueend, bluecount, bluecounthex
Dim increments, count
increments=128
redstart=0
greenstart=255
bluestart=0
redend=0
greenend=0
blueend=0
Sub pass()
 change()
' pw=InputBox ("Enter the password")
' If pw="password" then change(): Exit Sub
' MsgBox "Wrong Password"
End Sub
Sub change()
 greencount=greenstart
 redcount=redstart
 bluecount=bluestart
 count=0
 changenext()
End Sub
Sub changenext()
 redcounthex=Hex(redcount)
 greencounthex=Hex(greencount)
 bluecounthex=Hex(bluecount)
 If Len(redcounthex)=1 Then redcounthex="x"&"0"&redcounthex
 If Len(greencounthex)=1 Then greencounthex="x"&"0"&greencounthex&" "
 If Len(bluecounthex)=1 Then bluecounthex="x"&"0"&bluecounthex
 alter.color=right(redcounthex,2)&right(greencounthex,2)&right(bluecounthex,2)
 if redstart>redend then redcount=redcount-((redstart-redend)/increments)
 if redstart<redend then redcount=redcount+((redend-redstart)/increments)
 if greenstart>greenend then greencount=greencount-((greenstart-greenend)/increments)
 if greenstart<greenend then greencount=greencount+((greenend-greenstart)/increments)
 if bluestart>blueend then bluecount=bluecount-((bluestart-blueend)/increments)
 if bluestart<blueend then bluecount=bluecount+((blueend-bluestart)/increments)
 if count=increments*(15/16) then exit sub
 count=count+1
 wait()
End Sub
Sub wait()
 l=setTimeOut("changenext()",50)
End Sub
-->
</SCRIPT>
</HEAD>
<BODY bgcolor="#00ff00" text=lime>
<CENTER><B>
<INPUT type=button value="Click here to view secret information" onClick="pass()">
<FONT id="alter"><P>This is secret information that you cannot see untill you click the button.
<P>Passwords can also be added later if neccessary!
</FONT></B></CENTER>
</BODY>
</HTML>
```

