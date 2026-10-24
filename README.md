<div align="center">

# XXD Panel 343｜悬浮像素画片

**把照片主体收成一块居中悬浮、右下带柔影的淡彩像素小画。**

<strong>简体中文</strong> · <a href="README.en.md">English</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.ar.md">العربية</a>

</div>

<table>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-01.png" alt="XXD Panel 343 · 01 · 海岸灯塔"><br><sub>01 · 海岸灯塔</sub></td>
    <td width="50%"><img src="./assets/examples/sample-02.png" alt="XXD Panel 343 · 02 · 黄色电车"><br><sub>02 · 黄色电车</sub></td>
  </tr>
</table>

<p align="center"><sub>上半是原照片，下半是这个风格画出来的样子。</sub></p>

## 这是什么

一个给 AI Agent（Claude Code、Codex 等）用的 Skill。你给它一张照片，它按 Panel 343 的原始提示词画出一张 PNG 成品。

- **画成什么样：** 主体被重画成一块边界完整的小画片，悬在大片浅色留白正中，右下方有一道与画片错开、由近及远淡出的柔影。画里用统一大小的像素格，曲线拆成横竖台阶，细节合并成成组的矩形，不描黑边，远近靠色带宽窄和遮挡来分。颜色从照片取四到六种，调成高明度淡彩，加少量沉稳的深色和一处略鲜明的亮点，色块干净平整，没有颗粒和做旧。画片外侧可以有一行轻细的无衬线小字，写照片里具体的东西或地点，也可以不写；照片那一半不放字。
- **关键词：** 淡彩像素小画 · 阶梯轮廓 · 居中悬置 · 右下柔影 · 宽阔留白 · 轻细无衬线
- **能出哪些图：** 上下对照（上原图、下设计）、左右对照、只要设计图，或一套手机／平板／电脑／手表壁纸。可以多选，比例和像素随你定。
- **不是什么：** 不是滤镜，也不是套模板：每张都从你的照片重新画，一张照片一个独立任务。

## 三步用起来

**1. 安装。** Claude Code、Codex 等支持 Skills 的 Agent 都能用：

```bash
npx skills add https://github.com/nevertoday/xxd-panel-343 --skill xxd-panel-343
```

装完重开一次 Agent 会话。也可以 `git clone` 本仓库，再把目录链接到 `~/.claude/skills/xxd-panel-343` 或 `~/.codex/skills/xxd-panel-343`。

**2. 确认 Agent 能生图。** 这个 Skill 不自带生图模型，用的是你 Agent 的生图能力，首选 GPT Image 2。

