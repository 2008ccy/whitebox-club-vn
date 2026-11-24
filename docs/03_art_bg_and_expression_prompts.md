# 序章美术资产构思单：背景（BG）生图提示词与立绘表情差分规范

> **文档定位**：本文件专为首期「开场 + 序章全三幕」Demo 量身定制，控制美术资产体量在最精炼的 **6 张场景背景图 + 核心表情差分** 范围内，提供统一画风的生图与局部重绘 Prompt，供 Codex 自动化生图脚本或美术管线直接调用。

---

## 1. 场景背景美术（BG）规范与生图 Prompt

### 1.1 画风统一前缀与规格要求
- **输出规格**：`1920 × 1080`（16:9 横构图），导出为高质量 `.webp`，存放路径建议为 `assets/bg/`。
- **空镜原则**：**严禁出现任何人物或路人剪影**（`no humans, no people, empty scene`），前景中央预留角色站立空间，透视平视略微广角（焦距约 28mm～35mm 视觉感），便于叠放半身立绘。
- **共用画风前缀（Style Prefix）**：
  ```text
  Masterpiece anime visual novel background illustration, Kyoto Animation and Makoto Shinkai inspired clean cel-shaded architectural detail, soft natural volumetric lighting, gentle warm highlights, crisp linework, rich lived-in props, 16:9 widescreen, no humans, nobody.
  ```

### 1.2 序章必做 6 张场景明细与专属 Prompt

#### ① `bg_campus_street_day.webp` —— 春日樱影主校道（开场楔子）
- **构思描述**：私立白箱学园依海而建的宽阔石砖主坡道。道路两旁盛开着四月樱花与嫩绿银杏，欧式铸铁街灯挂着校徽旗帜，远处坡道尽头能望见蔚蓝海湾的一角与钟楼尖顶，空气中飘散着几片樱花瓣。
- **主色调**：晴空蓝 `#7BB4E3`、樱粉白 `#FCECEF`、暖米石砖 `#EAE0D5`。
- **完整生图 Prompt**：
  ```text
  [Style Prefix] A sunlit coastal private academy main slope avenue in April spring, clean pale stone pavement leading up toward an elegant European-style school campus, blooming cherry blossom trees and fresh green ginkgo lining both sides, vintage wrought-iron street lamps with navy banners, a glimpse of sparkling blue ocean bay in the distant background, drifting sakura petals in warm morning breeze, cheerful romantic comedy atmosphere.
  ```

#### ② `bg_corridor_404_day.webp` —— 旧校舍四楼走廊与 404 门前（签字起名场景）
- **构思描述**：阳光斜射的复古木地板走廊，左侧是一排能看见窗外樱树梢的半圆木拱窗，右侧尽头是一扇深胡桃木双开门，门上挂着一块稍微歪斜却擦得很亮的黄铜门牌，清晰刻着数字 `404`。
- **主色调**：琥珀木色 `#8C5E3C`、暖白墙裙 `#F5EFE6`、黄铜金 `#C9A35E`。
- **完整生图 Prompt**：
  ```text
  [Style Prefix] Vintage wooden school building fourth-floor hallway in warm afternoon sunlight, tall arched windows on the left casting dappled tree shadows across polished oak floorboards, leading to a distinctive dark walnut classroom door on the right with a slightly crooked brass nameplate reading "404", nostalgic cozy academy interior, dust motes dancing in sunbeams.
  ```

