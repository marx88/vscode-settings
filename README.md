# vscode-settings
导出的VSCode配置


### 快捷键
- `ctrl + shift + p`：打开命令行面板
- `ctrl + k` + `v`：右侧打开markdown预览


### Tip
- 快速重启vscode：`ctrl + shift + p`中选择`reload window`，选中即可


### 配置项
按`ctrl + ,`打开设置，点击右上角`打开设置(json)`，在打开的文件里输入：

#### 普通配置项
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
    "editor.suggest.snippetsPreventQuickSuggestions": false,
    "workbench.startupEditor": "newUntitledFile",
    "go.formatTool": "goimports"
}
```

#### 扩展GO配置项
```
"go.formatTool": "goimports"
```


### 插件列表
- Chinese (Simplified) Language Pack for Visual Studio Code：汉化包。`ctrl + shift + p`中选择`display language`后，选择显示的语言。
- Google Translate：翻译工具。[下载](https://github.com/marx88/vsc-google-translate/releases)后，在`vscode`的扩展界面，点击右上角`...`，选择`从VSIX安装`。
- Go：`vscode`集成`Golang`的开发工具。`ctrl + shift + p`中选择`install/update tool`后，安装这些tool：goimports,golangci-lint,dlv,godef,go-outline,gopkgs,gocode-gomod,golint,gocode。
- Git History：查看git日志，文件历史。
- GitLens：文件比较。
