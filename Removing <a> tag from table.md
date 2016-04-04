This removes the <a> tag from a table that contains it in each cell (<td>)

F: (?<=<td>).+?">
<br>
R: (None)

Example:

From:
```html
<table border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td>MUSIC - Hurst, Stephanie F</td>
</tr>
</tbody>
</table>
<div>
<div>
<table border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td><a href="link" target="_top"> P3 FYT/</a></td>
</tr>
</tbody>
</table>
</div>
<div>
<table border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td><a href="link" target="_top"> P3 FYT/</a></td>
</tr>
</tbody>
</table>
```

To:
```html
<table border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td>MUSIC - Hurst, Stephanie F</td>
</tr>
</tbody>
</table>
<div>
<div>
<table border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td> P3 FYT/</a></td>
</tr>
</tbody>
</table>
</div>
<div>
<table border="0" cellspacing="0" cellpadding="0">
<tbody>
<tr>
<td> P3 FYT/</a></td>
</tr>
</tbody>
</table>
```html
