# doki-3js-scenes v1.0.0

Doki Labs 用的 Three.js 场景资料库：配方、质检门槛与参考目录。本包**不含**子技能，也不替代 `threejs-*` 引擎教程。

## 安装

```bash
npx skills add luaproxy1993/doki-3js-scenes -y
# or
./install.sh                  # ~/.grok/skills/doki-3js-scenes
./install.sh --force
./install.sh --all-agents     # also Claude / Cursor / Codex / .agents
./install.sh --dir ~/.cursor/skills/doki-3js-scenes
```

`npx skills add` 与 `./install.sh` 装的都是本仓库这一棵。已存在的目标默认跳过。`--force` 才覆盖。`--all-agents` 会再装到 `~/.claude/skills`、`~/.cursor/skills`、`~/.codex/skills`、`~/.agents/skills`。

装好后，斜杠：`/doki-3js-scenes`。

## 位置

`~/.grok/skills/doki-3js-scenes/SKILL.md`

## 调用

- `/doki-3js-scenes`
- `/doki-3js-scenes catalog`
- `/doki-3js-scenes techniques`
- `/doki-3js-scenes isometric-toy` · `explorable-map` · `product-viz` · `cinematic-drive` · `geo-sandbox` · `shader-etude` · `surreal-corridor`

## 关联 skill

| 需求 | Skill |
|------|--------|
| 卡带封装、实时 demo / 地点挂进 `doki.pack` | `/doki-game-maker` |
| 地点板、地图、立绘 | `/world-bible-pack` |
| 网状战役场景静帧与 idle loop | `/mesh-rpg-craft` |
| 世界书 / 核心规则书 | `/world-bible`（`/core-rule-book`） |
| 出包质检 | `/world-ship-qa` |
| 相机、材质、灯光、R3F、后期、性能 | 现成 `threejs-fundamentals`、`threejs-materials`、`threejs-lighting`、`threejs-scene-craft`、`threejs-react-three-fiber`、`threejs-postprocessing`、`threejs-performance` 等 |

## 卸

```bash
rm -rf ~/.grok/skills/doki-3js-scenes
```
