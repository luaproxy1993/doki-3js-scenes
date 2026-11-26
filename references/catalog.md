# 参考目录

整理日期：2026-11-26（Asia/Shanghai）。条目只提供官方或已核对的链接，以及可学的模式。本仓库不收录第三方截图、模型、音乐或源码。小红书笔记通常需要登录才能打开。

链接状态以本次抓取为准：能打开的写「已核」；失败的写明状态，不再当成可用地址。

## 开源与可玩站点

### 溪间四时 · Streamside Four Seasons

- 作者署名：创意、视觉与需求设计由 AC（[annac777](https://github.com/annac777)）完成。小红书笔记作者署名为 momo，是否同一人以仓库署名为准。
- 许可证：MIT（Copyright (c) 2026 AC）
- 源码（已核 200）：https://github.com/annac777/xi4u
- 在线（已核 200，标题「溪间四时 · Streamside Garden」）：https://xi4u.pages.dev
- 小红书笔记：https://www.xiaohongshu.com/explore/6a9d19c60000000011037c8c?xsec_token=ABdMCv0eMpi5QITthUtHqAjpcjkqrLHMeakfq7uLBmO7o=&xsec_source=pc_feed
- 技术：React、TypeScript、Three.js（约 0.180）、Vite / vinext；建筑、植物、人物、天气和水面均由代码生成，不加载外部模型、HDR 或网络字体。
- 可学：等轴测微缩庭院；原生 / 像素双画风；统一的时辰、四季与天气时间线；深度法线墨线、色阶与 Bayer 抖动；季节道具显隐表。手法与文件路径见 [techniques.md](techniques.md)。仓库内还有上游技能 `skills/threejs-reference-diorama/`，讲从参考图做程序化微缩场景。
- 不要做：把这座庭院、标题、印章或音乐搬进 Doki 包当产品。MIT 允许学习与衍生，但必须保留许可与署名，且本技能不 vendoring 该项目。

### THE GROWING VALLEY

- 作者：jade（小红书笔记）；站点无公开源码仓库（本次未找到）。
- 在线（已核 200，标题「The Growing Valley — Portfolio」）：https://growing-valley-portfolio.fyshark.workers.dev
- 小红书笔记：https://www.xiaohongshu.com/explore/6a9ca4c7000000000d02708a?xsec_token=ABPWBGgmg4VQ14XPf2LdK6WlXE_PgFdSpQ9OVZZEIzhK0=&xsec_source=pc_feed
- 作者自述：低多边形可探索植物园式个人站点；React + TypeScript + Three.js / R3F；模型多为代码生成而非 Blender；Codex + Claude；用过 Ponytail、3D Runtime Check、ImageGen 等技能；部署在 Cloudflare Workers。作者提到在中国大陆可能需要翻墙。
- 本次从已加载站点观察（只看模式，不扒资源）：页面为 vinext / Next 风格前端；主场景块为 `ValleyExperience` 与 `ValleyCanvas`；使用 `@react-three/fiber`、`InstancedMesh` 和 `OrbitControls`；打包后的脚本里未见 `GLTFLoader` / `useGLTF` / `.glb`，与「模型多为代码生成」相符。分区路标为 Origins、Crossroads、Workshop、Horizon、Photo House。页面文案里对应 The Herbarium、A New Path、The Systems Workshop、The Future Studio、Moonlight Photo House（导航简称 Photo）。Contact 是页面侧栏 / 表单，不是同一组地面路标。季节按钮为 spring / summer / autumn / winter（界面把这项叫 weather），另有日夜切换。
- 可学：把履历或世界章节做成可走的分区；季节与日夜是全局状态；代码搭低模比先导入重型资产更适合 vibe coding。
- 不要做：镜像该站点的地形、分区文案或视觉识别，把它当成自己的作品集或 Doki 地点。

### Threejs-Punk Drive

- 官方可玩（已核 200）：https://www.threejspunk.com
- 页面署名：Anderson Mancini 与 Sunag。`<title>`、`author`、`creator` 与说明均写「Cyberpunk driving game in WebGPU & Three.js by Anderson Mancini and Sunag」。技术为实时 WebGPU、Three.js 与 TSL（Three Shading Language）。Twitter 账号为 `@andersonmancini`；Open Graph 地址为 https://threejspunkdrive.vercel.app/ 。作者站：https://andersonmancini.dev/
- 小红书笔记（小陈的AI频道）：https://www.xiaohongshu.com/explore/6b01a433000000002303e94c?xsec_token=AB8i_-AFxRjIAwexshVp4bl8i7MKKTKQt3MhgbM5yWNvI=&xsec_source=pc_feed
- 诚实说明：笔记标题曾写这是 Astra 做的；正文与官方页面都把作品归给 Anderson Mancini 和 Sunag。本目录把它当作可玩参考，不当作 Astra 原创。
- 可学：雨夜霓虹的驾驶气氛、灯与湿路面、电影感跟随，而不是再造一款竞速网游。

## Dilum Sanjaya 的产品级 Web 3D

小红书「Vibe Coding天花板盘点」（山鬼）转述了 Dilum Sanjaya 的一组作品：Protocol Explorer、Cell Architecture Studio、WareTrack、Backcountry 101。视觉用 Midjourney / Nano Banana，3D 资产提到 Hunyuan3D / World Labs，技术栈为 React + Three.js + TypeScript。以下以作者官方站点为准。

- 作者站（已核 200）：https://dilum.dev/  
  简介写明做 AI 实验、手写开源演示，以及 React 与 Three.js 相关内容。
- Primers（已核，本次成功读到页面）：https://dilum.dev/primers
- AI Lab（已核，本次成功读到页面）：https://dilum.dev/lab
- Protocol Explorer：官方 Primers 链到 https://protocol-explorer-alpha.vercel.app （本次用浏览器 UA 抓取为 200，标题「Protocol Explorer · Learn how the internet works」，author 为 Dilum Sanjaya）。该域名偶尔会碰到 Vercel Security Checkpoint，以官方站上的链接为准。
- Backcountry 101：官方 Primers 链到 https://backcountry-101.vercel.app 。本次一度返回 200 且标题为「Backcountry 101 · Survival skills, step by step, in 3D」，随后同样可能被 Vercel 检查页挡住。
- Cell Architecture Studio：官方 AI Lab 卡片链到 X 帖 https://x.com/DilumSanjaya/status/2053155739389378849 ，未在官网给出独立 Web 应用地址。主机名猜测 `cell-architecture.vercel.app` 曾出现过同名标题，但多次落到 Vercel 检查页，且官网未链接，**不作为已确认可玩地址**。
- Warehouse Digital Twin（笔记里的 WareTrack）：官方 AI Lab 卡片链到 X 帖 https://x.com/DilumSanjaya/status/2106426962738880879 ，官网没有给出独立 Web 应用。`waretrack.vercel.app` 打开是无关的「Modernize Free」登录页；`warehouse-digital-twin.vercel.app` 标题为「Nestle-DC1 Warehouse Visibility」，**不能据此当成 Dilum 的官方演示**。
- 可学：把复杂系统做成可逐步操作的 3D 说明，而不是只能绕着看的模型；资产可以来自生成工具，但交互状态必须自己设计。
- 小红书笔记：https://www.xiaohongshu.com/explore/6afbb905000000002a029d6a?xsec_token=ABW_DjMwI-FByQoqf7SLs0kdIkskSJEnOHcGAdZK4yCmI=&xsec_source=pc_feed

## 仅有笔记、没有已核开源仓库的条目

这些条目只记录模式。不要把笔记里的画面或未证实的仓库当成立项材料。

### 腾讯企鹅岛（飞翔的熊猫）

- 小红书：https://www.xiaohongshu.com/explore/6aeb297d000000000300b707?xsec_token=ABb7p2HefjC3uAwDmR7v_sUZqYyGQT76VcO118HPlAMmk=&xsec_source=pc_feed
- 模式：用 OSM 与卫星底图做大铲湾沙盘；太阳位置按深圳纬度计算；单文件 HTML。作者说仍然较卡，站点未公开。
- 可学：真实地块的日照与底图叠加；单文件便于分发，但 dense 地形要注意性能。地图密钥若需要，不能进前端包。

### 颠倒世界（兼容不可）

- 小红书：https://www.xiaohongshu.com/explore/6ab927bf000000000d020ae7?xsec_token=ABspL9r7iv0oLbLyB42Ki8q4AOFgkfRkclpUANVLBd38g=&xsec_source=pc_feed
- 模式：倒置隧道、红色线框、悬浮代码面板，怪奇（Stranger Things 式）气质。
- 可学：空间规则为情绪服务；线框与界面元素可以当布景，不必做成工具窗口。

### 夜雪林（肥泡）

- 小红书：作者称用 Claude Opus 5.5，大约 5 小时，并用过名为 saltine 的 skill；雾、雪、村庄。
- 曾给出的仓库 https://github.com/zhuojiepao-maker/world-forge 在 2026-11-26 再次请求为 **HTTP 404**，不要写成可克隆地址。
- 可学：雾与雪的层次、有限时间内能完成的夜景村庄气氛。没有可用源码时，只记模式。

### 风格化草地 Grass Paint（糯米鸡NoMiKi）

- 小红书：https://www.xiaohongshu.com/explore/6a6d64e0000000002500c304?xsec_token=AB3scKLfFZlEDULuecppJg0b590Tg1RDes2_h57Xg2tM0=&xsec_source=pc_feed
- 模式：可调密度与风的草地着色；作者说明并非纯代码，含部分美术资产。
- 可学：风场与实例化草地的参数化；交付时写清哪些是 shader、哪些是贴图。

### 3D 版贪吃蛇（咪会困啊）

- 小红书：https://www.xiaohongshu.com/explore/6b080f16000000002203961b?xsec_token=ABHOnwE0ypIpe5HHUFzxPyJunLlB_F4i6XQvMuh-OHW_w=&xsec_source=pc_feed
- 模式：立方小岛上的微缩贪吃蛇；Codex + Three.js。
- 可学：把一个极简玩法放进有边界的立体舞台，舞台本身要有完成度。

### 「That is an anchor」（ai的三行诗转述 Nikita）

- 小红书：https://www.xiaohongshu.com/explore/6b080858000000002b01b54a?xsec_token=ABHOnwE0ypIpe5HHUFzxPyJlXXFxD7k-OtGq9dgwDjWH4=&xsec_source=pc_feed
- 笔记转述 Nikita 的实时 Three.js 演示，主题与 AI 智能爆炸有关。本次未能独立核对到一个稳定的官方演示地址，故不杜撰链接。
- 可学：实时演示也可以围绕一个强观念，而不是只展示技术栈。引用时标明这是转述。

### 用 VibeCoding 搭建可交互 3D 场景（Kelly的科研日常）

- 小红书：https://www.xiaohongshu.com/explore/6aa8c6e60000000025037cdc?xsec_token=ABLbnQvM01sQ-N9tHXHHKqkgqZjy_qQL_uhDfQWSGuuFk=&xsec_source=pc_feed
- 诚实说明：这是流程拆解。笔记里的纽约街景演示跑在 **Unreal**，不是浏览器里的 Three.js。不要把它列入 Three.js 可玩参考。
- 可学：从需求到可交互场景的工序；引擎选择要按实际运行时写清楚。
