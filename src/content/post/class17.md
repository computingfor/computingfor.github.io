+++
date = "23 Mar 2024"
draft = false
title = "Class 17: Programming in JavaScript"
author = "David Evans"
slug = "class17"
+++

### Schedule

[Project 3](/project3) is due on Friday, 29 March.

### Slides

[Class 17: ](https://www.dropbox.com/scl/fi/yoc3j1jo3xeq5kxc031ls/cs1010-class17.pdf?rlkey=6h6galxp9abtzkkiz4szho0et&dl=0)

- Recapping and Extending BNF Grammars
- News Highlights: Poisoning, Tim Berners-Lee, and the Reddit IPO!
- Programming in JavaScript

### Code

The code we ended up with in class today is below [jsboom-class17.html](/jsboom-class17.html):

```JavaScript
<html>
<body>
    <h1>Exploring the DOM</h1>

    <script>
        function updateCount() {
            i = i - 1; // single "=" means assignment (":=") 

            countobj = document.getElementById("count");
            console.log("Updating i: " + i);
            countobj.innerHTML = "<b>" + i + "</b>";

            if (i <= 0) { // double "==" is equality comparison
                countobj.innerHTML = "<b><font size='+5'>BOOM!</b>";
            }

        }
    </script>

    <script>
        var i = 5;
    </script>

    <h2>Count Down: <span id="count"><script>document.write(i)</script></span></h2>
    <button onclick="updateCount()">Next</button>

</body>
</html>
```

We didn't get to actually changing the color of the background. To do this, you can set a DOM attribute directly:
```JavaScript
        document.body.style.backgroundColor = color;
```
The value of `color` could be a string the describes a color for a web browser - for example `"red"` or `"#FF0000` (the hexadecimal color encoding with maximum Red, no Green, and no Blue).
