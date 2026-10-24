# 婚序·婚礼主持助手 - 应用研发规范

## 应用概览
- 定位：国内婚礼主持人专用免费工具，高端婚礼品牌质感
- 风格：中式喜庆红与香槟金，精致优雅，留白呼吸感
- 核心：手动编辑流程 + 海报导出为主，AI 为增强辅助
- 适配：移动端竖屏优先（最大宽度 480px 居中），桌面端整齐美观

## 设计规范

### 色彩系统（高端婚礼品牌质感）

**主色调**
- 主色·婚礼红：`#B91C3C`（更深沉的中式红，不再艳俗）
- 主色亮：`#D4354F`（hover / 渐变高光）
- 主色暗：`#8B1530`（文字深描边）

**辅助色**
- 香槟金：`#C9A961`（精致低饱和金，装饰用）
- 香槟金亮：`#E8D5A3`（高光 / 渐变）
- 香槟金暗：`#A08040`

**背景**
- 页面背景：`#FBF6F0`（暖调米白，带一点点粉感）
- 卡片背景：`#FFFFFF`（纯白 + 柔光阴影）
- 次级背景：`#FDF9F5`（浅米白，分组/输入框背景）
- 深色纹理背景：渐变 `linear-gradient(135deg, #2C0A14 0%, #5C1525 50%, #8B1530 100%)`（品牌区/海报用）

**文字**
- 主文本：`#1A1414`（暖黑，不冷）
- 次文本：`#6B5C5C`（暖灰）
- 辅助文本：`#A09090`（浅暖灰）
- 白色文本：`#FFFDF8`（暖白，带点米感）

**分割线 / 边框**
- 分割线：`#F0E6DE`（暖米色）
- 边框：`#E8DCD0`（稍深）
- 输入框边框：`#E0D4C8`

**语义色**
- 成功：`#4A9D58`（低饱和绿）
- 警告：`#D4A03A`（金橙色）
- 错误：`#C93030`（暖调红）
- 信息：`#4A7BA0`

### 阴影系统（柔光阴影）
- xs: `0 1px 3px rgba(139, 21, 48, 0.04)`
- sm: `0 2px 8px rgba(139, 21, 48, 0.06)`
- md: `0 4px 16px rgba(139, 21, 48, 0.08)`
- lg: `0 8px 24px rgba(139, 21, 48, 0.10)`
- xl: `0 12px 32px rgba(139, 21, 48, 0.12)`
- 金箔阴影：`0 2px 12px rgba(201, 169, 97, 0.25)`

### 排版（精致优雅中文排版）

**字体族**
- 标题："Noto Serif SC", "Source Han Serif SC", "PingFang SC", "Microsoft Yahei", serif（衬线体，婚礼仪式感）
- 正文："PingFang SC", "Microsoft Yahei", "-apple-system", "Helvetica Neue", Arial, sans-serif
- 数字/英文："Inter", "SF Pro Display", system-ui, sans-serif

**字号层级**
- 品牌大标题：text-3xl font-bold（首页LOGO标题）
- 页面大标题：text-2xl font-bold
- 区块标题：text-xl font-semibold
- 卡片标题：text-lg font-semibold
- 正文：text-base（16px）行高 1.6
- 辅助文字：text-sm（14px）行高 1.5
- 小字/标签：text-xs（12px）

**字重**
- 标题：600-700
- 正文：400-500
- 强调：600

**字间距**
- 标题：tracking-tight（收紧，精致感）
- 正文：tracking-normal
- 小字标签：tracking-wide（散开一点）

### 间距系统
- 页面水平内边距：px-5（20px，更舒适的呼吸感）
- 卡片内边距：p-5
- 卡片间距：gap-4
- 列表项间距：space-y-3
- 区块间距：space-y-6
- 底部导航高度：h-20（80px，更舒展）
- 顶部品牌区高度：约 200px

### 圆角
- 卡片圆角：rounded-2xl（16px，圆润精致）
- 按钮圆角：rounded-full（胶囊形）
- 输入框圆角：rounded-xl（12px）
- 标签/小元素：rounded-lg

### 组件规范

**主按钮**
- 背景：linear-gradient(135deg, #D4354F 0%, #B91C3C 100%)
- 文字：#FFFDF8（暖白）
- 高度：h-12（48px）
- 圆角：rounded-full
- 阴影：0 4px 12px rgba(185, 28, 60, 0.30)
- 字体：font-medium

**次按钮**
- 边框：1.5px solid #B91C3C
- 文字：#B91C3C
- 背景：transparent
- 高度：h-12
- 圆角：rounded-full

**金质按钮（装饰用）**
- 背景：linear-gradient(135deg, #E8D5A3 0%, #C9A961 100%)
- 文字：#5C4520
- 阴影：0 2px 8px rgba(201, 169, 97, 0.4)

**卡片**
- 背景：#FFFFFF
- 圆角：rounded-2xl
- 阴影：shadow-md（柔光）
- 内边距：p-5

**输入框**
- 边框：1px solid #E0D4C8
- 背景：#FDF9F5
- 圆角：rounded-xl
- 高度：h-12
- 聚焦：border-[#B91C3C]，shadow-sm 红色光晕
- 占位符：text-gray-400

**标签 / 徽章**
- 圆角：rounded-full
- 内边距：px-3 py-1
- 字号：text-xs font-medium

### 底部 Tab 导航
- 5 个 Tab：首页、台词库、档期、工具箱、我的
- 高度：h-20（含安全区 padding）
- 背景：白色 + 顶部细分割线
- 选中态：主色图标 + 主色文字 + 上方小圆点指示器（微动效）
- 未选中：灰色图标 + 灰色文字
- 图标尺寸：w-6 h-6
- 字体：text-xs

### 动效规范
- 页面切换：opacity 0→1 + translateY 8px→0，200ms ease-out
- 底部滑出面板：translateY 100%→0，300ms cubic-bezier(0.32, 0.72, 0, 1)
- 背景压暗：opacity 0→0.5，300ms
- 按钮按压：scale 1 → 0.97，100ms
- 列表项出现：stagger 50ms，fade + slide up
- Tab 切换指示器：平滑滑动过渡 250ms cubic-bezier(0.4, 0, 0.2, 1)

## 技术架构

### 数据边界
- 所有数据持久化到服务端数据库，登录后可见
- AI 调用使用插件能力（文本生成 + 文本转JSON）

### 模块划分
- 认证模块：auth（用户信息、AI额度自动初始化）
- 婚礼项目模块：wedding（项目CRUD、流程编辑、海报模板）
- 台词库模块：script（台词分类、收藏、自定义、AI改写）
- 档期模块：schedule（月历+列表双视图、撞单检测、状态标记）
- 工具箱模块：toolkit（彩排清单、应急备忘、合同模板）
- AI模块：ai（流程生成、台词生成、需求解析、风险检测）
- 商店模块：shop（AI充值、海报模板购买、模拟支付）
- 用户模块：user（个人资料、AI额度、订单、收藏）
- 商圈模块：mall（婚庆商家分类展示，广告位预留）
- 问卷模块：questionnaire（新人问卷生成与分享）

### 数据库表
- wedding_projects：婚礼项目
- wedding_steps：婚礼流程环节
- scripts：台词库（系统 + 用户自定义）
- schedules：档期
- ai_quotas：AI额度
- orders：订单
- user_profiles：用户资料
- questionnaires：新人问卷（新增）

### 海报模板
- classic：中式古典（红金配色，传统纹样）
- minimal：现代简约（黑白金，极简排版）
- cinema：电影质感（宽画幅，海报电影风）

