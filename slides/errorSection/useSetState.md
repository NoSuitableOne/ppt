1. 请使用setState更新状态

```javascript[16|19-20|23-24]
class SomeComponent extends React.Component {
  constructor (props) {
    super(props);
    this.state = {
      value: '',
      bigObject: {
        ...
        someKey: someValue,
        ...
      },
      list: []
    };
  }
  
  // 更新state的错误方式
  this.state.value = newValue; // 这样的更新不能触发react的刷新
  
  // 不要依赖js对象的特性管理状态
  const newObj = this.state.bigObject;
  newObj[someKey] = newValue;
  
  
  const newList = this.state.list;
  newList.push(newElement)
}
```