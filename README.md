# ArknightsGameDataComposite

聚合处理的《明日方舟》游戏数据。

基于 [ArknightsGameData](https://github.com/Kengxxiao/ArknightsGameData) 项目聚合处理。

## 聚合处理

过期的游戏数据条目偶尔会被删除，故本项目旨在将被删除的数据条目聚合。

目前经聚合处理的游戏数据：

- `*/gamedata/excel/*.json`

目前仅支持聚合形式如下的游戏数据：

若要将新的对象 A（在本项目中为 [ArknightsGameData](https://github.com/Kengxxiao/ArknightsGameData) 中的新数据）聚合到已存在的对象 B（在本项目中为本项目已存在的数据）之上，则聚合规则为：

1. 检查对象 A 的所有键。
2. 若该键在对象 B 中不存在，则添加该键值对至对象 B 上。
3. 若该键在对象 B 中存在，但所对应的值在对象 A **或**对象 B 中不是对象（即是原始类型），则使用对象 A 中该键对应的值替换对象 B 中该键对应的值。
4. 若该键在对象 B 中存在，且所对应的值在对象 A 和对象 B 中均是对象（即非原始类型），则将对象 A 中该键对应的值**利用以上规则**聚合到对象 B 中该键对应的值上。
