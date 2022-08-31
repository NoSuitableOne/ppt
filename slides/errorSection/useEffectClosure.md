5. useEffect的闭包问题
   
```javascript
  useEffect(() => {
    setInterval(() => doSomeThing(param1, param2), 10000);
  }, [dependence])
```

<span>解决方案: useCallback/useMemo、useRef、添加dependence、使用class组件</span>