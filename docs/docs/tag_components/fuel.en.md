# combined_dynamic:fuel
[<返回](../index.md)

`tag组件`  `Alpha0.6.0`

格式： `combined_dynamic:fuel;<time>`

定义该物品为可以供机器使用的燃料，如在青铜蒸汽锅炉中燃烧。

| 参数 | 类型 | 描述 |
| ---   | ---  | :---:  |
| time | number | 可供燃烧的时间，按`tick`计算 |

示例：煤粉燃料定义
```json title='coal_dust.json'
...
"minecraft:tags": {
  "tags": [
    "combined_dynamic:fuel;1600"
  ]
},
...
```