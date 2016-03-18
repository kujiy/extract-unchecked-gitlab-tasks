
# Extract

[bookmarklet](     javascript:(function(){var out;$(&quot;.task-list-item-checkbox:checkbox:not(:checked)&quot;).parent().each(function(){var item=&quot;\n - [ ] &quot;+$(this).html().replace(/<.*?>/g,'');out+=item;});document.write('<textarea cols=\'100\' rows=\'100\' selected=\'selected\'>'+out+'</textarea>');$('textarea').select();})();    )


# html

<table border="0">
<tbody><tr>
  <th colspan="4">Output</th>
</tr>
<tr>
  <td colspan="4"><a id="codeOut" href="javascript:(function(){var out;$(&quot;.task-list-item-checkbox:checkbox:not(:checked)&quot;).parent().each(function(){var item=&quot;\n - [ ] &quot;+$(this).html().replace(/<.*?>/g,'');out+=item;});document.write('<textarea cols=\'100\' rows=\'100\' selected=\'selected\'>'+out+'</textarea>');$('textarea').select();})();">Your Bookmarklet</a></td>
</tr>
<tr>
  <td><b>Bytes:</b>   <input name="sizeOut" type="text" size="10" disabled="disabled"></td>
  <td><b>Saved:</b>   <input name="sizeDiff" type="text" size="10" disabled="disabled"></td>
  <td colspan="2"><b>% Saved:</b> <input name="pctOut" type="text" size="10" disabled="disabled"></td>
</tr>
</tbody></table>





# consoleに打つ版
```javascript
var out;
$(".task-list-item-checkbox:checkbox:not(:checked)").parent().each( function() {
    var item = "\n - [ ] " + $(this).html().replace( /<.*?>/g, '' );
    if(item != "") {
       out += item;
    }
});
/* console.log(out); */
document.write('<textarea cols=\'100\' rows=\'100\' selected=\'selected\'>' + out + '</textarea>');
$('textarea').select();
```

