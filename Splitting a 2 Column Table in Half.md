```html
Getting half the right half of a two column table when it has a break in the second cell of each row:
F: (?s)(?<=</td>)+.<td.+?</td>
R: (nothing. The right side will be deleted)
```

From:
```html
<table>
<tbody>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
<td width="319">
<p>2</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
```
To:
```html
<table>
<tbody>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
<tr>
<td width="319">
<p>1</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
```
