# My.Usefull.snippets
 
```js

// https://developer.mozilla.org/en-US/docs/Mozilla/Tech/XUL/Events#Mutation_DOM_events

// Mutation DOM eventsSection
// Event   Description
// DOMAttrModified

// This event is sent to an element when one of its attributes is modified. In the event handler, you can retrieve the attribute that was modified using the event's attrName property, and you can retrieve the old and new values of the attribute using the event's prevValue and newValue properties.

// DOMNodeInserted

// This event is sent when a node is added as a child of a element. If you capture this event at the document level, you can be notified of document changes.

// DOMNodeRemoved

// This event is sent when a node is removed from an element. If you capture this event at the document level, you can be notified of document changes

// const selectElement = document.querySelector('.ice-cream');

// DOMAttrModified
// DOMNodeInserted
// DOMNodeRemoved
// DOMSubtreeModified https://www.w3.org/TR/DOM-Level-3-Events/#event-type-DOMSubtreeModified
selectElement.addEventListener('change', (event) => {
  const result = document.querySelector('.result');
  result.textContent = `You like ${event.target.value}`;
});

```


```batch
https://stackoverflow.com/questions/2768608/batch-equivalent-of-bash-backticks


You can get a similar functionality using cmd.exe scripts with the for /f command:

for /f "usebackq tokens=*" %%a in (`echo Test`) do my_command %%a
Yeah, it's kinda non-obvious (to say the least), but it's what's there.

See for /? for the gory details.

Sidenote: I thought that to use "echo" inside the backticks in a "for /f" command would need to be done using "cmd.exe /c echo Test" since echo is an internal command to cmd.exe, but it works in the more natural way. Windows batch scripts always surprise me somehow (but not usually in a good way).

share


```