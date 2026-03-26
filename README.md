# TwinWeld：基于 WebGL 的轻量化焊接机器人数字孪生仿真系统

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Web-orange.svg)
![Tech](https://img.shields.io/badge/tech-Three.js-green.svg)

**TwinWeld** 是一款专为中等职业学校焊接专业学生设计的轻量化工业机器人仿真平台。它利用数字孪生技术，在浏览器端实现了高精度的机器人示教、编程与焊接轨迹仿真，旨在解决实训设备昂贵、耗材成本高及操作风险大等现实教学痛点。

---

## 🌟 核心特性 (Key Features)

- **🚀 轻量化 Web 架构**：基于 WebGL (Three.js) 开发，无需安装任何插件，即开即用，支持跨平台访问。
- **🤖 自研运动学算法**：内置工业级六轴机器人正/逆运动学 (FK/IK) 求解器，支持笛卡尔坐标与关节角度的实时转换。
- **📦 自定义模型导入**：支持 STL 等多种格式的 3D 工件模型上传，并具备智能坐标对齐（Z 轴向上）与网格吸附功能。
- **🎮 虚拟示教编程**：模拟真实工业示教器交互，支持记录点位、轨迹插补计算及全流程仿真回放。
- **🛠 几何体快速建模**：内置参数化几何体生成工具（方块、圆柱、带坡口平板等），快速搭建实训场景。
- **📐 高精度仿真**：支持 1mm 级别的位移控制与角度吸附，确保仿真逻辑与工业实际标准对标。

---

## 🛠 技术栈 (Tech Stack)

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **3D Engine**: [Three.js](https://threejs.org/) (WebGL)
- **UI Components**: Lucide Icons, Custom CSS Components
- **Algorithms**: 自研六轴机器人 D-H 参数模型及逆运动学求解逻辑

---

## 🚀 快速开始 (Quick Start)

### 环境要求
- 现代浏览器（Chrome, Edge, Firefox, Safari 等）
- 建议开启硬件加速以获得最佳性能

### 本地运行
1. 克隆仓库：
   ```bash
   git clone https://github.com/your-username/TwinWeld.git
   ```
2. 进入项目目录：
   ```bash
   cd TwinWeld
   ```
3. 使用静态服务器运行（例如使用 VS Code 的 Live Server 插件，或使用 Python）：
   ```bash
   # Python 3
   python -m http.server 3000
   ```
4. 在浏览器访问 `http://localhost:3000/public/robot_simulation.html`

---

## 📖 使用指南 (Usage Guide)

1. **导入工件**：点击右侧面板的“上传模型”或使用“基本几何体”生成焊接对象。
2. **位置调整**：选中模型后，使用 TransformControls（平移/旋转手柄）或右侧输入框精确调整工件位置。
3. **示教编程**：
   - 操控机器人末端到达目标点。
   - 点击“记录点位”保存当前坐标。
4. **仿真回放**：点击“运行仿真”，机器人将按照记录的路径执行焊接动作。
5. **视图切换**：使用鼠标左键旋转相机，右键平移，滚轮缩放。

---

## 📄 开源协议 (License)

本项目采用 [MIT License](LICENSE) 开源协议。

---

*注：本项目旨在推动职业教育数字化转型，欢迎各位开发者提交 Issue 或 Pull Request 共同完善。*
