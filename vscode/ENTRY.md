# 入口文件

## vscode入口文件

```
out/main.js
//该文件会调用out/vs/code/electron-main/main.js
```

```
out/vs/code/electron-main/main.js
//该文件的（259行）main方法中回去打开我们的客户端窗口



const context = !!process.env['VSCODE_CLI'] ? OpenContext.CLI : OpenContext.DESKTOP;
if (environmentService.args['new-window'] && environmentService.args._.length === 0) {
    windowsMainService.open({ context, cli: environmentService.args, forceNewWindow: true, forceEmpty: true, initialStartup: true }); // new window if "-n" was used without paths
} else if (global.macOpenFiles && global.macOpenFiles.length && (!environmentService.args._ || !environmentService.args._.length)) {
    windowsMainService.open({ context: OpenContext.DOCK, cli: environmentService.args, pathsToOpen: global.macOpenFiles, initialStartup: true }); // mac: open-file event received on startup
} else {
    windowsMainService.open({ context, cli: environmentService.args, forceNewWindow: environmentService.args['new-window'] || (!environmentService.args._.length && environmentService.args['unity-launch']), diffMode: environmentService.args.diff, initialStartup: true }); // default: read paths from cli
}
```

## 客户端html

```
out/vs/workbench/electron-browser/bootstrap/index.html
```

## 客户端入口js

```
out/vs/workbench/electron-browser/bootstrap/index.js
```

## 客户端UI主文件

```
out/vs/workbench/electron-browser/workbench.ts
```



