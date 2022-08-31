```javascript[2-5]
handleClick = () => {
  setTimeout(() => {
    this.setState(({ count }) => ({ count: count + 1 }));
    // { count: 1, flag: false } before React 18
    // { count: 0, flag: false } React 18
    console.log(this.state);

    this.setState(({ flag }) => ({ flag: !flag }));
  });
};
```