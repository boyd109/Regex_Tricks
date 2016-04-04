#Replacing the rightmost cell of a six column table with the contents of the first column.

F:(?s)(?<=<tr>)(.+?<td>)(.+?)(</td>\s+?[\w\<\>&;\/]+\s+?[\w\<\>&;\/]+\s+?[\w\<\>&;\/]+\s+?[\w\<\>&;\/]+\s+?\s+?)(<td>)(.+?)(</td>)
<br>
R:\1\2\3\4\2\5\6

Changes:
```html
<table>
    <tbody>
        <tr>
            <td>&nbsp;School</td>
            <td>Win</td>
            <td>Loss&nbsp;</td>
            <td>Tie&nbsp;</td>
            <td>Points&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;1 Serrano</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;2 Oaks</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;3De Anza</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;4 Veron</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;5/6 Edison</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;5/6 Vinevard Stem</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;7/8 Wiltsey</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;7/8 Vina Danks</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;9 Central</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
    </tbody>
</table>
```
To:
``html
<table>
    <tbody>
        <tr>
            <td>&nbsp;School</td>
            <td>Win</td>
            <td>Loss&nbsp;</td>
            <td>Tie&nbsp;</td>
            <td>Points&nbsp;</td>
            <td>&nbsp;School&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;1 Serrano</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;1 Serrano&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;2 Oaks</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;2 Oaks&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;3De Anza</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;3De Anza&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;4 Veron</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;4 Veron&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;5/6 Edison</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;5/6 Edison&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;5/6 Vinevard Stem</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;5/6 Vinevard Stem&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;7/8 Wiltsey</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;7/8 Wiltsey&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;7/8 Vina Danks</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;7/8 Vina Danks&nbsp;</td>
        </tr>
        <tr>
            <td>&nbsp;9 Central</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
            <td>&nbsp;9 Central&nbsp;</td>
        </tr>
    </tbody>
</table>
```
