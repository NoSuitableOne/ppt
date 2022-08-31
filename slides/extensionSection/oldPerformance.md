### Before React 18:
- event handlers中的state更新都会batch处理
- 在fetch callback、Promise.then、timeout中不会batch