# Crack-Sheep-Sheep

快速通关小游戏“羊了个羊”，基于 Quantumult X 重写功能。

## 思路

通过 Quantumult X 抓包得知，第一关的 map_id 为 80001，第二关的 map_id 为 90015。

只需要将每一关的 map_id 重写为 80001 即可快速通关小游戏。

## 重写规则

```
(^https?:\/\/cat-match\.easygame2021\.com\/sheep\/v1\/game\/map_info)(\?map_id=)(.*) url 302 https://cat-match.easygame2021.com/sheep/v1/game/map_info?map_id=80001
```

## 使用方法

此处借助了 Quantumult X 实现了效果，理论上任意一款抓包软件都可以实现相同效果。

操作流程如下

![操作流程](/img/sheepsheep.jpg)

1. 点击重写规则 - 左下角的加号。

2. 选择 302，分别填入下方的正则表达式和链接。

```
(^https?:\/\/cat-match\.easygame2021\.com\/sheep\/v1\/game\/map_info)(\?map_id=)(.*)
```

```
https://cat-match.easygame2021.com/sheep/v1/game/map_info?map_id=80001
```

3. 启用全部代理 + 重写规则。

4. 进入游戏，通关。

## 注意事项

1. 仅供技术交流，也可以抚慰一下始终无法过关的心灵。
2. 如果想真一点，建议过 12 分钟左右再通关，否则很容易看出是作弊了。
3. 仓库中提供了一个 [snippet](Crack-Sheep-Sheep.snippet) 文件，可以下载到本地后导入。
