# F1-note 个人知识管理系统

> 🎓 面向华南理工大学学生的个人知识管理工具，集成了 AI 智能摘要、知识图谱可视化等功能。
> 🏆 **荣获 2025 腾讯黑客松大赛一等奖**

**主要开发者**：田田
**合作成员**：章予涵

> [!IMPORTANT]
> ⏳ **代码正在整理和审核中，即将开源，敬请期待！**
> 欢迎先点右上角 ⭐ **Star** 收藏本仓库，开源后第一时间获取通知！

---

## ✨ 项目亮点

1. **智能化**：集成多种 AI 模型，自动提取文档摘要和关键词。
2. **用户友好**：直观的界面设计，流畅的交互体验，华工主题设计。
3. **技术先进**：现代化技术栈（React 18 + FastAPI），模块化架构设计。
4. **扩展性强**：清晰的代码结构，便于功能扩展。
5. **华工特色**：融入华工红（#CC0000）等学校元素，贴合华工学生需求。

---

## 🛠️ 技术架构

### 前端技术栈（React）
- **核心框架**：React 18.2.0
- **UI组件库**：Ant Design 5.12.8
- **样式方案**：TailwindCSS 3.3.6 + @tailwindcss/typography
- **图标库**：Lucide React + Ant Design Icons
- **PDF处理**：pdfjs-dist 3.11.174
- **Markdown渲染**：react-markdown 8.0.7
- **知识图谱**：vis-network 9.1.6

### 后端技术栈（FastAPI）
- **Web框架**：FastAPI 0.104.1 + Uvicorn
- **数据库**：SQLite + SQLAlchemy 2.0.23
- **文件处理**：python-multipart, PyPDF2, pdfminer.six
- **AI集成**：OpenAI API, Hugging Face模型
- **跨域支持**：CORS中间件

---

## 🚀 核心功能模块

1. **文档管理系统**
   - PDF文件上传与存储
   - 智能后端端口检测（9000-9005）
   - AI自动摘要提取、关键词智能标签化
   - 文档搜索与标签筛选、批量删除操作、摘要重新生成
2. **AI智能处理引擎**
   - PDF文本提取（支持多页处理、智能元数据提取、文本质量验证）
   - Hugging Face模型集成（异步加载、摘要生成、关键词提取、模型状态监控）
3. **RESTful API设计**
   - 涵盖服务状态检查、健康检查、AI模型状态、PDF上传、文档列表获取、单/批量删除、摘要重新生成等核心端点。
4. **前端组件架构**
   - 主应用（侧边栏导航、页面路由管理、华工主题设计）
   - 首页仪表板（每日灵感展示、快速统计面板、功能快捷入口）

---

## 📁 项目结构预览

```text
F1-note-backend/
├── main.py                     # FastAPI主应用，API路由定义
├── db.py                       # SQLAlchemy数据库模型和配置
├── requirements.txt            # Python依赖管理
├── AI处理模块 (src/)
│   ├── pdf_utils_optimized.py  # 优化的PDF文本提取
│   ├── huggingface_models.py   # Hugging Face模型集成
│   └── pdf_utils.py            # 基础PDF处理工具
├── React前端 (src/)
│   ├── App.jsx                 # 主应用组件，路由管理
│   ├── components/
│   │   ├── HomePage.jsx        # 首页仪表板
│   │   ├── NotesPage.jsx       # 笔记管理核心页面
│   │   ├── KnowledgeGraphPage.jsx # 知识图谱可视化
│   │   └── InspirationPage.jsx # 灵感卡片管理
│   └── utils/
│       ├── fileProcessor.js    # 文件处理工具
│       └── openaiService.js    # OpenAI API集成
└── 配置文件
    ├── package.json            # 前端依赖和脚本
    ├── tailwind.config.js      # TailwindCSS配置
    └── postcss.config.js       # PostCSS配置
