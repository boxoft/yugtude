# [Your Ultimate Guide to Understanding DOM Events](https://egghead.io/courses/your-ultimate-guide-to-understanding-dom-events-6c0c0d23)

## Contents

1. Introduction to the DOM Events Course

2. High-Level DOM Events Concepts

- [Event](https://developer.mozilla.org/en-US/docs/Web/API/Event)

  - [Dozens of Types](https://developer.mozilla.org/en-US/docs/Web/Events)

    - Animation
    - Asynchronous data fetching
    - Clipboard
    - Composition
    - CSS transition
    - Database
    - DOM mutation
    - Drag'n'drop, Wheel
    - Focus
    - Form
    - Fullscreen
    - Gamepad
    - Gestures
    - History
    - HTML element content display management
    - Inputs
    - Keyboard
    - Loading/unloading documents
    - Manifests
    - Media
    - Messaging
    - Mouse
    - Network/Connection
    - Payments
    - Performance
    - Pointer
    - Print
    - Promise rejection
    - Sockets
    - SVG
    - Text selection
    - Touch
    - Virtual reality
    - RTC (real time communication)
    - Server-sent events
    - Speech
    - Workers

  - [3 Phases](https://developer.mozilla.org/en-US/docs/Web/API/Event/eventPhase)

- [EventTarget](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget)

- https://domevents.dev/

  - 4 Event Targets

3. Listen to Events using HTML Attribute Event Handlers

- HTML Attribute Event Handler

  - [GlobalEventHandlers](https://developer.mozilla.org/en-US/docs/Web/API/GlobalEventHandlers)
  - Bubble phase only!
  - DOM0 Event Handler
  - [Event Handler Content Attribute](https://html.spec.whatwg.org/multipage/webappapis.html#event-handler-content-attributes)

4. Listen to Events using Object Property Event Handlers

- Object Property Event Handler

  - Bubble phase only!
  - DOM0 Event Handler
  - [Event Handler IDL Attribute](https://html.spec.whatwg.org/multipage/webappapis.html#event-handler-idl-attributes)

5. Understand the Relationship Between HTML Attribute and Object Property Event Handlers

6. Add an Event Listener with addEventListener

- addEventListener

  - [EventTarget.addEventListener()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
  - DOM2 / DOM2+ Event Listener
  - Bubble phase by default
  - Syntax

    ```js
    addEventListener(type, listener)
    addEventListener(type, listener, options)
    addEventListener(type, listener, useCapture)
    ```

7. Remove an Event Listener with removeEventListener

- removeEventListener

  - [EventTarget.removeEventListener()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/removeEventListener)
  - [bind-event-listener](https://github.com/alexreardon/bind-event-listener)

8. Choose an Event Listener Mechanism

9. The Execution Order of Event Listeners

10. The Execution Order of Event Listeners in the Target Phase

11. The Event Object

- Clicking the parent element and the button shall get different results.
- [Event](https://developer.mozilla.org/en-US/docs/Web/API/Event)
  - [Event.timeStamp](https://developer.mozilla.org/en-US/docs/Web/API/Event/timeStamp)
  - Event.returnValue #deprecated
  - [Event.currentTarget](https://developer.mozilla.org/en-US/docs/Web/API/Event/currentTarget)
    - The `currentTarget` property changes as the event flows through the different event listeners. And it's also set to null when the event is finished dispatching.

12. Log Events to the Console

- Developer Tools
  - Console
    > This value was evaluated upon first expanding.

13. Cancel Events

- [Event.preventDefault()](https://developer.mozilla.org/en-US/docs/Web/API/Event/preventDefault)
- [Event.defaultPrevented](https://developer.mozilla.org/en-US/docs/Web/API/Event/defaultPrevented) #readonly
- [mousedown](https://w3c.github.io/uievents/#event-type-mousedown)
  - Default action
    > Varies: Start a drag/drop operation; start a text selection; start a scroll/pan interaction (in combination with the middle mouse button, if supported)

14. Cancel Bespoke Events

- `error`

  - [Window: error event](https://developer.mozilla.org/en-US/docs/Web/API/Window/error_event)
  - [Element: error event](https://developer.mozilla.org/en-US/docs/Web/API/Element/error_event)

- `beforeunload`
  - [Window: beforeunload event](https://developer.mozilla.org/en-US/docs/Web/API/Window/beforeunload_event)

15. Stop Events

- [Event.stopPropagation()](https://developer.mozilla.org/en-US/docs/Web/API/Event/stopPropagation)
- [Event.stopImmediatePropagation()](https://developer.mozilla.org/en-US/docs/Web/API/Event/stopImmediatePropagation)

16. The Event Delegation Pattern

- [Event delegation](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events#event_delegation)

17. Create and Dispatch Synthetic Events

- synthetic
  - / sɪnˈθetɪk /
  - Synthetic products are made from chemicals or artificial substances rather than from natural ones.
  - e.g. Boots made from synthetic materials can usually be washed in a machine.
- [Event()](https://developer.mozilla.org/en-US/docs/Web/API/Event/Event)
  - [Event.timeStamp](https://developer.mozilla.org/en-US/docs/Web/API/Event/timeStamp)
    - The `event.tiemStamp` property is set when the event is created and not when it's dispatched.
- [MouseEvent()](https://developer.mozilla.org/en-US/docs/Web/API/MouseEvent/MouseEvent)
- [EventTarget.dispatchEvent()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/dispatchEvent)
  - When an event is dispatched, its internal `stopPropagation` and `stopImmediatePropagation` flags are cleared, but the internal `canceled` flag is not cleared.
- [CustomEvent()](https://developer.mozilla.org/en-US/docs/Web/API/CustomEvent/CustomEvent)

18. Deprecated Event Creation Mechanisms

- [Document.createEvent()](https://developer.mozilla.org/en-US/docs/Web/API/Document/createEvent) #deprecated

19. Events are Dispatched Synchronously

- [EventTarget.dispatchEvent()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/dispatchEvent)
  - > Unlike "native" events, which are fired by the browser and invoke event handlers asynchronously via the **event loop**, `dispatchEvent()` invokes event handlers _synchronously_. All applicable event handlers are called and return before `dispatchEvent()` returns.

20. Add and Remove Event Listeners while an Event is Dispatching

21. DOM Events and the Event Loop

- [The event loop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)
- [Event loops](https://html.spec.whatwg.org/multipage/webappapis.html#event-loops)
  - > An event loop has one or more task queues. A task queue is a set of tasks.

22. DOM Events and Microtasks

- > When a task for an event is being executed on the Call Stack, all event listeners for the event are executed.
- > When the Call Stack is empty, our microtask queue will be executed. What this means is that microtasks queued within an event listener will be executed immediately after that event listener, and before the next event listener is executed.

- [queueMicrotask()](https://developer.mozilla.org/en-US/docs/Web/API/queueMicrotask)

23. Improve Scroll Performance with Passive Event Listeners

- Problem

  - > If a user is trying to scroll the page, the browser has to wait for our `wheel` event listeners to be processed before the browser can know if native scrolling is allowed to happen. It has to wait to see if the event was canceled. This delay can be significant and can make a web page feel unresponsive.
  - > This delay can be even worse if the browser is already executing some other tasks in the Call Stack, which needs to be finished before the `wheel` event can even start to be processed.
  - > The solution to this problem is passive event listeners.
  - > If all of our event listeners on our event path are passive, the browser does not need to wait for the event path to be processed to know if an event will be canceled. It already knows the event cannot be canceled. The browser can allow the native scroll to start straight away without needing to wait for any JavaScript.

- Passive event listeners

  - [EventTarget.addEventListener()](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)
    - Parameters
      - options
        - passive
          - > A `boolean` value that, if `true`, indicates that the function specified by listener will never call `preventDefault()`.
  - [Use passive listeners to improve scrolling performance](https://web.dev/uses-passive-event-listeners/)

- Scrolling
  - [Element: touchstart event](https://developer.mozilla.org/en-US/docs/Web/API/Element/touchstart_event)
  - [Element: touchmove event](https://developer.mozilla.org/en-US/docs/Web/API/Element/touchmove_event)
  - [Element: wheel event](https://developer.mozilla.org/en-US/docs/Web/API/Element/wheel_event)

24. Default Passive Values on the Body Element

25. Synchronous and Asynchronous Events (Ordered and Unordered Events)

- [Synchronous and asynchronous events](https://www.w3.org/TR/uievents/#sync-async)
  - > EXAMPLE 3
    - > During loading of a document, an inline script element is parsed and executed. The `load` event is queued to be fired asynchronously at the script element. However, because it is an async event, its order with relation to other synchronous events fired during document load (such as the `DOMContentLoaded` event from [HTML5]) is not guaranteed.
- `focus`
  - [Element: focus event - Specifications](https://developer.mozilla.org/en-US/docs/Web/API/Element/focus_event#specifications)
  - [focus](https://w3c.github.io/uievents/#event-type-focus)

26. Window Reflecting Body Element Event Handlers

- [Window-reflecting body element event handler set](https://html.spec.whatwg.org/multipage/webappapis.html#window-reflecting-body-element-event-handler-set)
  - onblur
  - onerror
  - onfocus
  - onload
  - onresize
  - onscroll

27. Debug and Inspect Event Listeners with Chrome Developer Tools

- [Chrome DevTools](https://developer.chrome.com/docs/devtools/)
  - Console
    - [Console API reference](https://developer.chrome.com/docs/devtools/console/api/)
    - [Console Utilities API reference](https://developer.chrome.com/docs/devtools/console/utilities/)
      - $0
      - getEventListeners(object)
      - monitorEvents(object [, events])
      - unmonitorEvents(object [, events])
  - Sources
    - [Debug JavaScript](https://developer.chrome.com/docs/devtools/javascript/)
    - [JavaScript debugging reference](https://developer.chrome.com/docs/devtools/javascript/reference/)

28. Debug Event Listener Performance with Chrome Developer Tools

- [Chrome DevTools](https://developer.chrome.com/docs/devtools/)
  - Performance
    - [Analyze runtime performance](https://developer.chrome.com/docs/devtools/evaluate-performance/)

## Known Issues

1. My document and code are different from the official version.
