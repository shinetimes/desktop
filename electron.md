##桌面框架 Electron
[electron](https://github.com/atom/electron) 使用 web 页面作为它的 GUI   
[awesome](https://github.com/sindresorhus/awesome-electron) 资源清单  
[packager](https://github.com/electron-userland/electron-packager) 打包工具    
[quick-start](https://github.com/atom/electron-quick-start) 快速启步   
[开发文档](https://github.com/electron/electron/tree/master/docs-translations/zh-CN)


```
// 全局安装
npm install electron-prebuilt -g
npm install electron-packager -g

// 本地安装
npm install electron-prebuilt --dev-save
npm install electron-packager --dev-save
```

##主进程
在 Electron 里，运行 package.json 里 main 脚本的进程被称为主进程。在主进程运行的脚本可以以创建 web 页面的形式展示 GUI

##渲染进程
由于 Electron 使用 Chromium 来展示页面，所以 Chromium 的多进程结构也被充分利用。每个 Electron 的页面都在运行着自己的进程，这样的进程我们称之为渲染进程

##主进程与渲染进程的区别

主进程使用 BrowserWindow 实例创建网页。每个 BrowserWindow 实例都在自己的渲染进程里运行着一个网页。当一个 BrowserWindow 实例被销毁后，相应的渲染进程也会被终止

主进程管理所有页面和与之对应的渲染进程。每个渲染进程都是相互独立的，并且只关心他们自己的网页

由于在网页里管理原生 GUI 资源是非常危险而且容易造成资源泄露，所以在网页面调用 GUI 相关的 APIs 是不被允许的。如果你想在网页里使用 GUI 操作，其对应的渲染进程必须与主进程进行通讯，请求主进程进行相关的 GUI 操作

在 Electron，我们提供用于在主进程与渲染进程之间通讯的 ipc 模块。并且也有一个远程进程调用风格的通讯模块 remote

