凡纳弘途是使命驱动的酒店、旅居与延展服务企业构建者。业务覆盖酒店、旅居、康养与延展服务；赛道：酒店旅居 · 康养服务 · 企业构建；受众：酒店业主 · 旅居运营方 · 康养品牌。

## 品牌身份 Identity

- 主名称永远是 **凡纳弘途**（主语言：中文）。英文名 **VANAHOM** 作为标注的别名出现：`凡纳弘途 VANAHOM`，不要反过来。
- IP ID / asset key：`vanahom`。子品牌：**AXISEE**（AI 原生的“第二大脑”）与 **SANCTEM**（疗愈与康养，见 SANCTEM 章节）。
- 品牌理念：**为者常成，行者常至** — *Building Tomorrow, Today*（出处《晏子春秋》）。品牌承诺：**明德至善，渐入佳境** — *To elevate the human experience*（出处《大学》）。
- 名字寓意：“VANA”源自梵语“森林”，象征稳定、可持续的生态体系；“HOM”代表宇宙的根本之音，去繁存简；“凡纳弘途”即“博纳万物之凡，弘扬大道之途”。

## 内容与语气 Voice

- **精准、温暖、以证据说话，东西方兼容的视野。** 先讲具体结果和有名有姓的成果，人在中心：“为超10000家酒店搭建收益管理体系与数据看板，实现收益倍增。”
- 双语并置时以中文领先、英文镜像关键术语：“品牌开创与标准起草”后可接 “Brand DNA”“Tone of Voice”。
- 引用格言必配出处，用 `Maxim` 组件：格言 + 英文行 + “出处 -《…》”。
- 句式简洁、名词具体。服务描述的结构：**服务定义**（一句话说清是什么）→ **服务内容（基础版）**（分组的要点）→ 脚注“*上述服务内容仅供参考，实际内容以项目服务建议书为准。”
- 人物姓名写作 `中文名 English NAME`（姓氏大写）：陈鹏飞 David CHEN。
- 不要：夸张承诺、“颠覆”类词汇、空洞术语、制造焦虑；不披露未公开的财务、股权或内部关系。不用 emoji。

## 色彩 Color

- **白色是底。** 页面以 `paper` 为地，`mist` 用于安静的分区底。每个视图至少 40% 留白。
- **弘途红 `hongtu-red` 是唯一的主色，任何视图不超过 8%。** 用于：字标、页头的品牌词与 96px 红线（`SectionTitle`）、表头（`ServiceMatrix`）、唯一的主行动按钮、照片后方的偏移色块（`CaseStudy`）。
- 白底上的红色文字用 `hongtu-red-deep`（9.0:1）：正文中被点名的服务或成果、人物角色、项目标题。红色永远不做长段正文的背景；唯一例外是 `BioBanner` 里的短行标题（白字 6.68:1）。
- `red-wash` 是淡红底：矩阵的行标题、激活与聚焦态填充。
- 苍灵灰 `cangling-grey` 是辅色：细线、分隔、eyebrow。它在白底上只有 2.27:1，不承载必须读到的信息；需要可读的灰字用 `grey-deep`（4.75:1，仅在 `paper` 上）。
- 正文 `ink-soft`，标题 `ink`。细线 `line`（1px，`hairline`）。
- SANCTEM 的陶土色（`sanctem-*`）只属于 SANCTEM，不得与 `hongtu-red` 出现在同一区块，也不得进入 VANAHOM 企业页面。

## 字体 Typography

- 配对：**衬线用于展示与声音，无衬线用于结构。**
  - `display` 族：Cormorant Garamond（英文）+ Noto Serif SC（中文），字重 400–600，字距 -0.01em，行高 1.06，`text-wrap: balance`。样式 `mega` `display` `h1` `h2` `h3`。
  - `sans` 族：Manrope（英文）+ Noto Sans SC（中文），只用 400 / 500 / 600。样式 `lead` `body` `body-strong` `label` `small` `eyebrow` `micro`。
- 字号是流式的，token 记录的是最大值；按各样式说明使用 `clamp()`：如 `h1` = clamp(32px, 4.6vw, 64px)，`body` 固定 16px。
- 只有 `eyebrow` 全大写（12px，0.18em）。其余一律句首大写或中文常规排写。
- `lead` 用 `grey-deep`，`text-wrap: pretty`。
- 四款字体均为 Google Fonts 托管字体，`components/bundle.css` 首行已 `@import`。注意：中国大陆网络常无法访问 Google Fonts；面向大陆受众的正式站点应自托管字体文件（见 REVIEW.md）。
- 待确认：现有提案 PPT（v0.4）的英文为几何无衬线（Montserrat 风格）、中文为思源黑体；IPTrust 准则规定的是 Cormorant Garamond + Manrope。本系统按准则执行，提案与准则的差异需品牌方裁定（见 REVIEW.md）。

## 版式与间距 Layout & spacing

- 8pt 体系：`space-1` 4 · `space-2` 8 · `space-3` 12 · `space-4` 16 · `space-6` 24 · `space-10` 40 · `space-16` 64 · `space-24` 96 · `space-32` 128。区块节奏 `section`：clamp(64px, 10vw, 140px)。
- 页头（`SectionTitle`）在左上，字标在右上，与之对齐。左右边距：提案幻灯片约为 96px，网页可用 `space-24`（宽屏）到 `space-6`（手机）——此为建议值，官方准则未规定。
- 常见页面骨架（来自提案）：左文右图 50/50（`CaseStudy`）；四列矩阵（`ServiceMatrix`）；三列人物卡（`TeamCard`）；人物详情页 = `BioBanner` + 双栏“专业背景 / 主要项目经验”，栏标题下有一条短红线。

## 形状、边框、阴影 Shape

- 方角：默认 `radius-none`，控件最多 `radius-sm`（2px）。
- **没有阴影。** 结构来自 1px 细线（`hairline` + `line`）和留白。照片后的红色偏移块是实色块，不是阴影。
- `TeamCard` 的切角（左上、右下 24px）是唯一的装饰形状。

## 动效 Motion

- 克制：淡入 + 8px 上移，`motion-base`（320ms）ease-out。尊重 `prefers-reduced-motion`；内容后面不放循环或俏皮动画。

## 影像 Imagery

- 官方准则未单列影像规则。以下观察自 v0.4 提案，待品牌方确认后再作为硬性规定：使用真实项目实景（酒店、窑洞宾馆、山居民宿）；照片方角，与全系统的 `radius-none` 一致；人物照片使用团队本人。
- 不要用图库人物冒充项目或团队。

## 图标 Iconography

- 品牌未提供图标集。提案中仅有少量线性图标（地图上的细线旗帜、SANCTEM 矩阵中的圆形图标）。需要图标时使用 1px–1.5px 线性、方端点的图标，颜色 `ink` 或 `grey-deep`；不使用 emoji。此项为待补充内容。

## 标志 Logo

- 字标为 SVG（`assets/Logos/`，由官方 PNG 描摹而成，非设计师原稿；官方 SVG 到位后应替换），通过 `Wordmark` 组件放置：红色为主，红底用白色，红色横幅上用灰色，单色印刷用墨色。
- 安全空间：四周至少一个 V 的高度。不重新排字、不改色、不加渐变阴影、不拉伸旋转。

## 始终 / 绝不 Always / Never

- 始终：让所有人都在故事里——企业、利润与人；用具体成果；让留白工作；格言配出处。
- 绝不：满屏红色；把 SANCTEM 陶土色混入企业页面；挤压或改色字标；过度推销、贩卖焦虑、堆砌术语。
