---
layout: post
title: If/else blocks, the switch statement and ternary operators  
tags: 
 - Programming
 - javascript
 - 2012
---

Earlier this week I was coding on [Codecademy](http://www.codecademy.com/#!/exercises/0), and I learned about a couple of alternatives to the normal **if/else** conditional statements.  The first is the **switch** statement.

The **switch** statement allows you to collect all of your conditionals into one large grouping.  The syntax is similar to a function.
    
    *var variable = "something";
    var result;

    switch (variable) {
    
      case "option1":
        result = "result1";
        break;
        
      case "option2":
        result = "option2";  
        break;
        
      case "option3":
        result = "option3";
        break;
    
      default:
        result = "Nothing matched my available options";
    }*

You start by setting up your initial variable, and then you create an empty variable termed *result*.  The **switch statement** is coded like a **function** in that you have the name **switch** two parenthesis and then open curly brackets.  Each condition section I like to think of in this manner.  In the case of option1 the result is result1...and so forth.  In many ways it's also like an **array**.

I found the **switch statement** to be an interesting alternative, but I'm not sure how useful it is.  You can do pretty much do the same thing by using an **array** in javascript, with the **array** being even more powerful in usefulness.  In Robey's mind, the **switch statement** is really only a relic from before people used functions as a way to split things up.  Just thinking about what that must have been like is making my head hurt...  

The second alternative presented was the **Ternary Operator**.  The **ternary operator** basically gives you a more simplistic way of coding an if/else condition within your code in one line.  A normal piece of code might look something like this:

    //Typical if/else block
    var variable1 = something;
    var variable2 = somethingelse; 
    
    if (variable1 === variable2) {
      result = "good job";
    }
    else {
      result = "bad job";
    }

    //Here is the ternary operator
    result = (variable1 === variable2) ? "good job" : "bad job";

As you can see, it basically shortens things up significantly.  It does, however, look incredibly different from most code.  It's so very different, that unless you're very comfortable with them they might be very easy to miss when reading through code.  If your code becomes complex and large, it could cause more problems than they're worth.

Sorry for the extra long post today, but don't fret!  Pictures of vacation to come on Monday :)  