- Codex 开着内置生图时直接能用。
- Claude Code 等没有内置生图的 Agent，需要接一个 OpenAI 兼容的生图接口，五分钟配好，见[没有内置生图怎么配](#没有内置生图怎么配)。

不确定也可以直接用。不能生图时 Skill 会先停下来告诉你，不会白跑。

**3. 发照片，说一句话：**

> 用 xxd-panel-343 把这张照片做成 3:4 上下对照海报，配中文标题。

说清楚了就直接出图；没说到的（版式、比例、文字）它会问你，通常一两个问题。成品是 PNG，放在 `~/Desktop/xxd/xxd-panel-343/` 下本次任务的新文件夹里。

## 什么照片效果好

**效果好**

- 主体轮廓清楚、一眼能认的照片：一栋房子、一艘小船、一辆车、一只猫
- 地标和街角小景：灯塔、电话亭、一家小店门面、桥
- 构图一般、背景杂乱或主体很小的照片，画片会删掉环境、只留主体

**不太合适**

- 需要看清人脸表情或精细纹理的照片，像素台阶会把它们归并掉
- 想保留整个场景、让画面铺满的需求，这种画法必须是小画片加大留白
- 想要卡通风、光滑曲线、塑料质感或旧纸纹理的需求

## 样张

下面每张都是这个 Skill 用一张照片生成的成品。上下对照和左右对照用的是不同的照片。

### 上下对照：上原照片，下设计

<table>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-01.png" alt="XXD Panel 343 · 01 · 海岸灯塔"><br><sub>01 · 海岸灯塔</sub></td>
    <td width="50%"><img src="./assets/examples/sample-02.png" alt="XXD Panel 343 · 02 · 黄色电车"><br><sub>02 · 黄色电车</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-03.png" alt="XXD Panel 343 · 03 · 帆船"><br><sub>03 · 帆船</sub></td>
    <td width="50%"><img src="./assets/examples/sample-04.png" alt="XXD Panel 343 · 04 · 荷兰风车"><br><sub>04 · 荷兰风车</sub></td>
  </tr>
</table>

<details>
<summary>再看 16 张</summary>

<table>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-05.png" alt="XXD Panel 343 · 05 · 富士山"><br><sub>05 · 富士山</sub></td>
    <td width="50%"><img src="./assets/examples/sample-06.png" alt="XXD Panel 343 · 06 · 雪中木屋"><br><sub>06 · 雪中木屋</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-07.png" alt="XXD Panel 343 · 07 · 公路骑行"><br><sub>07 · 公路骑行</sub></td>
    <td width="50%"><img src="./assets/examples/sample-08.png" alt="XXD Panel 343 · 08 · 露营车"><br><sub>08 · 露营车</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-09.png" alt="XXD Panel 343 · 09 · 摩天轮"><br><sub>09 · 摩天轮</sub></td>
    <td width="50%"><img src="./assets/examples/sample-10.png" alt="XXD Panel 343 · 10 · 红狐"><br><sub>10 · 红狐</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-11.png" alt="XXD Panel 343 · 11 · 五重塔"><br><sub>11 · 五重塔</sub></td>
    <td width="50%"><img src="./assets/examples/sample-12.png" alt="XXD Panel 343 · 12 · 长颈鹿"><br><sub>12 · 长颈鹿</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-13.png" alt="XXD Panel 343 · 13 · 港口渔船"><br><sub>13 · 港口渔船</sub></td>
    <td width="50%"><img src="./assets/examples/sample-14.png" alt="XXD Panel 343 · 14 · 红色谷仓"><br><sub>14 · 红色谷仓</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-15.png" alt="XXD Panel 343 · 15 · 山坡孤树"><br><sub>15 · 山坡孤树</sub></td>
    <td width="50%"><img src="./assets/examples/sample-16.png" alt="XXD Panel 343 · 16 · 高架火车"><br><sub>16 · 高架火车</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-17.png" alt="XXD Panel 343 · 17 · 街角咖啡馆"><br><sub>17 · 街角咖啡馆</sub></td>
    <td width="50%"><img src="./assets/examples/sample-18.png" alt="XXD Panel 343 · 18 · 红色电话亭"><br><sub>18 · 红色电话亭</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-19.png" alt="XXD Panel 343 · 19 · 火烈鸟"><br><sub>19 · 火烈鸟</sub></td>
    <td width="50%"><img src="./assets/examples/sample-20.png" alt="XXD Panel 343 · 20 · 复古小摩托"><br><sub>20 · 复古小摩托</sub></td>
  </tr>
</table>

</details>

### 左右对照：左原照片，右设计

<table>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-21.png" alt="XXD Panel 343 · 21 · 埃菲尔铁塔"><br><sub>21 · 埃菲尔铁塔</sub></td>
    <td width="50%"><img src="./assets/examples/sample-22.png" alt="XXD Panel 343 · 22 · 仙人掌"><br><sub>22 · 仙人掌</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-23.png" alt="XXD Panel 343 · 23 · 金鱼"><br><sub>23 · 金鱼</sub></td>
    <td width="50%"><img src="./assets/examples/sample-24.png" alt="XXD Panel 343 · 24 · 企鹅"><br><sub>24 · 企鹅</sub></td>
  </tr>
</table>

<details>
<summary>再看 16 张</summary>

<table>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-25.png" alt="XXD Panel 343 · 25 · 西瓜"><br><sub>25 · 西瓜</sub></td>
    <td width="50%"><img src="./assets/examples/sample-26.png" alt="XXD Panel 343 · 26 · 盆栽绿植"><br><sub>26 · 盆栽绿植</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-27.png" alt="XXD Panel 343 · 27 · 猫头鹰"><br><sub>27 · 猫头鹰</sub></td>
    <td width="50%"><img src="./assets/examples/sample-28.png" alt="XXD Panel 343 · 28 · 汉堡"><br><sub>28 · 汉堡</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-29.png" alt="XXD Panel 343 · 29 · 红色邮筒"><br><sub>29 · 红色邮筒</sub></td>
    <td width="50%"><img src="./assets/examples/sample-30.png" alt="XXD Panel 343 · 30 · 柴犬"><br><sub>30 · 柴犬</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-31.png" alt="XXD Panel 343 · 31 · 棕榈树"><br><sub>31 · 棕榈树</sub></td>
    <td width="50%"><img src="./assets/examples/sample-32.png" alt="XXD Panel 343 · 32 · 鸟居"><br><sub>32 · 鸟居</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-33.png" alt="XXD Panel 343 · 33 · 蜗牛"><br><sub>33 · 蜗牛</sub></td>
    <td width="50%"><img src="./assets/examples/sample-34.png" alt="XXD Panel 343 · 34 · 冲浪板"><br><sub>34 · 冲浪板</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-35.png" alt="XXD Panel 343 · 35 · 帆布鞋"><br><sub>35 · 帆布鞋</sub></td>
    <td width="50%"><img src="./assets/examples/sample-36.png" alt="XXD Panel 343 · 36 · 老式相机"><br><sub>36 · 老式相机</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-37.png" alt="XXD Panel 343 · 37 · 圣诞树"><br><sub>37 · 圣诞树</sub></td>
    <td width="50%"><img src="./assets/examples/sample-38.png" alt="XXD Panel 343 · 38 · 兔子"><br><sub>38 · 兔子</sub></td>
  </tr>
  <tr>
    <td width="50%"><img src="./assets/examples/sample-39.png" alt="XXD Panel 343 · 39 · 茶壶"><br><sub>39 · 茶壶</sub></td>
    <td width="50%"><img src="./assets/examples/sample-40.png" alt="XXD Panel 343 · 40 · 小黄鸭"><br><sub>40 · 小黄鸭</sub></td>
  </tr>
</table>

</details>

## 常用说法

不用记参数，直接说就行：

| 你想要 | 直接这样说 |
|---|---|
| 上下对照 | 做成 3:4 上下对照 |
| 左右对照 | 做成 16:9 左右对照，左边放原图 |
| 只要设计图 | 只要设计，不要原图，9:16 竖版 |
| 一套壁纸 | 做一套手机、平板、电脑、手表壁纸，风格连起来 |
| 一次多种比例 | 同一张做 1:1、3:4、16:9 各一张 |
| 用自己的文字 | 标题就写「让风经过这里」，一个字都别改 |
| 不要文字 | 不要任何文字 |
| 指定文字语言 | 文字用日语 |
| 整个文件夹 | 把这个文件夹里的照片都做成上下对照 |
| 沿用上次 | 沿用上次的设置 |

习惯命令行也行，参数和上面一一对应：

```text
/xxd-panel-343 photo.jpg --mode top-bottom --size 3:4 --text prompt --locale zh-CN
/xxd-panel-343 photo.jpg --mode design-only --size 9:16 --text none
/xxd-panel-343 ./photos --mode left-right --size 16:9 --text prompt --locale en-US
```

全部参数见[参数参考](#参数参考)。

## 常见问题

**一定要放原照片吗？** 不用。说「只要设计图」或者做壁纸，整张都是设计。

**文字是谁写的？** 默认由生图模型看着你的照片现写，你只定语言。要用自己的字就直说，会一字不改；也可以完全不要字。看起来像事实的信息（地名、日期、数字）只用你给的或照片里看得见的，不会编。

**不满意怎么办？** 说「再来一张」。它会从原照片重新画，而不是在上一张上修改，所以每次结果都不一样。

**批量会不会串？** 不会。每张照片单独生成，不借用别的照片的颜色、文字或构图。整批只问一次设置。

**我的照片会发到哪里？** 只发给你自己的 Agent 所用的生图模型。Skill 不往别处上传，也不在输出里显示接口地址和密钥。

**和其他 Panel 是什么关系？** XXD Panel 是一组风格，一个编号一种，互不影响，可以只装你喜欢的。想让 AI 按照片推荐风格，或者一次比较几个风格，用总目录 [xxd-panel-all](https://github.com/nevertoday/xxd-panel-all)。

## 原始提示词

这个风格完全由小小东写的[原始提示词](references/original-prompt/zh-CN.md)决定。Skill 只在后面追加你选的版式、尺寸和文字设置，不总结、不翻译、不改写它。

阅读译文（只供阅读，不参与出图）：[English](references/original-prompt/en.md) · [日本語](references/original-prompt/ja.md) · [한국어](references/original-prompt/ko.md) · [العربية](references/original-prompt/ar.md)

## 没有内置生图怎么配

需要一个支持 `gpt-image-2`（或兼容模型）的 OpenAI 兼容接口和它的 API Key。下面单独建一份配置，不影响你 Codex 本身的设置：

```bash
mkdir -p ~/.xxd-imagegen
cat > ~/.xxd-imagegen/config.toml <<'EOF'
model_provider = "image"

[model_providers.image]
base_url = "https://api.openai.com/v1"   # 或你的兼容接口
env_key = "XXD_IMAGE_API_KEY"
EOF

# 写进 ~/.zshrc 或 ~/.bashrc，让 Agent 也能读到
echo 'export XXD_IMAGEGEN_CODEX_DIR=~/.xxd-imagegen' >> ~/.zshrc
echo 'export XXD_IMAGE_API_KEY=你的密钥' >> ~/.zshrc
```

重开终端和 Agent 后，在本 Skill 目录里检查一次：

```bash
python3 scripts/configured_imagegen.py probe
```

输出 `"ok":true` 就是通了；它只显示是否可用，不会打印地址和密钥。如果你的 Codex 已经通过兼容接口出图，不需要这一步。

## 参数参考

| 参数 | 取值 |
|---|---|
| `--mode` | `top-bottom` 上下对照 · `left-right` 左右对照 · `design-only` 只要设计 · `wallpaper-pack` 四端壁纸；可多选 |
| `--size` | `auto` 智能推荐 · `source` 跟随原图 · `1:1` `3:4` `4:3` `4:5` `5:4` `2:3` `3:2` `9:16` `16:9` `21:9` `5:7` `7:5` · 准确像素如 `2160x3840`；可多选 |
| `--text` | `prompt` 模型按照片写 · `exact` 用你的原文（配合 `--copy "…"`） · `none` 不要文字 |
| `--locale` | 文字语言，如 `zh-CN` `en-US` `ja-JP` `ko-KR` `ar` |
| `--wallpaper` | `linked` 四张风格连贯 · `independent` 四张各自独立 |
| `--wallpaper-size` | 指定设备像素，如 `phone=1440x3200,desktop=3840x2160` |
| `--out` | 换一个输出根目录（默认 `~/Desktop/xxd/xxd-panel-343/`） |
| `--prefs` | `last` 沿用上次 · `edit` 在上次基础上改 · `new` 重新选 · `off` 这次不记住 · `clear` 清除记录 |

- 参数齐全时不再提问，缺什么只问什么。`photo.jpg` 换成文件夹路径就是批量。
- 多选会逐个生成：2 种模式 × 3 种比例 = 6 张，每张都按自己的画布重新构图，不是裁出来的。
- 对照图严格 50:50：通常模型只画设计那一半，再由脚本把原照片原样拼上，所以分界在正中、原照片不会被改。
- 文件名形如 `source-001-street-top-bottom-3x4-1152x1536.png`，全部平铺在一个任务文件夹里。
- 只记住版式、尺寸、文字方式和语言这些设置，不记照片、文案和密钥。

<!-- xxd-readme-ads:start -->
## 关于 XXD

XXD 是小小东品牌名的缩写，本项目由小小东创建并维护：[@xiaoxiaodong01](https://x.com/xiaoxiaodong01)。

## 小小东多端会员 · 699 元/年

> **广告与商业信息声明：** 以下二维码、会员与付费服务链接属于小小东的广告信息。是否扫码或购买完全自愿，不影响本开源项目的访问与使用。

一次年费，同时开通三项会员权益：**知识星球 + 小小东成员提示词库 + 全部 将军总指挥 Skills 会员**。三项权益合并在同一份会员中，无需分别购买。

<!-- xxd-panel-command-system:start -->

### Skills 如何协作

| 层级 | 包含内容 | 用途 |
|---|---|---|
| **General** | [`xxd-panel-all`](https://github.com/xiaoxiaodong-ai/xxd-panel-all) | 识别可用的编号 Skills，按图片、主题和用途推荐，并组织多风格试稿与批量任务。 |
| **Soldier** | `xxd-panel-NNN` | 每个编号执行自己的原始提示词与审美，完成 General 分派的具体任务。 |

<!-- xxd-panel-command-system:end -->

### 会员权益

1. **微信一对一 AI 学习与项目答疑**
   扫描下方二维码，添加小小东微信，围绕 AI 学习、工具使用和实际项目进行一对一沟通，获得答疑与建议；代表性问题将整理为会员内容。
2. **持续更新的成员提示词库**
   [小小东成员提示词库](https://vip.xiaoxiaodong.ai/)当前约有 3.2 万条提示词，会持续整理和扩充，目标超过 10 万条。
3. **全部 将军总指挥 Skills 与使用答疑**
   一份会员覆盖全部 将军总指挥 Skills；使用过程中遇到问题，可以获得相应的使用说明与答疑。
4. **高频刚需优先处理**
   会员提出的高频、刚需提示词与 Skills 需求，会优先评估和开发。

### 如何开通

- 可在[成员网站](https://vip.xiaoxiaodong.ai/)自助开通。
- 也可以扫描下方二维码，添加小小东微信，进行一对一沟通并获得开通协助。

<p align="center"><a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="联系小小东" width="280"></a></p>
<!-- xxd-readme-ads:end -->

## 许可证

本项目（包括 Skill、提示词、脚本、文档及随附样张）采用 **PolyForm Noncommercial License 1.0.0**。完整法律条文请见 [LICENSE](LICENSE)，官方页面见 <https://polyformproject.org/licenses/noncommercial/1.0.0>。

许可范围说明：

- 个人可以用于学习、研究、实验、测试、兴趣项目和私人娱乐；慈善机构、教育机构、公共研究/安全/卫生机构、环保组织及政府机构也可以使用。
- 在**非商业目的**下，你可以使用、复制、修改、制作衍生作品并分享；分享时必须同时提供本许可证（或上面的链接）以及作者提供的所有 `Required Notice:` 声明。
- 不允许用于商业产品或服务、收费交付、出售访问权或许可，或任何预期会带来商业应用的用途。需要商业使用时，请先向版权方另行取得书面许可。
- 本协议只授予其中明确写出的著作权许可和有限的专利许可，不授予商标、品牌名称或其他未明确授予的权利，也不能把你的许可再转授给他人。
- 如果收到书面违约通知，须在 32 天内纠正并采取实际补救措施，否则许可会立即终止；就专利侵权提出书面主张也会终止专利许可。
- 内容按“现状”提供，在法律允许的范围内不作任何担保，使用风险和可能的损失由使用者自行承担。
