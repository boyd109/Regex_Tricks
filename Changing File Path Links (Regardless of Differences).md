# Newer Revision (For images):

F: (<img[^>]*?src=['"]).*?\/([^.\/<>]*\.(png|gif|jpg|jpeg))(['"][^><]*?\/>)
R: \1#\2\4

where "#" is the filepath

# Changes:
<!--
<td><img class='hello' src='http://www.example.com/images/items/myitem.png' alt='My Item'/>
    <img class='hello' src='http://www.example.com/images/items/myitem.png' alt='My Item'/><img class='hello' src='http://www.example.com/images/items/myitem.png' alt='My Item'/>
</td>
-->

# Into: 
<!--
<td><img class='hello' src='#myitem.png' alt='My Item'/>
    <img class='hello' src='#myitem.png' alt='My Item'/><img class='hello' src='#myitem.png' alt='My Item'/>
</td>
-->

# Fixed:
- now works with tags in the img-tag and lines not separated by a break.



# OLD

Only pdf extensions: (Greedy, so it allows for .pdf in name)
F: (?<=href=")(.+)/(.+\.pdf)
R: path\2

For Pictures: (With extensions jpg, png, gif)
F: (?<=src=")(.+)/(.+\.(jpg|png|gif))
R: path\2

Where the "path" is the new filepath.

Problems:
- the img or href tags need to be separated by a new line

Changes:
<!--
<p><a href="oldpath213/15-16%20SY%20Calendar%202.pdf.pdf">2015-16 School Calendar</a></p>
<p><a href="oldpath1/ElemBellSched.pdf">Bell Schedule</a></p>
<p><a href="oldpath2/FAQ_DressCode.pdf">Dress Code</a></p>
<p><a href="facebook.com/10920">Facebook</a></p>
-->

To:
<!--
<p><a href="path/15-16%20SY%20Calendar%202.pdf.pdf">2015-16 School Calendar</a></p>
<p><a href="path/ElemBellSched.pdf">Bell Schedule</a></p>
<p><a href="path/FAQ_DressCode.pdf">Dress Code</a></p>
<p><a href="facebook.com/10920">Facebook</a></p>
-->

Doesn't work:
(?<=src=").+(?=\w+)(\w+.jpg|png|gif)
(?<=src=").+(?=\w+)(?!=[\<|\>])(\w+\.jpg|png|gif)

Adapted From:
Find: (<a[^>]*href=")[^"]*("[^>]*>)
Replace: $1#$2

