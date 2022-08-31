Event Bus是什么
```javascript
class EventBus {
  constructor() {
    EventBus.instance = this;
    this.eventListeners = {};
    this.listenerMap = {};
  }

  addListener = (eventName, listener) => {
    const listeners = this.eventListeners[eventName];
    ...
    if (Array.isArray(listeners)) {
      listeners.push(listener);
    } else {
      this.eventListeners[eventName] = [listener];
    }
    ...
  };

  fireEvent = (eventName, data) => {
    const listeners = this.eventListeners[eventName];
    listeners.forEach(listener => {
      new Promise((resolve, reject) => {
        ...
        resolve(listener(data));
        ...
      })
      .then(() => {})
      ...
    }
  };
```