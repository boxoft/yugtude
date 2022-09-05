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
19. Events are Dispatched Synchronously
20. Add and Remove Event Listeners while an Event is Dispatching
21. DOM Events and the Event Loop
22. DOM Events and Microtasks
23. Improve Scroll Performance with Passive Event Listeners
24. Default Passive Values on the Body Element
25. Synchronous and Asynchronous Events (Ordered and Unordered Events)
26. Window Reflecting Body Element Event Handlers
27. Debug and Inspect Event Listeners with Chrome Developer Tools
28. Debug Event Listener Performance with Chrome Developer Tools

## Known Issues

1. My document and code are different from the official version.
