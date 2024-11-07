# combined_dynamic:pressable
[<返回](../index.md)

`tag组件`  `Alpha0.6.0`

格式： `combined_dynamic:pressable;<result>;<amount?>`

定义该物品为可以锻压的物品，即可以在锻压台上将物品锻压或者粉碎。
  
| 参数 | 类型 | 描述 |
| ---   | ---  | :---:  |
| result | string | 锻压结果物品的标识符 |
| amount? | number | 结果数量，默认为1 |

示例：将青铜锭锻压为青铜板
```json title='bronze_ingot.json'
...
"minecraft:tags": {
  "tags": [
    "combined_dynamic:pressable;combined_dynamic:bronze_plate"
  ]
},
...
```