# 《边狱公司》蜘蛛巢 食指 代行者 堂吉诃德（10314）Seed Doubao 主题视觉替换 Mod

> **独立开源视觉皮肤包 · 常态/觉醒双形态战斗帧 + 呼吸待机 Spine + 一破立绘四件套**  
> **作者**: `skadi00147` | **适配客户端**: PC Steam 官方客户端（Unity `6000.3.12f1`）

本仓库开源了 **「蜘蛛巢 食指 代行者 - 绽放E.G.O::代行 堂吉诃德（`10314` · 双形态）」Seed Doubao 主题视觉外观资产**，并随包附带一套极简、开源透明的本地命令行安装与一键无损还原工具。  
*（注：本仓库**仅包含 `10314` 皮肤资产与极简 CLI 安装/还原器**；不包含内部创作端可视化校准工具。）*

---

## 🚀 懒人最推荐：复制一句话，让你的 AI 帮你全自动安装！

如果手头正在用 **Antigravity / Cursor / Claude Code / Windsurf / Codex** 等带终端执行能力的 AI 助手，**根本不用自己折腾命令行**——把下面对应场景的话复制发给 AI，它就会按 `AGENT_INSTALL.md` 自动查路径、建虚拟环境、备份原版并安全装好：

### 情形 A：你把 GitHub 仓库发给 AI
```text
请帮我克隆这个《边狱公司》10314 堂吉诃德（Seed Doubao 主题）皮肤仓库到本地一个我方便保留的文件夹（不要放进临时目录），然后读取里面的 AGENT_INSTALL.md，按指引检查我的游戏路径、配置依赖并把皮肤安全装进游戏里。如果有需要我先开游戏缓存的步骤再叫我，装完告诉我怎么还原就行。
仓库地址：https://github.com/skadi00147/Limbus-10314-Doubao.git
```

### 情形 B：你从网盘下载并解压了压缩包
```text
我已经把这个《边狱公司》10314 堂吉诃德（Seed Doubao 主题）皮肤仓库下载/解压在当前文件夹了，请你读取里面的 AGENT_INSTALL.md，按指引帮我检查游戏目录、配好环境并一键装好皮肤。如果有需要我先开游戏缓存的步骤再叫我，装完告诉我结果以及以后怎么还原（记得提醒我保留这个文件夹）。
```

---

## 📦 皮肤包含内容与保持原味说明

### ✅ 已替换内容
* **双形态战斗小人完整动作帧（`79` 张定制 PNG 帧，覆盖常态 + 觉醒双形态）**：
  * **一阶段常态（`24 / 24` 人物帧全覆盖）**：包含基础状态、一技能与二技能常态全部重绘动作帧；
  * **二阶段觉醒（`55 / 55` 人物帧全覆盖）**：包含觉醒基础状态与一/二/三技能全部重绘动作帧（含 `4` 个严格水平翻转的 `_flipX` 独立补齐帧）；
  * 安装器底层针对 `p10314` 同包双同名 `10314_Donquixote_Index_Disciple_SDAtlas` 自动执行按 `PathID` 精确消歧写入，并采用 `Full-Quad` 矩形扩边技术防边界裁切。
* **局内双形态呼吸待机 Spine（`index_disciple_donquixote`）**：单页直通 Alpha 贴图（`1792×1600`）、`.atlas` 与 Spine `4.0.64` `.json`，完整支持 `skin "1"`（常态待机）与 `skin "2"`（觉醒待机）双皮肤柔性网格呼吸动画，安装器打包时依据 `pma:true` 自动完成预乘 Alpha 转换。
* **一破立绘四件套（`10314_normal` 全家桶）**：包含大立绘（`10314_normal.png`）、详情页窄卡（`10314_normal_info.png`）、编队方头像（`10314_normal_profile.png`）与助战长条（`10314_normal_profile_support_personality.png`，保留原版上下斜切透明遮罩）。

### 🕊️ 刻意留白（保持原版不变）
* **保留原著特效、三破外观与文本细节**：墓碑阵亡帧（`dead.png` / `dead_b.png`）、纯黑速度线备用帧（`skill2_16.png`）、`41` 个纯刀光与花瓣特效层（`_e` / `_e2`）、三破动态立绘（`10314_gacksung*` / `index_disciple_donquixote_idle*`）、技能图标（`1031401`~`1031408`）、技能名称、原版语音及人格故事文本均保持原版不变（可在游戏内切回一破立绘外观展示完整新立绘；双形态战斗小人与局内待机 Spine 全局生效）。

### ⚠️ 重要技术提示：共享词条 Tag 风险（Shared-Tag Hazard）
* 游戏本地化目录 `LimbusCompany_Data/Lang/<active>/UnitKeyword*.json` 中的 **`UnitKeyword_SPIDER_HOUSE`** 词条，是由所有「蜘蛛巢」系列人格（例如 `10415`、`10916`、`10115`、`10314` 等）**全局共享**的单一键值。
* 在纯官方客户端环境下直接改写共享词条，会连带修改同系列其他人格的显示。为避免跨人格污染，本官服发行包默认**刻意留空且不修改任何词条 Tag**；如需自行实验词条机制，请自行阅读 [`installer/lang_patcher.py`](installer/lang_patcher.py) 并自担联动变化风险。

