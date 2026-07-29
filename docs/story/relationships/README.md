# 人物关系与关系图

状态：**初始草图**

本目录用于保存人物、组织、地点、系统和重要现象之间的结构化关系。

机器可读数据见：[relationships.json](relationships.json)。

## 关系数据原则

每条关系应尽量记录：

- 起点 ID；
- 终点 ID；
- 关系描述；
- 确定程度；
- 生效阶段；
- 是否对玩家公开；
- 可能被哪些世界旗标改变。

当前 `certainty` 主要使用：

- `confirmed`：已确认。
- `confirmed_in_character_background`：人物原始背景已确认，但尚未完全整合进全局世界观。
- `confirmed_mainline_direction`：主线方向已确认，具体演出待设计。
- `confirmed_design_goal`：设计目标已确认。
- `draft`：讨论草案。
- `draft_from_background`：从背景推导出的支线草案。

## 当前 Mermaid 草图

该图只是规范和占位，不代表最终人物关系图。

```mermaid
flowchart LR
    Players[玩家社区]
    Light[逐光会]
    Jiang[江晚]
    Yuchi[尉迟南]
    Baizhi[白芷]
    Husband[赵越强]
    Son[赵晓]
    Daughter[赵倩]
    Epsilon[伊普西隆]
    Pollution[污染]
    Rebirth[重生系统]
    Observatory[通兰天文台]
    Signal[未知信号 / 回应]

    Jiang ---|配偶| Husband
    Jiang ---|母子| Son
    Jiang ---|母女| Daughter

    Epsilon -->|感染并导致死亡| Husband
    Epsilon -->|感染并导致死亡| Son
    Epsilon -->|感染并导致死亡| Daughter
    Jiang -->|研究| Epsilon

    Pollution -->|导致异常| Rebirth

    Light -->|带走或使其失踪| Baizhi
    Jiang -.医学与伦理对照·草案.-> Baizhi
    Jiang -.合作或体系内部·草案.-> Light

    Yuchi -->|任职与返回修复| Observatory
    Yuchi -.广播与等待回应·草案.-> Signal

    Players -.证据与医疗决策.-> Jiang
    Players -.支持、限制或阻止广播.-> Yuchi
    Players -.行动与讨论影响.-> Light
```

## 后续正式关系图建议

正式关系图可以同时输出两种视图：

1. **作者视图**
   包含隐藏关系、人物秘密、真实立场和未来变化。

2. **玩家阶段视图**
   只显示玩家在特定阶段理论上可能知道的关系，避免剧透。

关系图还可以按阶段生成：

- 余梦期；
- 管制期；
- 疑光期；
- 破晓期；
- 结局后历史图。
