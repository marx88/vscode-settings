# vscode-settings
导出的VSCode配置

### 快捷键
- `ctrl + shift + p`：打开命令行面板

### Tip
- 快速重启vscode：`ctrl + shift + p`中选择`reload window`，选中即可

### 配置项
按`ctrl + ,`打开设置，点击右上角`打开设置(json)`，在打开的文件里输入：
```
{
    "files.exclude": {
        "**/.idea": true
    },
    "files.watcherExclude": {
        "**/vendor/*/**": true
    },
    "workbench.tree.indent": 18,
    "workbench.tree.renderIndentGuides": "always",
    "telemetry.enableCrashReporter": false,
    "telemetry.enableTelemetry": false,
    "files.eol": "\n",
    "files.insertFinalNewline": true,
    "editor.suggest.snippetsPreventQuickSuggestions": false
}
```

### 插件列表
- Chinese (Simplified) Language Pack for Visual Studio Code：汉化包。`ctrl + shift + p`中选择`display language`后，选择显示的语言。
- Google Translate：翻译工具。[下载](https://github.com/marx88/vsc-google-translate/releases)后，在`vscode`的扩展界面，点击右上角`...`，选择`从VSIX安装`。
