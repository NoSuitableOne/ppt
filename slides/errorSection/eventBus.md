4. 理解EventBus

![EventBus in Project](images/event-bus-in-project.png) 

```javascript
  // 注册事件
  bus.addListener('eventName', (params) => {
    // callback here    
  })
  // 触发事件
  bus.emit('eventName', { ...payload });
```