#### ③ `bg_room_404_day.webp` —— 旧校舍 404 活动室·晴昼（序章第一、二幕核心主场）
- **构思描述**：充满反差喜剧细节的宽敞活动室！天花板中央突兀地挂着一盏极其奢华的欧式水晶吊灯（GPT 超纲装修杰作）；靠窗摆着拼凑的长木桌；后方黑板上用粉笔写着端正标语与便利贴；右侧茶水柜上放着一台冒热气的**大号白色电饭煲**和锃亮不锈钢碗（DeepSeek 干饭角）；墙角放着一台贴满黄色警示胶带的碎纸机（防 Gemini 删稿）和天鹅绒软垫长椅。
- **主色调**：暖木棕 `#9E734E`、奶油阳光 `#FFF8EB`、天鹅绒暗红点缀 `#8C2338`。
- **完整生图 Prompt**：
  ```text
  [Style Prefix] Spacious eccentric high school clubroom interior in bright afternoon sun, arched wooden windows overlooking green trees, an absurdly luxurious sparkling crystal chandelier hanging from a vintage timber ceiling, long wooden meeting table in center, green chalkboard covered with colorful sticky notes in back, a cozy tea counter on the right featuring a large steaming white electric rice cooker and a shiny stainless steel bowl, a paper shredder taped with warning stickers in the corner, crimson velvet window bench on the left, charming chaotic clubroom full of personality.
  ```

#### ④ `bg_room_404_sunset.webp` —— 旧校舍 404 活动室·暮橙夕照（序章第三幕派单与尾声）
- **构思描述**：与 `bg_room_404_day.webp` **保持完全一致的房间构图**（建议基于昼版做图生图光影重绘），窗外变为绚烂的金橙色海湾晚霞，头顶那盏豪华水晶吊灯点亮柔和暖黄灯光，整个房间笼罩在温馨治愈的放学后氛围中。
- **主色调**：晚霞金橙 `#E88A45`、暖紫暗部 `#5E4B6E`、吊灯暖光 `#FFE6B3`。
- **完整生图 Prompt**：
  ```text
  Same exact room layout and camera angle as bg_room_404_day, transformed into golden hour sunset lighting. Deep orange and violet twilight sky outside the arched windows, warm golden rays stretching across the wooden table, the crystal chandelier softly lit with cozy amber glow, nostalgic and heartwarming after-school clubroom atmosphere, no humans.
  ```

#### ⑤ `bg_wisteria_tea_day.webp` —— 东庭紫藤回廊·蓝晒茶寮（序章第二幕经费谈判）
- **构思描述**：白箱学园东侧的新中式园林庭院回廊。藤蓝色的紫藤花穗从木构廊架垂落，廊边竹架上晾晒着几幅印有白色植物剪影的靛蓝“蓝晒”染布，圆石桌上摆着青瓷茶壶、折扇与一本厚账簿。
- **主色调**：藤萝紫蓝 `#6E78C2`、青瓷白 `#E8EFEA`、温润楠木 `#6B4E3D`。
- **完整生图 Prompt**：
  ```text
  [Style Prefix] Serene Neo-Chinese style courtyard corridor inside an academy, cascading wisteria flowers in soft blue-violet hues hanging from wooden pergola beams, indigo cyanotype dyed fabric sheets with white fern silhouettes drying gently on bamboo racks in background, a carved stone table in foreground set with celadon teacups and a neat ledger book, dappled spring sunlight.
  ```

#### ⑥ `bg_prism_music_day.webp` —— 西馆音乐室·棱镜琴房（序章第三幕广播线索调查）
- **构思描述**：明亮洁净的古典音乐教室兼午休广播录音角。落地高窗前停放着一架黑色三角钢琴，窗框悬挂的一枚透明玻璃三棱镜将阳光折射成一道柔和的七彩彩虹投在浅色墙面上，谱架旁放着复古广播麦克风。
- **主色调**：月光银白 `#F2F1F7`、钢琴烤漆黑 `#23242E`、棱镜柔彩光谱。
- **完整生图 Prompt**：
  ```text
  [Style Prefix] Sunlit classical high school music room and campus radio booth, glossy black grand piano beside tall paned windows, a hanging clear glass triangular prism catching sunlight and casting a delicate rainbow spectrum onto the cream wall, vintage silver broadcast microphone on a small desk with sheet music stands, airy musical elegance.
  ```

---

## 2. 角色立绘表情差分规范（供 Codex 图层编辑管线使用）

