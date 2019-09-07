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
// DOMSubtreeModified
selectElement.addEventListener('change', (event) => {
  const result = document.querySelector('.result');
  result.textContent = `You like ${event.target.value}`;
});

```