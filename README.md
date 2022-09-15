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