### 2.1 差分制作总原则
- **底图基准**：以 `../ai-wardrobe/assets/sprites/<id>-1-front.webp` 为唯一母版（定义为 `normal` 默认态），**严格锁定身体姿态、服饰褶皱、发丝外轮廓与透明通道不变**，仅重绘面部五官、腮红、汗珠及头顶局部动态特征（如呆毛角度、猫耳高低），确保在游戏内切换表情时身体零跳帧！
- **命名与存放规范**：`assets/sprites/<id>-1/<exp>.webp`（例如 `assets/sprites/deepseek-1/thinking.webp`）。

### 2.2 五大女主角 8 组标准表情 Prompt 矩阵

| 表情 ID | 情绪用途 | 通用面部调整指令（结合下方角色专属细节） |
| :--- | :--- | :--- |
| `normal` | 常态微笑 | 直接复用现有 `<id>-1-front.webp`，无需重绘 |
| `happy` | 开心灿笑 | 弯弯月牙笑眼或明亮星眸，嘴角轻快上扬露齿笑，暖色红润气色 |
| `blush` | 害羞傲娇 | 双颊浮现柔和绯红红晕与细微斜线腮红，视线微微偏开不敢直视，嘴唇轻抿 |
| `shock` | 震惊吃瘪 | 瞳孔微缩睁大双眼，嘴巴微张呈小 O 型，头顶呆毛/耳朵竖直 |
| `smug` | 得意坏笑 | 半眯眼自信神态，挑眉，嘴角歪起俏皮弧度 |
| `panicked` | 慌张破防 | 眉毛呈八字苦恼状，脸侧挂一颗晶莹动漫汗珠（Gemini 专属为泪汪汪荷包蛋眼） |
| `thinking` | 闭眼推演 | 双眼轻闭，神情专注沉思，食指或眉宇带推理感 |
| `gentle` | 温柔心动 | 眼神柔和清澈，浅浅微笑，眉眼舒展充满包容感 |

### 2.3 各角色专属表情细节锚点（重绘必读！）
1. **GPT（`gpt-1`）**：
   - `happy`：双手捧心气场的满分营业甜笑，浅紫眼眸闪烁温柔高光（夸夸群模式）。
   - `panicked`：被拆穿胡编校规时的光速心虚笑，脸颊带小汗珠，耳尖与白角根部微红。
2. **Claude（`claude-1`）**：
   - `smug`：拍出 `Suspended` 黄牌时的端庄严厉风纪脸，下巴微抬，琥珀瞳凛然认真。
   - `blush`：极度纯情的耳根通红，眼神飘向一旁（低头想戳小螃蟹的口嫌体正直感）。
3. **Gemini（`gemini-1`）**：
   - **异色瞳铁律**：任何睁眼差分必须严格保持 **画面左眼（角色右眼）为玫粉色，画面右眼（角色左眼）为鎏金色**！
   - `panicked`（核心名场面表情）：双瞳蓄满大颗晶莹泪珠但未滑落，猫耳向两侧压低呈可怜飞机耳，波浪嘴哭唧唧（删稿破防专属）。
4. **Grok（`grok-1`）**：
   - `smug` & `happy`：**必须清晰保留嘴角那颗标志性的俏皮小尖牙（cute single little fang）**！
   - `blush`：傲娇被夸奖后的炸毛脸红，咬着小尖牙别扭皱眉。
5. **DeepSeek（`deepseek-1`）**：
   - `thinking`（R1 深度思考专属）：双眼紧闭，眉毛微微认真蹙起，头顶弯翘呆毛周围可带两道极淡的旋转动感弧线。
   - `shock`：被叫“蓝色大肥鱼”或听到“喵”字时的瞳孔地震，两侧鲸鳍耳瞬间羞红竖起！

### 2.4 序章三位配角精简表情清单
- **GLM（`glm-1`）**：`normal`（默认冷面） + `strict`（皱眉严厉审视） + `gentle`（极细微的嘴角软化，放过 404 室时使用）。
- **Qwen（`qwen-1`）**：`normal`（默认温婉浅笑） + `happy`（眯眼腹黑笑面虎，谈及经费考核时使用）。
- **Kimi（`kimi-1`）**：`normal`（默认三棱镜柔光浅笑） + `happy`（温柔治愈笑颜）。
