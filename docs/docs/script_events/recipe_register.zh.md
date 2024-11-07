# combined_dynamic:recipe_register
[<返回](../index.md)

`脚本事件`  `Alpha0.6.0`

注册自定义机器配方，或者使用新的配方取代原来的配方。

## 基本配方格式

| 参数 | 类型 | 描述 |
| ---   | ---  | :---:  |
| identifer | string | 配方标识符，若需要替换配方，请使用与您想要替换的配方相同的标识符 |
| time | number | 配方进行的时间，按`tick`[^3]计算 |
| tags | Array<string\> | 配方tag，该配方可用于使用对应tag的机器 |
| priority | number | 配方优先级，在出现多个标识符相同的配方时，将采用优先级最高的配方 |
| ingredients | Array<ItemIngredient \| TagIngredient \| Array<ItemIngredient \| TagIngredient\>\> | 配方原料 |
| results | Array<ItemResult\> | 配方结果 |

## 示例

下面是一个粉碎机配方示例。

```json
{
    "identifer": "combined_dynamic:raw_copper_dust",
    "tags": ["bronze_macerator"],
    "priority": 0,
    "time": 140,
    "ingredients": [
        {
            "item": "minecraft:raw_copper"
        }
    ],
    "results": [
        {
            "item": "combined_dynamic:raw_copper_dust",
            "amount": 2
        }
    ]
}
```

## 不同机器适配

基本配方格式中所给出的原料与结果格式仅为通用格式，实际上，不同的机器所能够接受的原料与结果种类数量，以及它们支持的接口种类都有所区别，以下给出所有机器的tag与其支持的原料与结果的种类和最大种类数量。

| 机器类型 | 支持tag | 支持原料种类与数量 | 支持结果种类与数量 | 加入版本 |
| --- | --- | --- | --- | --- |
| 青铜粉碎机 | bronze_macerator | ItemIngredient \| TagIngredient \| Array<ItemIngredient \| TagIngredient\> : 1 | ItemResult : 1 | Alpha0.6.0 |
| 青铜辊压机 | bronze_rolling_machine | ItemIngredient \| TagIngredient \| Array<ItemIngredient \| TagIngredient\> : 1 | ItemResult : 1 | Alpha0.6.0 |
| 青铜切割机 | bronze_cutting_machine | ItemIngredient \| TagIngredient \| Array<ItemIngredient \| TagIngredient\> : 1 | ItemResult : 1 | Alpha0.6.0 |
| 青铜搅拌机 | bronze_mixer | ItemIngredient \| TagIngredient \| Array<ItemIngredient \| TagIngredient\> : 2; PropertyIngredient \| Array<PropertyIngredient\> : 2 | ItemResult : 2; PropertyResult : 2 | Alpha0.6.0 |