# usefulCodeSnippets

---

### Allow numbers _only_

_DOM_

```html
<input type="text" onkeypress="validate(event)" />
```


_Script_

```javascript
function validate(evt) {
  var theEvent = evt || window.event;
  var key = theEvent.keyCode || theEvent.which;
  key = String.fromCharCode( key );
  var regex = /[0-9]|\./;
  if( !regex.test(key) ) {
    theEvent.returnValue = false;
    if(theEvent.preventDefault) theEvent.preventDefault();
  }
}
```
