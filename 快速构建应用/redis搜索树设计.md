## 搜索树 redis 设计

工程数据集合

1. 整数集合 工程编号 (其他信息 id, id)
2. icdSystem 系统列表
   单个节点：(id,name,parentId)
3. icddevice 设备列表
4. 429 信息表
5. 664 信息列表
6. nobus 信息列表
7. can 信息列表
8. 域链表

测试方法：后端生成树结构数据（树数据 10 层，每层 20 个节点），提供接口；前端调用接口获取到整棵树数据，渲染到前端界面上
测试目标：从拿到接口返回数据后开始，到前端正确显示整棵树结构需要的时间

数据结构是

```js
{
    uuid:"xxx", // 唯一标识
    name:"xxx", // 名称
    fullpath:"xxx", // 全路径
    nodeType:"xxx", // 节点类型
    children:[{ // 孩子节点
        uuid:"",
        name:"",
        fullpath:"xxx",
        nodeType:"xxx",
        children:[{
            ...
        }]
    },...]
}
```
