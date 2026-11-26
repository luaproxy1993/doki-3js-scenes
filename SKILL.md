---
name: doki-3js-scenes
description: >
  Doki Labs 的 Three.js 地点 / vibe-coded 场景 / 实时 demo 资料库：配方家族、质检门槛与参考目录。
  用来给 doki.pack 里的地点、可探索小世界和实时演示做有气氛的 Web 3D，不替代卡带管线。
  Use when the user runs /doki-3js-scenes, says Doki 3D 场景, vibe coding Three.js,
  等轴测小世界, 可探索地图, 实时 demo, 地点沙盘, 或要把一个精致的浏览器 3D 场景挂进 Doki 包。
  通用的 Three.js 引擎问题（相机、材质、灯光、加载器、R3F、后期、性能）交给现成
  threejs-fundamentals、threejs-materials、threejs-lighting、threejs-scene-craft、
  threejs-react-three-fiber、threejs-postprocessing、threejs-performance 等技能。
  本技能是参考库 + 配方 + 品质门槛，不是另一份引擎教程。
argument-hint: "[catalog|techniques|isometric-toy|explorable-map|product-viz|cinematic-drive|geo-sandbox|shader-etude|surreal-corridor]"
user-invocable: true
metadata:
  version: "1.0.0"
  short-description: Doki 3D 地点与 Three.js 实时 demo 的配方、门槛和参考目录
  feeds: "doki-game-maker, mesh-rpg-craft, world-bible-pack"
---

# Doki 3js Scenes

给 Doki Labs 做浏览器里的 3D 地点，不是再讲一遍 Three.js。卡带入口仍是 `/doki-game-maker`。本技能回答三件事：什么时候算够格、可以走哪几类配方、怎样诚实借鉴公开作品。

详细目录见 [references/catalog.md](references/catalog.md)。手法摘要与开源文件路径见 [references/techniques.md](references/techniques.md)。

## 何时使用

用户要的是下面之一，就读本技能：

- 一个能挂进 `doki.pack` 的 **地点**、**可探索小世界** 或 **实时 demo**
- vibe-coded 的 Three.js 庭院、山谷、沙盘、走廊、驾驶或产品可视化，并且要达到「能给人看」的完成度
- 想学习小红书 / 开源上那些精致场景的做法，再做**自己的**世界

不要在这里重讲 Renderer、PBR 贴图或 R3F 的 hook 用法。那些走 `threejs-*`。本技能也不写卡带 D0–D6、不写出包质检；插座和导出仍归 `/doki-game-maker`，质检归 `/world-ship-qa`。地点板、立绘、2D 地图仍归 `/world-bible-pack`。网状战役的静帧 / idle loop 锁序仍归 `/mesh-rpg-craft`。

## 质检门槛

转立方体贴图不算交付。一个 Doki 用的 3D 地点，至少要同时站得住这几条：

1. **有明确气质。** 一句话能说出时间、气候和情绪，例如「夏日午后的回廊」或「雨夜的窄街」，而不是「一个 Three.js 场景」。
2. **光是讲得通的。** 主光有方向和色温；夜景靠灯具锚点，而不是整幅提亮。日夜切换时不要突然跳光，也不要出现方向相反的双影。
3. **时间或天气会改变场面。** 至少做日夜，或四季，或一种会改变材质与道具的天气。自动流转要可暂停；手动切换要有短过渡，UI 不要跟着淡出。
4. **地方是可走或可切换的。** 要么能绕着看、走进分区，要么能在几个命名地点之间切换。不要只有一帧摆拍。
5. **物体有支撑。** 道具放在能承托它的面上；角色或动物的头、颈、肢体要连着；旋转一圈后不能露出纸片或悬浮。
6. **界面是浮在场景上的。** 画布铺满预定区域，文字保持清晰，不要把 UI 送进像素后期。手机竖屏和桌面都要能用。
7. **包是干净的。** 相对路径、无运行时密钥、无漏网的 `server/` 或 `.env`。编译通过不等于已经在真机上看过。

未达到门槛时，先修光、构图和状态表，再加粒子或新物件。

## 配方家族

先锁定气质和家庭，再选技术栈。不要把七种做法叠进同一个地点。

