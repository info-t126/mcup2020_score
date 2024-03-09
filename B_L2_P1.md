# 形狀-圓形與球形

## 怎麼使用?

按下執行後，使用聊天指令 r1 r2 r3 就會開始建造不同的球形建築外觀，完成後再自行美化內容。

可以自己嘗試修改 <br/>
1. 使用不同的方塊材質 <br/>
2. 半徑大小

```template
let 建造原點: Position = null
player.onChat("r1", function () {
    建造原點 = player.position()
    shapes.sphere(
    GLASS,
    positions.add(
    建造原點,
    pos(0, -1, 0)
    ),
    10,
    ShapeOperation.Outline
    )
    shapes.circle(
    LIGHT_BLUE_WOOL,
    positions.add(
    建造原點,
    pos(0, -1, 0)
    ),
    10,
    Axis.Y,
    ShapeOperation.Replace
    )
})
player.onChat("r2", function () {
    建造原點 = player.position()
    shapes.sphere(
    SNOW,
    positions.add(
    建造原點,
    pos(0, -1, 0)
    ),
    10,
    ShapeOperation.Outline
    )
    shapes.circle(
    SNOW,
    positions.add(
    建造原點,
    pos(0, -1, 0)
    ),
    10,
    Axis.Y,
    ShapeOperation.Replace
    )
})
player.onChat("r3", function () {
    建造原點 = player.position()
    shapes.sphere(
    WOOL,
    positions.add(
    建造原點,
    pos(0, 3, 0)
    ),
    10,
    ShapeOperation.Outline
    )
    shapes.circle(
    WOOL,
    positions.add(
    建造原點,
    pos(0, 2, 0)
    ),
    10,
    Axis.Y,
    ShapeOperation.Hollow
    )
    shapes.circle(
    WOOL,
    positions.add(
    建造原點,
    pos(0, 1, 0)
    ),
    10,
    Axis.Y,
    ShapeOperation.Hollow
    )
    shapes.circle(
    WOOL,
    positions.add(
    建造原點,
    pos(0, 0, 0)
    ),
    10,
    Axis.Y,
    ShapeOperation.Hollow
    )
    shapes.circle(
    PINK_WOOL,
    positions.add(
    建造原點,
    pos(0, -1, 0)
    ),
    10,
    Axis.Y,
    ShapeOperation.Replace
    )
    shapes.line(
    PLANKS_OAK,
    positions.add(
    建造原點,
    pos(0, 13, 0)
    ),
    positions.add(
    建造原點,
    pos(10, 0, 0)
    )
    )
    shapes.line(
    PLANKS_OAK,
    positions.add(
    建造原點,
    pos(0, 13, 0)
    ),
    positions.add(
    建造原點,
    pos(0, 0, 10)
    )
    )
    shapes.line(
    PLANKS_OAK,
    positions.add(
    建造原點,
    pos(0, 13, 0)
    ),
    positions.add(
    建造原點,
    pos(-10, 0, 0)
    )
    )
    shapes.line(
    PLANKS_OAK,
    positions.add(
    建造原點,
    pos(0, 13, 0)
    ),
    positions.add(
    建造原點,
    pos(0, 0, -10)
    )
    )
})
```
