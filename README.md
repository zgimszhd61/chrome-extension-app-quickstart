# chrome-extension-app-quickstart
以下是一个最简单的 Chrome 插件的完整代码示例。这个插件会在用户点击浏览器中的插件图标时，弹出一个带有 "Hello, World!" 的弹出窗口。

### 文件结构
你需要创建一个包含以下文件的文件夹：

```
my-simple-chrome-extension/
│
├── manifest.json
├── popup.html
└── popup.js
```

### 1. manifest.json

```json
{
  "manifest_version": 3,
  "name": "My Simple Chrome Extension",
  "version": "1.0",
  "description": "A simple Chrome extension that says Hello, World!",
  "action": {
    "default_popup": "popup.html",
    "default_icon": {
      "16": "icon.png",
      "48": "icon.png",
      "128": "icon.png"
    }
  },
  "permissions": []
}
```

### 2. popup.html

```html
<!DOCTYPE html>
<html>
<head>
  <title>Popup</title>
  <style>
    body {
      width: 200px;
      font-family: Arial, sans-serif;
    }
    h1 {
      font-size: 20px;
      text-align: center;
    }
  </style>
</head>
<body>
  <h1>Hello, World!</h1>
  <script src="popup.js"></script>
</body>
</html>
```

### 3. popup.js

```javascript
document.addEventListener('DOMContentLoaded', function() {
  console.log('Hello, World!');
});
```

### 4. icon.png
你需要提供一个图标图片，命名为 `icon.png`，并放在与 `manifest.json` 同一个文件夹内。你可以随便使用一个16x16, 48x48, 128x128像素的 PNG 图片。

### 步骤

1. 打开 Chrome 浏览器，输入 `chrome://extensions/` 并回车。
2. 打开右上角的 "开发者模式" 开关。
3. 点击 "加载已解压的扩展程序" 按钮，选择你的插件文件夹 `my-simple-chrome-extension`。
4. 你应该会在扩展程序列表中看到你的插件 "My Simple Chrome Extension"。
5. 点击浏览器右上角插件图标，你会看到一个带有 "Hello, World!" 的弹出窗口。

这个插件展示了最基本的 Chrome 扩展的结构和功能。你可以根据需要进一步扩展功能和界面。

### 在DallE生成icon.png
```
请生成一个icon.png，要求 128x128像素
```
