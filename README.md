#mcup 2020 score

##How to

```template
let 結束時間 = 0
let 開始時間 = 0
player.onChat("run", function () {
    開始時間 = gameplay.timeQuery(GAME_TIME)
    gameplay.title(mobs.target(ALL_PLAYERS), "開始計算分數", "")
    player.teleport(world(-80, 35, -10))
    player.execute(
    "tag @s add calcScore"
    )
})
player.onTellCommand("end", function () {
    gameplay.title(mobs.target(ALL_PLAYERS), "分數計算完畢", "")
    結束時間 = gameplay.timeQuery(GAME_TIME)
    player.say("執行時間：" + Math.trunc((結束時間 - 開始時間) / 1200) + "分" + Math.trunc((結束時間 - 開始時間) / 20 % 60) + "秒")
})
player.onChat("score", function (num1) {
    if (num1 >= 1 && num1 <= 4) {
        player.execute(
        "scoreboard players set @s ShowData " + num1
        )
    } else {
        player.execute(
        "scoreboard players set @s ShowData 9"
        )
    }
})
```
