# 🎵 Arc-music

一个基于Nextjs的网页本地音乐播放器，提供流畅的音乐播放体验。（lite分支为调用gdstudio api版，可直接部署到vercel等平台使用）
* pc端:
![k3jT5GMpn9HXntiFYYsZmgyEXnXv5iQ0.jpg](https://cdn.nodeimage.com/i/k3jT5GMpn9HXntiFYYsZmgyEXnXv5iQ0.jpg) 
* 移动端
![LtQgFXl37PSNIHvXtISnrSuXe2dWoHAH.jpg](https://cdn.nodeimage.com/i/LtQgFXl37PSNIHvXtISnrSuXe2dWoHAH.jpg) 


## ✨ 特性
- 🤓 **开箱即用** - 使用浏览器就能访问服务器的音乐
- 🎨 **现代化设计** - 简洁美观的玻璃态设计风格，适配pc和手机设备
- 🎶 **多功能播放** - 支持播放、暂停、上一曲、下一曲、进度控制、歌曲分享（直链）、列表播放、随机播放、歌曲搜索
## 🚀 快速开始

### 环境要求

- chrome或edge等内核较新的浏览器（webview版本较低及旧版Safari可能存在错）
- 本地或服务器环境（推荐，因为音乐存储在本地，未来可能加入api功能可轻量化部署vercel等paas平台）

### 安装步骤

1. **克隆项目**
```bash
git clone https://github.com/armjukl/arc-music.git
cd arc-music
```
2. **自定义配置**

 * 将音乐文件放入 `public/music/` 目录

* 更改背景图
在public/bg/目录下上传图片，在components/MusicPlayer.tsx中441行中修改图片地址，示例
```
 backgroundImage: "url('/bg/3.jpeg')"
```


3. **修改好启动后**
```bash
# 安装npm和nodejs后
npm install
npm run build
npm start
```

3. **访问应用**
* 打开浏览器访问 `http://localhost:3000` 可配置反向代理或cdn
* 访问 `http://localhost:3000/api/music` 即可看到自动生成的歌曲列表json
```javascript
[
  {
    "id": 1,
    "name": "STAY",
    "url": "/music/STAY.mp3"
  },
  {
    "id": 2,
    "name": "test",
    "url": "/music/test.mp3"
  }
......
]
```


## 🎮 使用方法

### 播放器

- **左随机按钮**：随机选择歌曲播放
- **右随机按钮**：切换单曲循环或随机播放或列表播放


### 播放列表

1. 点击任意歌曲开始播放
2. 使用搜索框快速查找歌曲 


## 📝 开发计划

- [ ] 增加api获取歌曲
- [ ] bilibili解析
- [ ] 收藏功能
- [ ] 播放历史
- [ ] 夜间模式
- [ ] 莫奈取色

## 📁 主要项目结构

```
arc-music/             
├── components/
│   └── MusicPlayer.tsx    # 主页面
├── pages/
│   ├── index.tsx          # 提供默认跳转
│   ├── api/
│   │   └── music.ts   #播放列表生成
│   └── _app.tsx     
├── public/
│   ├── bg/            # 背景图片
│   └── music/         # 示例音乐文件
└── README.md
```

## 🐛 问题反馈

如果您遇到任何问题，请通过以下方式反馈：

1. 查看 [Issues](https://github.com/armjukl/arc-music/issues) 页面
2. 创建新的 Issue，描述详细的问题和复现步骤
3.联系qq

## 🙏 致谢

- 感谢所有贡献者
- 感谢cto.new提供gpt5支持
- 感谢各大音乐网站提供音乐下载

---

**享受音乐！** 🎧

如果这个项目对您有帮助，请给个 ⭐️ 支持！
