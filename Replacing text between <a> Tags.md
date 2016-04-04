```html
Replacing something that is the text of an <a> tag with <p> tag
```
F: <p>(.+?)<a href="(.+?)">(.+?)</a></p>
<br>
R: <p><a href="\2">\1</a></p>

Example:
```html
<h3>Main Navigation Menu</h3>
<p>Home <a href="school.com/">http://school.com/</a></p>
<p>Elementary (K-4) <a href="http://Elementary.html">http://Elementary.html</a></p>
<p>Middle School (5-8) <a href="http://MiddleSchool.html">http://MiddleSchool.html</a></p>
<p>High School (9-12) <a href="http://HighSchool.html">http://HighSchool.html</a></p>
<p>Sports and Clubs <a href="http://SportsClubs.html">http://SportsClubs.html</a></p>
```
Goes to: 
```html
<h3>Main Navigation Menu</h3>
<p><a href="school.com/">Home</a></p>
<p><a href="http://Elementary.html">Elementary (K-4)</a></p>
<p><a href="http://MiddleSchool.html">Middle School (5-8)</a></p>
<p><a href="http://HighSchool.html">High School (9-12)</a></p>
<p><a href="http://SportsClubs.html">Sports and Clubs</a></p>
```

Problems, keep in mind:
- the text must be between the initial <p> and <a> tags before the link
- the link cannot be on it's own line (The <p> tag of text will be closed)

Example: (you don't want this)
```html
<p>2015 School Calendar</p>
<a href="link/15-16%20SY%20Calendar%202.pdf.pdf">link/15-16%20SY%20Calendar%202.pdf.pdf
</a>
```
You want:
```html
<p>2015 School Calendar 
<a href="link/15-16%20SY%20Calendar%202.pdf.pdf">link/15-16%20SY%20Calendar%202.pdf.pdf
</a></p>
```
- don't want text after the </a> tag and before the next <p> tag (just annoying. Delete in rare occurences) 

