# 🌌 Three.js 演示项目集合

一个包含多个Three.js演示的项目集合，展示了现代Web 3D图形技术的强大功能和多样性。

## 📁 项目结构

```
three_js_demo/
├── cube.html              # 🌌 3D太阳系演示
├── particle_wave.html     # 🌊 交互式粒子波浪
├── morphing_geometry.html  # 🔄 几何变形演示
├── audio_visualizer.html  # 🎵 3D音频可视化器
└── README.md              # 📖 项目文档
```

## 🎯 演示项目

### 1. 🌌 3D太阳系演示 (`cube.html`)

一个完整的太阳系模拟器，展示天体运动和光照效果。

#### ✨ 功能特性
- **天体系统**: 太阳、地球、月球、火星、木星
- **真实物理**: 公转、自转、轨道运动
- **视觉效果**: 实时光照、阴影、星空背景
- **交互控制**: 鼠标拖拽、滚轮缩放、空格暂停

#### 🎮 操作方式
| 操作 | 功能 |
|------|------|
| 鼠标拖拽 | 旋转视角 |
| 滚轮 | 缩放视距 |
| 空格键 | 暂停/继续 |

### 2. 🌊 交互式粒子波浪 (`particle_wave.html`)

一个高性能的粒子系统演示，展示多种视觉效果模式。

#### ✨ 功能特性
- **粒子系统**: 10,000个动态粒子
- **多种模式**: 波浪、螺旋、爆炸、漩涡、脉冲
- **实时交互**: 鼠标控制波浪形态
- **性能监控**: FPS显示、实时统计
- **自定义着色器**: GLSL顶点和片段着色器

#### 🎮 操作方式
| 操作 | 功能 |
|------|------|
| 鼠标移动 | 控制波浪 |
| 滚轮 | 调整视角 |
| 1-5键 | 切换效果模式 |
| 空格键 | 暂停/继续 |
| R键 | 重置波浪 |

#### 🎨 效果模式
1. **波浪模式**: 经典的正弦波效果
2. **螺旋模式**: 螺旋上升的粒子流
3. **爆炸模式**: 径向爆炸效果
4. **漩涡模式**: 旋转漩涡动画
5. **脉冲模式**: 节拍式脉冲效果

### 3. 🔄 几何变形演示 (`morphing_geometry.html`)

展示3D几何体之间的平滑变形动画和材质效果。

#### ✨ 功能特性
- **几何变形**: 球体、立方体、圆柱体、圆环、八面体
- **平滑过渡**: 顶点插值动画
- **动态材质**: 颜色变化、脉冲效果
- **多种模式**: 颜色模式、线框模式、光照切换
- **实时信息**: 顶点数、面数、变形进度

#### 🎮 操作方式
| 操作 | 功能 |
|------|------|
| 点击按钮 | 切换几何形状 |
| 鼠标拖拽 | 旋转视角 |
| 滚轮 | 缩放 |
| 空格键 | 暂停动画 |
| C键 | 切换颜色模式 |
| W键 | 切换线框模式 |
| L键 | 切换光照 |
| ↑↓键 | 调整动画速度 |

#### 🎨 几何形状
- 🔮 **球体**: 经典的球形几何
- 📦 **立方体**: 分段立方体
- 🥫 **圆柱体**: 圆柱形几何
- 🍩 **圆环**: 甜甜圈形状
- 💎 **八面体**: 钻石形几何

### 4. 🎵 3D音频可视化器 (`audio_visualizer.html`)

一个实时的3D音频频谱可视化器，支持多种音频源和可视化模式。

#### ✨ 功能特性
- **多音频源**: 文件上传、麦克风输入
- **可视化模式**: 频谱柱状图、波形图、球形频谱、环形频谱
- **实时分析**: Web Audio API频谱分析
- **交互控制**: 灵敏度调节、平滑度控制
- **颜色主题**: 多种动态颜色方案

#### 🎮 操作方式
| 操作 | 功能 |
|------|------|
| 选择文件 | 加载音频文件 |
| 麦克风按钮 | 使用麦克风输入 |
| 模式按钮 | 切换可视化模式 |
| 鼠标拖拽 | 旋转视角 |
| 滚轮 | 缩放 |
| 1-4键 | 快速切换模式 |
| C键 | 切换颜色主题 |
| F键 | 全屏模式 |

#### 🎨 可视化模式
1. **频谱柱状图**: 经典的频率柱状显示
2. **波形图**: 音频波形的3D线条
3. **球形频谱**: 球面分布的频谱点
4. **环形频谱**: 多层环形频谱显示

## 🚀 快速开始

