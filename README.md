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


https://stackoverflow.com/questions/39615/how-to-loop-through-files-matching-wildcard-in-batch-file
```

You can use this line to print the contents of your desktop:

FOR %%I in (C:\windows\desktop\*.*) DO echo %%I 
Once you have the %%I variable it's easy to perform a command on it (just replace the word echo with your program)

In addition, substitution of FOR variable references has been enhanced You can now use the following optional syntax:

%~I         - expands %I removing any surrounding quotes (")
%~fI        - expands %I to a fully qualified path name
%~dI        - expands %I to a drive letter only
%~pI        - expands %I to a path only (directory with \)
%~nI        - expands %I to a file name only
%~xI        - expands %I to a file extension only
%~sI        - expanded path contains short names only
%~aI        - expands %I to file attributes of file
%~tI        - expands %I to date/time of file
%~zI        - expands %I to size of file
%~$PATH:I   - searches the directories listed in the PATH
               environment variable and expands %I to the
               fully qualified name of the first one found.
               If the environment variable name is not
               defined or the file is not found by the
               search, then this modifier expands to the
               empty string


[https://ss64.com/nt/syntax-args.html][1]
In the above examples %I and PATH can be replaced by other valid values. The %~ syntax is terminated by a valid FOR variable name. Picking upper case variable names like %I makes it more readable and avoids confusion with the modifiers, which are not case sensitive.

You can get the full documentation by typing FOR /?

45.6k4848 gold badges155155 silver badges216216 bronze badges
This doesn't seem to work. %%I was unexpected at this time. \
@Brad if you're using this in the command-line (and not in a batch file), then use %I instead of %%I – doubleDown 

```