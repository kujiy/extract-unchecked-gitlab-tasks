
# Extract unchecked tasks in Gitlab

It's hard to recognize unchecked checkboxes in Gitlab issues when an issue has lots of comments and checkboxes.

In that case, let's make an new issue with only unchecked tasks!

# What will this tool give you
Extract only unchecked tasks in Markdown.

![](https://raw.githubusercontent.com/kujiy/extract-unchecked-gitlab-tasks/master/0318-05.png)



# Make a bookmark by yourself with a code below

```
javascript:(function(){var out;$(".task-list-item-checkbox:checkbox:not(:checked)").parent().each(function(){var item="\n - [ ] "+$(this).html().replace(/<.*?>/g,'');out+=item;});document.write('<textarea cols=\'100\' rows=\'100\' selected=\'selected\'>'+out+'</textarea>');$('textarea').select();})();
```


# With line breaks (to fix by yourself)
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
# Welcome for your help
Please make this useful!

