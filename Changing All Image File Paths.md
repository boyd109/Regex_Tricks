# Newer Revision (For images):

F: (src=['"]).*?\/([^.\/<>]*\.(png|gif|jpg|jpeg))
<br>
R: \1#\2\4

where "#" is the filepath

# Changes:
```html
<td><img class='hello' src='http://www.example.com/images/items/myitem.png' alt='My Item'/>
    <img class='hello' src='http://www.example.com/images/items/myitem.png' alt='My Item'/><img class='hello' src='http://www.example.com/images/items/myitem.png' alt='My Item'/>
</td>
```

# Into: 
```html
<td><img class='hello' src='#myitem.png' alt='My Item'/>
    <img class='hello' src='#myitem.png' alt='My Item'/><img class='hello' src='#myitem.png' alt='My Item'/>
</td>
```

# Fixed:
- now works with tags in the img-tag and lines not separated by a break.


Adapted From:
Find: (<a[^>]*href=")[^"]*("[^>]*>)
Replace: $1#$2

