
# Extract unchecked tasks in Gitlab

It's hard to recognize unchecked checkboxes in Gitlab issues when an issue has lots of comments and checkboxes.
In that case, let's make an new issue with only unchecked tasks!


# Make a bookmark by yourself with a code below

```
javascript:(function(){var out="";$(".task-list-item-checkbox:checkbox:not(:checked)").parent().each(function(){var check=$(this).clone();check.find("*").remove();var item="";$(this).parents("li.task-list-item").each(function(){item+="    ";});item+="- [ ] "+check.html().replace(/^\s+|\s+$/g,'')+"\n";if(item!=""){out+=item;}});document.write('<textarea cols="100" rows="100" selected="selected">'+out+'</textarea>');$('textarea').select();})();
```

# What will this tool give you
Extract only unchecked tasks in Markdown.

![](https://raw.githubusercontent.com/kujiy/extract-unchecked-gitlab-tasks/master/0318-05.png)


![](https://raw.githubusercontent.com/kujiy/extract-unchecked-gitlab-tasks/master/0318-08.png)




# With line breaks (to fix by yourself)
```js
var out = "";
$(".task-list-item-checkbox:checkbox:not(:checked)").parent().each( function() {
    var check = $(this).clone();
    check.find("*").remove();
    var item = "";
    $(this).parents("li.task-list-item").each(function (){
        item += "    ";
    });
    item += "- [ ] " + check.html().replace( /^\s+|\s+$/g, '' ) + "\n";
    if(item != "") {
       out += item;
    }
});
/* console.log(out); */
document.write('<textarea cols="100" rows="100" selected="selected">' + out + '</textarea>');
$('textarea').select();
```


# Feedback is welcome
And please make this more useful!