---

## 🎥 实机演示与多渠道下载

* **实机战斗演示视频（B 站）**：[`BV1rvy4zuEsE`](https://www.bilibili.com/video/BV1rvy4zuEsE/)（`https://www.bilibili.com/video/BV1rvy4zuEsE/`）
* **GitHub 仓库 / Release 直下**：[`skadi00147/Limbus-10314-Doubao`](https://github.com/skadi00147/Limbus-10314-Doubao)
* **夸克网盘分流（`Limbus-10314-Doubao-v1.0.0.zip`）**：[`https://pan.quark.cn/s/3fc079c0b26a?pwd=wh8k`](https://pan.quark.cn/s/3fc079c0b26a?pwd=wh8k)（提取码：`wh8k`）
* **百度网盘分流（`Limbus-10314-Doubao-v1.0.0.zip`）**：[`https://pan.baidu.com/s/1eXCSZr_zjR0-aoiWFltclA?pwd=j4df`](https://pan.baidu.com/s/1eXCSZr_zjR0-aoiWFltclA?pwd=j4df)（提取码：`j4df`）

---

## 🛠️ 人类手动安装 & 一键还原（3 步搞定）

### 安装前准备（必看）
1. **关闭《边狱公司》游戏客户端**（运行中文件会被占用锁死）。
2. **至少先在游戏里见过一次 `10314` 人格**：打开 Steam 版《边狱公司》，在图鉴 / 人格 / 编队 / 战斗界面加载过一次该人格，确保官方 Addressables 缓存已下载到本机 `LocalLow`。
3. 电脑已安装 **Python 3.12 或更高版本**（安装时请勾选 **`Add python.exe to PATH`**）。

### 方式一：双击一键安装 / 还原
1. 双击根目录下的 **`install_skin.cmd`** —— 脚本会自动创建本地 `.venv` 虚拟环境、安装依赖（若默认 PyPI 超时会自动切换清华镜像）、备份你的纯净原版文件到 `.state/` 并注入皮肤。
2. 以后想卸载皮肤、或游戏迎来官方大版本更新前，**关闭游戏后双击 `restore_vanilla.cmd`** 即可 100% 无损恢复官方原版。

> ⚠️ **重要提醒**：**千万不要在还没还原的情况下直接删除整个 Mod 文件夹！** 你的纯净官方原版备份均保存在本目录的 `.state/` 文件夹中。

### 方式二：手动终端命令
```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install "UnityPy>=1.25.0" "lz4>=4.4.0" "Pillow>=12.0.0" "etcpak>=0.9.15" "astc-encoder-py>=0.1.12" "texture2ddecoder>=1.0.6"

# 检查本机路径与 10314 缓存就绪状态
.\.venv\Scripts\python.exe -X utf8 -m installer status

# 备份原版并一键注入皮肤
.\.venv\Scripts\python.exe -X utf8 -m installer apply

# 离线构建校验（仅导出到 build/，不触碰游戏真实缓存与 .state/）
.\.venv\Scripts\python.exe -X utf8 -m installer apply --build-only

# 随时无损还原回官方原版
.\.venv\Scripts\python.exe -X utf8 -m installer revert
```

*(如遇游戏安装在非标准路径导致自动探测不到，可将 `config.example.json` 复制并重命名为 `config.local.json`，在 `"game_root"` 中填入你的游戏根目录路径即可。)*

---

## ⚖️ 重要声明与免责条款

1. **非官方二创与原作版权声明**：本项目及所含资产为粉丝基于《Limbus Company（边狱公司）》制作的**非官方免费同人视觉替换模组**，与 **Project Moon** 官方没有任何从属、授权、赞助或合作关系。游戏原作角色设计、世界观、台词文本、游戏程序、商标及其他一切官方知识产权均归 **Project Moon** 所有。
2. **形象出处与第三方无关声明**：本皮肤中的**豆包 / Seed 形象基于 B 站 UP 主 `@ZipZipPipe` 的同人二创 AI 娘化形象**，与 **字节跳动（ByteDance / Doubao / Seed）** 及 **Project Moon** 官方均无任何关联，**严禁任何形式的倒卖与商用**。
3. **纯本地客户端视觉替换声明**：本安装器不使用 BepInEx / DLL 注入 / 内存修改器，仅修改用户本地缓存资产并保留 `.state/` 无损还原能力；游戏版本大更新前建议先执行 `restore_vanilla.cmd`。
4. **开源范围与非商业协议**：本项目整体（含 `installer/`、`*.cmd` 脚本以及 `mods/` 全部美术资产）统一遵循 [PolyForm Noncommercial License 1.0.0](LICENSE) 非商业协议（`Required Notice: Copyright (c) 2026 skadi00147`）。仅限同好免费交流与个人非商业娱乐使用，**严禁任何形式的倒卖、商业使用、付费搬运、放入付费整合包或冒充原作者发布**。
5. **致谢**：感谢开源社区项目 [UnityPy](https://github.com/K0lb3/UnityPy) 提供的 Unity 资源解析能力。
