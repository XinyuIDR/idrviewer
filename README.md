# IDRViewer - BuildVu 的 网页文档查看器

### ✨原代码仓在[这里](https://github.com/idrsolutions/idrviewer)

IDRViewer 是一个纯 HTML/JavaScript/CSS 查看器，旨在浏览器中显示 PDF 和 Office 文档。它与 [BuildVu](https://www.idrsolutions.com/buildvu/) 配合使用，后者将 PDF 文档转换为 HTML5 或 SVG 页面。

IDRViewer 是负责在网页浏览器中加载和显示页面的组件。它还处理如缩放、页面布局和选择模式等功能。

## UI 模板
我们还提供了多个用户界面模板，可以按原样使用或作为构建自定义用户界面的起点。模板是使用 webpack 构建的（请参见 NPM 任务部分）。

- 完整 UI（[源代码](src/templates/complete/)，[演示](https://files.idrsolutions.com/Examples/IDRViewerUI/complete/)）
- 简洁 UI（[源代码](src/templates/clean/)，[演示](https://files.idrsolutions.com/Examples/IDRViewerUI/clean/)）
- 简单 UI（[源代码](src/templates/simple/)，[演示](https://files.idrsolutions.com/Examples/IDRViewerUI/simple/)）
- 幻灯片 UI（[源代码](src/templates/slideshow/)，[演示](https://files.idrsolutions.com/Examples/IDRViewerUI/slideshow/)）

## 项目结构
```
examples/      - 已构建的 UI 模板（完整、简洁、简单、幻灯片）
src/
   css/        - 页面显示的 CSS，布局（连续、杂志、演示）和过渡效果
   js/         - 主要代码库（idrviewer.js）及其他实用工具（注释、搜索等）
   templates/  - 使用 webpack 编译成单个 index.html 文件的 UI 模板
   test/
      document/   - 用于测试的文档
      js/         - Playwright 测试
```

## 外部 IDRViewer API
请参见 [IDRViewer JavaScript API](https://support.idrsolutions.com/buildvu/api-documents/idrviewer-javascript-api)。

## 注释 JSON API
请参见 [Annotations JSON API](https://support.idrsolutions.com/buildvu/api-documents/annotations-json-api)。

## NPM 任务
1. 安装 [node.js](https://nodejs.org/)
2. 打开终端/命令提示符并进入 idrviewer 目录
3. 运行 `npm install`
4. 运行任务时，执行 `npm run <taskname>`，其中 `<taskname>` 为以下之一：
   - 'jshint' 用于对 JavaScript 文件进行静态分析。
   - 'playwright' 用于运行自动化的 IDRViewer 测试（位于 /src/test/ 目录下）
   - 'test' 同时运行 jshint 和 playwright 测试
   - 'webpack' 用于构建 UI
   - 'webpack-watch' 用于构建 UI 并监听更改

## 许可证

版权 2025 IDRsolutions

根据 Apache 许可证 2.0 版（“许可证”）授权；
除非遵守该许可证，否则不得使用此文件。
你可以在以下网址获取许可证副本：

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

除非适用法律要求或书面同意，否则根据该许可证分发的软件是按“原样”提供的，不附带任何形式的保证或条件，无论是明示的还是隐含的。
详细信息请参见许可证，了解有关权限和限制的具体规定。
