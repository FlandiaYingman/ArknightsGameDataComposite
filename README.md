# ArknightsGameDataComposite

聚合处理的《明日方舟》游戏数据。

基于 [ArknightsGameData](https://github.com/Kengxxiao/ArknightsGameData) 项目聚合处理。

## 聚合处理

过期的游戏数据条目偶尔会被删除，故本项目旨在将被删除的数据条目聚合。

目前经聚合处理的游戏数据：

- `gamedata/excel/story_table.json`
- `gamedata/excel/story_review_table.json`

目前仅支持聚合形式如下的游戏数据：

```typescript
{
  [key: string]: any
}
```

即数据条目直接位于根对象之下的游戏数据。

形式如下的游戏数据将在未来获支持：

```typescript
{
  entries1: {
    [key: string]: any
  },
  entries2: {
    [key: string]: any
  }
}
```