### 环境要求
- 现代浏览器 (Chrome 51+, Firefox 53+, Safari 10+, Edge 79+)
- 支持WebGL的显卡
- 网络连接 (用于加载Three.js CDN)

### 运行方法

1. **直接打开**
   ```bash
   # 在浏览器中直接打开任意HTML文件
   open cube.html
   open particle_wave.html
   open morphing_geometry.html
   open audio_visualizer.html
   ```

2. **本地服务器** (推荐)
   ```bash
   # 使用Python启动本地服务器
   python -m http.server 8000
   # 或使用Node.js
   npx serve .
   # 然后访问对应的HTML文件
   # http://localhost:8000/cube.html
   # http://localhost:8000/particle_wave.html
   # http://localhost:8000/morphing_geometry.html
   # http://localhost:8000/audio_visualizer.html
   ```

3. **Live Server** (VS Code用户)
   - 安装Live Server扩展
   - 右键点击HTML文件选择"Open with Live Server"

## 🛠️ 技术架构

### 核心技术栈
- **Three.js 0.160.0**: 3D图形渲染引擎
- **WebGL**: 底层图形API
- **GLSL**: 自定义着色器语言
- **HTML5 Canvas**: 渲染表面
- **ES6+ JavaScript**: 现代JavaScript特性

### 技术特色

#### 1. 太阳系演示
- 层级化场景管理
- 物理光照模型
- 阴影映射技术
- 粒子系统背景

#### 2. 粒子波浪
- 自定义GLSL着色器
- 高性能粒子渲染
- 实时uniform传递
- 加法混合模式

#### 3. 几何变形
- 顶点插值算法
- 动态几何更新
- 材质动画系统
- 缓动函数应用

#### 4. 音频可视化器
- Web Audio API集成
- 实时频谱分析
- 多种可视化算法
- 动态颜色映射

## 🎨 自定义扩展

### 添加新的粒子效果
```javascript
// 在particle_wave.html中添加新模式
if (mode == 6.0) {
    // 自定义效果
    pos.y = sin(distance * 0.05 + time) * 25.0;
}
```

### 创建新的几何形状
```javascript
// 在morphing_geometry.html中添加新形状
const geometries = {
    // 现有形状...
    pyramid: () => new THREE.ConeGeometry(15, 25, 4)
};
```

### 修改材质效果
```javascript
// 自定义材质属性
const material = new THREE.MeshPhongMaterial({
    color: 0xff6b6b,
    shininess: 100,
    transparent: true,
    opacity: 0.9
});
```

## 📊 性能优化

### 渲染优化
- 使用`requestAnimationFrame`确保流畅动画
- 启用抗锯齿提升视觉质量
- 合理设置阴影贴图分辨率
- 使用加法混合减少overdraw

### 内存管理
- 复用几何体和材质
- 及时更新缓冲区属性
- 适当的LOD控制
- 清理不需要的对象

### 着色器优化
- 减少片段着色器计算
- 使用uniform传递常量
- 避免条件分支
- 优化纹理采样

## 🐛 常见问题

### Q: 页面显示黑屏
**A**: 检查浏览器WebGL支持，更新显卡驱动

### Q: 粒子效果卡顿
**A**: 降低粒子数量或简化着色器计算

### Q: 几何变形不平滑
**A**: 确保源和目标几何体顶点数匹配

### Q: 鼠标控制不响应
**A**: 检查JavaScript控制台错误，确保页面完全加载

## 🔮 未来扩展

### 计划功能
- [ ] 添加更多粒子效果模式
- [ ] 实现几何体纹理贴图
- [ ] 添加音频可视化
- [ ] 支持VR/AR模式
- [ ] 添加物理引擎集成
- [ ] 实现实时阴影
- [ ] 添加后处理效果

### 技术改进
- [ ] 使用Web Workers优化计算
- [ ] 实现实例化渲染
- [ ] 添加GPU粒子系统
- [ ] 支持移动端触摸控制
- [ ] 优化内存使用
- [ ] 添加性能分析工具

## 📚 学习资源

### Three.js官方资源
- [Three.js官方文档](https://threejs.org/docs/)
- [Three.js示例](https://threejs.org/examples/)
- [Three.js编辑器](https://threejs.org/editor/)

### WebGL学习
- [WebGL基础教程](https://webglfundamentals.org/)
- [GLSL着色器教程](https://thebookofshaders.com/)
- [GPU Gems系列](https://developer.nvidia.com/gpugems/gpugems/contributors)

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

### 贡献指南
1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📞 联系方式

如有问题或建议，请通过以下方式联系：
- 提交 GitHub Issue
- 发送邮件至项目维护者

---

**探索3D图形的无限可能！** 🚀✨🎨