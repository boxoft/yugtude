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
8. Choose an Event Listener Mechanism
9. The Execution Order of Event Listeners
10. The Execution Order of Event Listeners in the Target Phase
11. The Event Object
12. Log Events to the Console
13. Cancel Events
14. Cancel Bespoke Events
15. Stop Events
16. The Event Delegation Pattern
17. Create and Dispatch Synthetic Events
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
