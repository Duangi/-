# VSCforUnity

## unity中设置默认编辑器

> Edit-Preferences-External Tools-External Scripts Editor
>
> 下拉框中选择Visual Studio Code
>
> 如果没有，则手动选择exe，我的路径在D:\Tools\Microsoft VS Code\Code.exe

## vsc中下载插件

1. C#
2. Debugger for Unity

## .NET core下载

- vsc可能会报找不到.NET core的错

下载地址 https://dotnet.microsoft.com/download

> 下载Core SDK，傻瓜式安装



- 安装完成.NET core之后，又显示找不到.NETFramework,Version = v4.7.1的错

登录这个报错信息给的网址，发现之前用visual studio编辑脚本时，是会自带Framework的，而我刚刚为了不用笨重的vs，一气之下给卸了，所以电脑里面缺了这个环境。

安装链接：

https://www.microsoft.com/net/download/visual-studio-sdks

> 选择相应的版本，安装devlopor Pack版本，我安装的是4.7.1



- 安装完成Framework之后，vsc仍会提示找不到.net core

此时的编辑器其实已经可以自动补全代码了。

> 手动关闭提示：打开vsc-File-Preferences-settings

> 搜索框中搜索dotnet

> Suppress Dotnet Install Warning一栏，勾选上

