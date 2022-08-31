3. 获取更新后的值

```javascript[4,6]
this.setState({
  key: newValue
}, () => {
  console.log(`get updated value here：${this.state.key}`)
});
console.log(`cannot get updated value here：${this.state.key}`);
```

```javascript[3]
const [value, setValue] = useState(initialValue);
setValue(newValue);
console.log(`cannot get updated value, use useEffect: ${newValue}`);
```