| 家族 | 适合什么 | 起步要点 |
|------|----------|----------|
| `isometric-toy` 等轴测玩具世界 | 庭院、房间、可旋转微缩景观 | 正交相机、竖向构图、程序化模型、统一时间线。像素风是可开关的后期，不是默认。参考手法见 `techniques.md` 里对《溪间四时》的摘要。 |
| `explorable-map` 可探索低模地图 | 个人站点式山谷、分区花园、履历世界 | 命名分区、可走到或点选、季节 / 日夜改变植被和天空。模型能用代码搭就不要先上重型 DCC。 |
| `product-viz` 产品级可视化 | 协议、细胞、仓库、教学工作台 | 交互说明一件真事；视觉可以华丽，但状态必须读得懂。不要只做会转的展示模型。 |
| `cinematic-drive` 电影感驾驶 | 夜雨道路、跟随镜头的短途行驶 | 车、路、雨和灯是一套气氛，不是赛车模拟器。官方演示要按原作者署名。 |
| `geo-sandbox` 地理沙盘 | 真实地块、OSM / 卫星底图、按纬度算太阳 | 先做可读的地形和日照，再堆建筑。性能和地图密钥都要提前想。 |
| `shader-etude` 风格化着色练习 | 草地、风、墨线、像素格 | 可以小，但参数要可调，并说清哪些是代码、哪些是贴图资产。 |
| `surreal-corridor` 超现实走廊 | 倒置空间、线框、悬浮界面、怪奇气质 | 空间规则要自洽；运动和材质为情绪服务，不要无故加玩法。 |

《溪间四时》仓库里还有一份上游技能 `skills/threejs-reference-diorama/`，讲的是「从参考图做程序化微缩场景」。需要按图复刻方法时去读原仓库，不要把那份技能拷进 Doki 包，也不要默认给每个地点加上四季和歌单。

## 署名与借用

- **学做法，不搬世界。** 可以借鉴时间线、分区、后期和模块切法。不要复制别人的地形、角色、音乐、标题、印章或可识别构图，再当成 Doki Labs 的产品。
- **开源可学习，不等于可以转卖。** [xi4u](https://github.com/annac777/xi4u)（《溪间四时》）是 MIT，署名 AC（annac777）。本技能只摘要手法并指向文件路径，不收录其源码、模型、音乐或资源。衍生工作必须保留原许可证与署名。
- **没有公开仓库的站点，只观察模式。** 例如 THE GROWING VALLEY 的在线页。不要把别人的包、贴图或网格扒进本仓库或 `doki.pack`。
- **转载要写清楚。** 小红书标题与正文、官方页面不一致时，以官方署名为准。演示若跑在 Unreal 或其他引擎，不要写成 Three.js。
- **链接要核过。** 404 的仓库不要当成可克隆地址。目录里已标明核查结果；发表前若再变，改 `catalog.md`。

## 怎样挂进 Doki 包

高阶接法如下。字段表和导出命令仍以 `/doki-game-maker` 为准。

1. **先把场景做成可单独打开的前端。** 一个入口 HTML、相对路径、本地打包 Three.js。不要在前端包里放 API 密钥、地图 token、Agora 长效凭证或 `.env`。
2. **选对插座型号。** 纯浏览的地点或沙盘，通常是 `frontend-static`（宿主 iframe 加载 entry）。已经是完整小游戏的，可用 `iframe-game`。还没收干净的野生 demo，先 `custom` 并能点开，再收成标准 runtime。需要宿主订棚的实时音视频，才是 `stream-client`；本技能做的多数 Three.js 地点用不到它。
3. **宿主保持瘦。** 发现页仍是角色卡。宿主只负责加载入口、可选的对话 / 记忆 / 计费，以及导出时剔除 `server/`、`.env`、session 和 token。场景内部的相机、四季和着色器，包自己管。
4. **地点要能对上世界书。** 若已有 `/world-bible-pack` 的地点板，3D 场景应承接同一地名、气质和时段，而不是另起一套无关的风景。
5. **导出前自己看一遍。** 日夜、分区、缩放和手机竖屏要在真画布上确认。编译成功只说明构建过，不能代替视觉验收。然后再走 `/doki-game-maker` 的 `export-static` / `handoff` 和 `/world-ship-qa`。

## 工作顺序

1. 一句话锁定气质、配方家族、是否需要日夜 / 四季 / 可走分区。
2. 读 `references/catalog.md` 里最接近的两条，记下可学的模式和不可抄的部分。
3. 需要手法细节时读 `references/techniques.md`，并打开它指向的上游文件，不要凭记忆复述着色器。
4. 引擎级问题转交对应的 `threejs-*` 技能。
5. 先做出可旋转或可切换的骨架（地面、主物体、光、相机），再填植物、天气和事件。
6. 对照上面的质检门槛。通过后再谈挂包。
