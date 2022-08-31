### 需要的代码

```javascript
// modal
export default {
  namespace: 'nameSpace',
  state: {
    treeData: [], // 设备树数据
    selectedNode: {
      nodeId: '',
      nodeName: ''
    }, // 当前选中的节点
    tableData: [], // 表格数据
    pagination: {
      pageSize: 20,
      currentPage: 1,
      total: 0
    }
  },
  effects: {
    *loadTree() {...},
    *selectTreeNode() {...},
    *changeFilterParams() {...},
    *loadTable() {...},
    *changePagination() {...},
  },
  reducer: {
    ...
  }
}
```