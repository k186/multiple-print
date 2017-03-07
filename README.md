###multiple-print
this plugins depend on jqprint , i made some change for it ,and can print
with mutiple dom selector

##[demo](http://k186studio.com/demos/printMutil)

###how to use it 

add print style with media='print'
```html
  <link href="css/print.css" rel="stylesheet" media="print"/>
```
and your html
```html
<div id="table1">
    <div id="print1" class="breakpage">
        <table>
            <thead>
            <tr>
                <th>head</th>
                <th>head</th>
                <th>head</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td>someText</td>
                <td>someText</td>
                <td>someText</td>

            </tr>

            </tbody>
        </table>
    </div>
</div>
<div id="table2" class="breakpage">
    <div id="print2">
        <table>
            <thead>
            <tr>
                <th>head</th>
                <th>head</th>
                <th>head</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td>someText</td>
                <td>someText</td>
                <td>someText</td>

            </tr>

            </tbody>
        </table>
    </div>
</div>
```

print some dom with
```javascript
$('#print1').jqprint()

//multiple-print
$('#print1,#print2').jqprint()
```

force page break css
```css
.breakpage {
    page-break-after: always;
}

.breakpage:last-child {
    page-break-after:avoid;
}
```