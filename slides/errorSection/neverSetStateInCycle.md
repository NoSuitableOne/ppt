2. 不要在循环中setState

```javascript [6-8|14-16]
dispatch({
  type: 'xxx',
  payload,
  onComplete: (code, msg, data) => {
    // ... some logic
    for (let i = 0; i < data.length; i++) {
      this.setNodeState(param1, param2, param3);
    }
  });
})

function setNodeState (param1, param2, param3) {
  // ... some logic
  this.setState({
    key: value
  });
}
```