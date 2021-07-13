# vscode-settings
导出的VSCode配置


### 快捷键
- `ctrl + shift + p`：打开命令行面板
- `ctrl + k` + `v`：右侧打开markdown预览


### Tip
- 快速重启vscode：`ctrl + shift + p`中选择`reload window`，选中即可


### 配置项
按`ctrl + ,`打开设置，点击右上角`打开设置(json)`，在打开的文件里输入：

```
{
    // 通用配置
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
    "editor.detectIndentation": false,
    "editor.renderControlCharacters": true,
    "editor.renderWhitespace": "all",
    "editor.tabSize": 4,
    "editor.insertSpaces": true,
    "editor.rulers": [80, 100],
    "workbench.startupEditor": "newUntitledFile",
    "window.zoomLevel": 0,
    "diffEditor.ignoreTrimWhitespace": false,
    "search.useIgnoreFiles": false,
    // YAML文件配置
    "[yaml]": {
        "editor.insertSpaces": true,
        "editor.tabSize": 4,
        "editor.autoIndent": "advanced"
    },
    // GO配置
    "go.formatTool": "goimports",
    "go.useLanguageServer": true,
    "[go]": {
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": true
        }
    },
    "gopls": {
        "usePlaceholders": true
    },
    // PHP配置
    "[php]": {
        "editor.formatOnSave": false,
        "editor.defaultFormatter": "junstyle.php-cs-fixer"
    },
    "php-cs-fixer.rules": "@PhpCsFixer",
    "php-cs-fixer.executablePath": "${extensionPath}/php-cs-fixer.phar",
    "php-cs-fixer.lastDownload": 1626137882631,
    // WEB配置
    "prettier.printWidth": 120, // 配合根目录.prettierrc.yaml一起用
    "[html]": {
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
        "editor.defaultFormatter": "esbenp.prettier-vscode",
    },
    "[javascript]": {
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
        "editor.defaultFormatter": "esbenp.prettier-vscode",
    },
    "[css]": {
        "editor.tabSize": 2,
        "editor.formatOnSave": false,
        "editor.defaultFormatter": "esbenp.prettier-vscode",
    },
    "[vue]": {
        "editor.defaultFormatter": "octref.vetur"
    },
    // vue的html格式化
    "vetur.format.defaultFormatter.html": "js-beautify-html",
    "vetur.format.defaultFormatterOptions": {
        "js-beautify-html": {
          "wrap_attributes": "force-expand-multiline"
        },
    },
}
```


### 插件列表
- Chinese (Simplified) Language Pack for Visual Studio Code：汉化包。`ctrl + shift + p`中选择`display language`后，选择显示的语言。
- Google Translate：翻译工具。[下载](https://github.com/marx88/vsc-google-translate/releases)后，在`vscode`的扩展界面，点击右上角`...`，选择`从VSIX安装`。
- Go：`vscode`集成`Golang`的开发工具。`ctrl + shift + p`中选择`install/update tool`后，安装这些tool：goimports,golangci-lint,dlv,godef,go-outline,gopkgs,gocode-gomod,golint,gocode,guru。
- PHP DocBlocker：代码注释用。
- ~~PHP Intellisense：代码提示啊等等。~~
- PHP Intelephense：上面的插件`use`时不提示`composer`里的库...
- ~~phpfmt PHP formatter：简单的代码格式化。有了php-cs-fixer插件就不用这个了。~~
- PHP CS Fixer：格式化代码，很好很强大。
- PHP Debug：代码调试用。前置操作包括，1、安装XDebug，按照插件提供的说明安装；2、`vscode`的`launch.json`里面的端口也写成9001；3、配置ini,扩展地址`zend_extension = 下载的xdebug名.dll`及xdebug配置：
```
[XDebug]
xdebug.mode=debug
xdebug.start_with_request=yes
;9001是避免与nginx的9000端口冲突
xdebug.client_port="9001"
```
- SFTP：ftp。
- Code Runner：右键或者`ctrl + alt + n`运行代码文件。
- Todo Tree：TODO高亮、TODO侧边栏
- EditorConfig for Visual Studio Code：让vscode支持`.editorconfig`文件
- Vetur：支持`.vue`文件
- vscode-proto3：支持`.proto`文件
- Prettier - Code formatter：格式化`js`、`css`、`html`代码
- DotENV：高亮`.env`文件
- TWIG：`vscode-twig`,高亮`.twig`文件
- Git History：查看GIT提交历史记录

