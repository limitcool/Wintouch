# Wintouch

未对文件`touch.ps1` 进行数字签名。无法在当前
系统上运行该脚本。有关运行脚本和设置执行策略的详细信息，请参阅 https:/go.microsoft.com/fwlink/?LinkID=135170 中的 about
_Execution_Policies。

```powershell
// 管理员权限下
set-executionpolicy Bypass
```

打开`powershell`，用管理员身份

```powershell
// 查看执行策略
get-ExecutionPolicy
// 修改执行策略
set-ExecutionPolicy RemoteSigned
```


收到的回复内容解释如下：微软官网

WINDOWS POWERSHELL 执行策略
默认执行策略为“Restricted”。

① RESTRICTED

- 允许单独的命令，但不会运行脚本。

② ALLSIGNED

- 脚本可以运行，对脚本安全、数字签名没有要求，存在安全风险

③ REMOTESIGNED

- 脚本可以运行，但对可以运行的脚本有要求：

- Ⅰ从 Internet 下载的脚本和配置文件（包括电子邮件和即时消息程序），具有受信任的发布者的数字签名。

- Ⅱ 在本地计算机上编写的脚本，可以没有数字签名。
