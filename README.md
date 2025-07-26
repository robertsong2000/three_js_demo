# 🌌 Three.js 3D Solar System Demo

一个使用 Three.js 构建的交互式3D太阳系模拟器，展示了现代Web 3D图形技术的强大功能。

## ✨ 功能特性

### 🪐 天体系统
- **太阳**: 发光的中心恒星，带有自转动画
- **地球**: 蓝色行星，围绕太阳公转并自转
- **月球**: 地球的卫星，围绕地球公转
- **火星**: 红色行星，独立的轨道运行
- **木星**: 最大的气态巨行星

### 🎮 交互控制
- **鼠标拖拽**: 360度旋转视角观察
- **滚轮缩放**: 自由缩放视距 (10-100单位)
- **空格键**: 暂停/继续动画播放
- **响应式设计**: 自适应不同屏幕尺寸

### 🎨 视觉效果
- **实时光照**: 太阳作为点光源照亮行星
- **阴影系统**: 真实的阴影投射效果
- **星空背景**: 10,000个随机分布的星点
- **轨道线**: 半透明的行星轨道指示线
- **材质效果**: Phong光照模型，支持高光和反射
- **渐变背景**: 深空主题的CSS渐变背景

### 🔧 技术特性
- **模块化代码**: 清晰的函数分离和组织
- **性能优化**: 高效的渲染循环和事件处理
- **跨浏览器兼容**: 支持现代浏览器的WebGL
- **无外部依赖**: 仅依赖Three.js CDN

## 🚀 快速开始

### 环境要求
- 现代浏览器 (Chrome 51+, Firefox 53+, Safari 10+, Edge 79+)
- 支持WebGL的显卡
- 网络连接 (用于加载Three.js CDN)

### 运行方法

1. **直接打开**
   ```bash
   # 在浏览器中直接打开
   open cube.html
   ```

2. **本地服务器** (推荐)
   ```bash
   # 使用Python启动本地服务器
   python -m http.server 8000
   # 或使用Node.js
   npx serve .
   # 然后访问 http://localhost:8000
   ```

3. **Live Server** (VS Code用户)
   - 安装Live Server扩展
   - 右键点击cube.html选择"Open with Live Server"

## 🎯 使用指南

### 基本操作
| 操作 | 功能 |
|------|------|
| 鼠标拖拽 | 旋转视角 |
| 滚轮 | 缩放视距 |
| 空格键 | 暂停/继续 |

### 观察技巧
- **近距离观察**: 滚轮向前滚动，靠近观察行星细节
- **全景视图**: 滚轮向后滚动，查看整个太阳系
- **动态追踪**: 拖拽鼠标跟随行星运动轨迹
- **静态分析**: 按空格键暂停，仔细观察天体位置关系

## 🛠️ 技术架构

### 核心技术栈
- **Three.js 0.160.0**: 3D图形渲染引擎
- **WebGL**: 底层图形API
- **HTML5 Canvas**: 渲染表面
- **ES6+ JavaScript**: 现代JavaScript特性

### 代码结构
```
cube.html
├── HTML结构
│   ├── 容器元素
│   ├── 信息面板
│   └── 控制说明
├── CSS样式
│   ├── 响应式布局
│   ├── 渐变背景
│   └── UI组件样式
└── JavaScript逻辑
    ├── 场景初始化
    ├── 几何体创建
    ├── 材质和光照
    ├── 动画控制
    └── 事件处理
```

### 关键组件

#### 1. 场景管理
```javascript
// 场景、相机、渲染器的初始化
scene = new THREE.Scene();
camera = new THREE.PerspectiveCamera(75, aspect, 0.1, 1000);
renderer = new THREE.WebGLRenderer({ antialias: true });
```

#### 2. 光照系统
```javascript
// 环境光 + 点光源组合
const ambientLight = new THREE.AmbientLight(0x404040, 0.3);
const sunLight = new THREE.PointLight(0xffffff, 2, 100);
```

#### 3. 轨道系统
```javascript
// 使用Group实现层级化的轨道运动
earthOrbit = new THREE.Group();  // 地球轨道
moonOrbit = new THREE.Group();   // 月球轨道
```

## 🎨 自定义扩展

### 添加新行星
```javascript
// 创建新行星的基本模板
const newPlanetOrbit = new THREE.Group();
const newPlanetGeometry = new THREE.SphereGeometry(radius, 32, 32);
const newPlanetMaterial = new THREE.MeshPhongMaterial({
    color: 0xcolor,
    emissive: 0xemissive
});
const newPlanet = new THREE.Mesh(newPlanetGeometry, newPlanetMaterial);
```

### 修改动画速度
```javascript
// 在animate()函数中调整旋转速度
earthOrbit.rotation.y += 0.01;  // 公转速度
earth.rotation.y += 0.02;       // 自转速度
```

### 添加纹理贴图
```javascript
// 使用TextureLoader加载行星纹理
const textureLoader = new THREE.TextureLoader();
const earthTexture = textureLoader.load('path/to/earth-texture.jpg');
const earthMaterial = new THREE.MeshPhongMaterial({
    map: earthTexture
});
```

## 📊 性能优化

### 渲染优化
- 使用`requestAnimationFrame`确保流畅动画
- 启用抗锯齿提升视觉质量
- 合理设置阴影贴图分辨率

### 内存管理
- 复用几何体和材质
- 适当的LOD (Level of Detail) 控制
- 及时清理不需要的对象

## 🐛 常见问题

### Q: 页面显示黑屏
**A**: 检查浏览器是否支持WebGL，或尝试更新显卡驱动

### Q: 动画卡顿
**A**: 降低星空粒子数量或关闭阴影效果

### Q: 鼠标控制不响应
**A**: 确保页面完全加载，检查JavaScript控制台是否有错误

### Q: CDN加载失败
**A**: 检查网络连接，或下载Three.js到本地引用

## 🔮 未来扩展

### 计划功能
- [ ] 添加更多行星和卫星
- [ ] 实现真实的行星纹理贴图
- [ ] 添加彗星和小行星带
- [ ] 支持VR/AR模式
- [ ] 添加行星信息面板
- [ ] 实现时间控制器
- [ ] 添加音效和背景音乐

### 技术改进
- [ ] 使用Web Workers优化计算
- [ ] 实现实例化渲染优化性能
- [ ] 添加后处理效果
- [ ] 支持移动端触摸控制

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

**享受探索宇宙的乐趣！** 🚀✨