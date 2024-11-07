# 接口文档
[<返回](../index.md)

这里收录了本Addon提供的接口，您可以在您的Addon中使用这些接口来为您的游戏内容添加与复合动力联动的功能。

## 内置tag

这些tag可以为您的物品添加一些预设的，简单的功能。

| 名称 | 描述 |
| --- | :---: |
| [`combined_dynamic:is_wrench`](./built_in_tags/is_wrench.md) | 将物品定义为扳手 |

## tag组件

这些长得很奇怪的tag是我们为您准备的，可以将您的自定义物品兼容至我们的机器运作逻辑内的方法，我们将其称为“tag组件”。

注意您应当将它们按格式写进自定义物品的`minecraft:tags`组件内，组件名和每个参数之间用`;`隔开。

| 名称 | 描述 |
| --- | :---: |
| [`combined_dynamic:pressable`](./tag_components/pressable.md) | 将物品定义为可锻压物品 |
| [`combined_dynamic:fuel`](./tag_components/fuel.md) | 将物品定义为机器燃料 |

## 脚本事件

您可以使用游戏提供的`/scriptevent`命令向脚本层发送事件，而我们内置了一些事件可以让您更深度地自定义游戏内容。

每个脚本事件传输的值都应当是一个合法的JSON对象。

| 名称 | 描述 |
| --- | :---: |
| [`combined_dynamic:recipe_register`](./script_events/recipe_register.md) | 注册机器配方 |

## 内置接口

| 名称 | 描述 |
| --- | :---: |
| [`ItemIngredient`](./built_in_interfaces/item_ingredient.md) | 物品配方原料 |
| [`TagIngredient`](./built_in_interfaces/tag_ingredient.md) | 标签配方原料 |
| [`ItemResult`](./built_in_interfaces/item_result.md) | 物品配方结果 |

## 枚举值

| 名称 | 描述 |
| --- | :---: |
| [`GasTypes`](./enums/gas_types.md) | 物品配方原料 |
| [`LiquidTypes`](./enums/liquid_types.md) | 标签配方原料 |