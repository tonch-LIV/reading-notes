# 401_Read_11 - Event Driven Applications

- [Event Driven Programming](#event-driven-programming)
  - [Answers.1](#answers1)
- [Bookmark and Review](#bookmark-and-review)
- [Things to Learn More About](#things-to-learn-more-about)

## [Event Driven Programming](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)

Event-Driven Programming is an approach to development where certain functions are executed only as response to events (triggers).

An ***event*** can be anything from hovering over an element, clicking a button, a connection event, etc.

- Event Emitter: The object that generates / emits events.
- Event Listener: A function that responds when a particular event occurs.
- Event Handler: Code that is executed in the response.
- Event-Driven Architecture: App structure where components communicate and react through events.

Node.js' ability to manage mult requests w/o waiting for every other operation to finish before starting the next (through supporting asynchronous, non-blocking I/O operations) is a benefit of using event-driven programming when creating apps.

### Answers.1

1. What native Node.js module allows us to get started with Event Driven Programming?
    - `events` module which includes the `EventEmitter` class.
        - The class allows creation of custom events, to register listeners, and to trigger functions when events occur.
2. What is the value of Object Oriented Programming used in tandem with Event Driven Programming?
    - the value is that OOP allows 'organization' of reusable classes and objects, and EDP allows blocks of code to be able to communicate and respond to events.
    - modularization and separation of responsibilities.
3. Consider your knowledge of Event Driven Programming in the Web Browser, now explain to a non-technical friend how Event Driven Programming might be useful on the backend using Node.js.
    - It could be useful in the way that code can respond to successfully logging in, when a DB query is made, or when error handlers come into play for unauthorized requests.
    - When shopping online for say, bread, and you add items to a cart; well in the backend, the event of you adding certain breads to your order can be soft modifying the inventory count of ingredients for future bread orders.  
    Once ready to checkout, payment services request can begin to be made and when confirmed the inventory count is updated to reflect the current purchase.  
    The back of house/bakers receive the order and know what to make.  
    The drivers/logistic persons takes your order into account and plans for which day the delivery will be made in accordance to the date of the order.  
    The driver receives your delivery address on the date of delivery, from way back when you checked out, once the order is ready.  
    The client can receive updates one order status and delivery confirmation.

## Bookmark and Review

- [Node docs: events](https://nodejs.org/api/events.html)
  - Examples of event registering, triggers, and listeners.
  - Methods and behavior in Node.js
    - `.on()`: Registers a listener that runs whenever an event occurs.
    - `.emit()`: Triggers an event and calls its registered listeners.
    - `.once()`: Registers a listener that executes only once.
    - `.off()`: Removes a specific event listener.
    - `.removeAllListeners()`: Removes all listeners or those associated with a particular event.

- One event can have ***multiple listeners*** and in turn trigger various functions.  
- Event-driven does not automatically mean asynchronous. By default, EventEmitter listeners ***execute synchronously*** in the order they were registered.  
- Events can send data (***pass arguments***) to their listeners using `.emit()`.
- Emitting an un***handled error*** can terminate the Node.js process, so the special error event should have a registered listener

## Things to Learn More About

- using EDP in a backend environment.
- follow the data flow.
- creating events, regitering listeners,
- understanding when EDP is useful or needed.
- maintaining structure.
- fullstack (front and back-end) event organiation.
