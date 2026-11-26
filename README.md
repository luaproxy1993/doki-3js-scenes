# Doki 3js Scenes

当前版本：**1.0.0**（`VERSION`）。

这是一份给编码智能体用的技能：帮助 Doki Labs（作者工作室名，不是 GitHub 组织）做出可挂进 `doki.pack` 的 **Three.js 地点、可探索小世界、实时 demo**。它是参考目录、配方和质检门槛，不是又一套 Three.js 引擎教程。

卡带入口仍是 [doki-game-maker](https://github.com/luaproxy1993/doki-game-maker)。发现页永远是角色卡；包内可以挂日程、小机制、静态页、AR / 实时 demo、嵌入游戏。本技能只把那些 3D 槽位做扎实，不替换卡带管线。

```text
/doki-3js-scenes
/doki-3js-scenes catalog
/doki-3js-scenes techniques
/doki-3js-scenes isometric-toy
```

## 安装

```bash
npx skills add luaproxy1993/doki-3js-scenes -y
# or
./install.sh                  # ~/.grok/skills/doki-3js-scenes
./install.sh --force
./install.sh --all-agents     # also Claude / Cursor / Codex / .agents
./install.sh --dir ~/.cursor/skills/doki-3js-scenes
```

详见 `INSTALL.md`。本仓库没有收纳子技能。

## 它做什么

先读 `SKILL.md` 的质检门槛和配方家族，再按需打开：

- `references/catalog.md`：从公开笔记与站点整理的参考作品（只链出去，不收录别人的图或源码）
- `references/techniques.md`：日夜四季、像素后处理、程序化建模、地理沙盘、草地实例化等手法摘要，并指向已开源的文件路径

通用的相机、材质、灯光、加载器、R3F 和性能问题，交给现成的 `threejs-*` 技能。这里管的是「这算不算一个有气氛的 Doki 3D 地点」，以及怎样诚实学习别人的做法、不要把别人的世界当成自己的产品。

## 相关仓库与技能

| 需求 | 去哪 |
|------|------|
| 卡带 / Game-as-Card / 实时 demo 插座 | [doki-game-maker](https://github.com/luaproxy1993/doki-game-maker) |
| 立绘、地图、地点板 | [world-bible-pack](https://github.com/luaproxy1993/world-bible-pack) |
| 网状 RPG 锁序与场景静帧 | [mesh-rpg-craft](https://github.com/luaproxy1993/mesh-rpg-craft) |
| 世界书 / 核心规则书 | [world-bible](https://github.com/luaproxy1993/world-bible) |
| 可玩一局 | [rpg-campaign-maker](https://github.com/luaproxy1993/rpg-campaign-maker) |
| 出包质检 | [world-ship-qa](https://github.com/luaproxy1993/world-ship-qa) |
| Three.js 引擎基础 | `threejs-fundamentals`、`threejs-materials`、`threejs-lighting`、`threejs-scene-craft`、`threejs-react-three-fiber`、`threejs-postprocessing`、`threejs-performance` 等 |

## License

Skill text and scripts: use and modify. Do not ship API keys, `.env`, official-book extracts, or other people's campaign books, scenes, or art in packs or static handoff zips.

第三方作品仍归原作者。学习开源项目时保留其许可证与署名；不要把别人的世界、模型或截图收录进本仓库或 Doki 包当产品。
