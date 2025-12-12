[--------------------------------------PE---------------------------------------]

WinNTsetup:
最新原版ISO
调整优化项

删除Windows Defender:
C:\Program Files\Windows Defender
C:\Program Files\Windows Defender Advanced Threat Protection
C:\Program Files (x86)\Windows Defender
C:\ProgramData\Microsoft\Windows Defender
C:\ProgramData\Microsoft\Windows Defender Advanced Threat Protection
C:\ProgramData\Microsoft\Windows Security Health

Dsim++:
关闭服务
sysmain
windows search
Diagnostic Policy Service
删除多余appx
调整系统优化部分

[------------------------------------系统-----------------------------------------]

删除Windows Defender残留:
HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Run
-SecurityHealthSystray.exe
-MDCoreSvc
-WinDefend
DefenderRemover选S

关遥测
设置
「隐私和安全性」>「诊断和反馈」，关闭「发送可选诊断数据」和「量身订制的体验」
「隐私和安全性」>「语音」，选择「停止提供我的语音剪辑」
「隐私和安全性」>「常规」，关闭所有
任务计划程序
「任务计划程序库」>「Microsoft」>「Windows」>「Customer Experience Improvement Program」禁用所有
组策略
「计算机配置」>「管理模板」>「Windows 组件」>「数据收集和预览版本」>「允许诊断数据」启用诊断数据关闭
注册表
HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\DataCollection\AllowTelemetry 0
服务
Connected User Experiences and Telemetry
Diagnostic Data Service
Microsoft Compatibility Telemetry

打开流量计费的网络

关闭Auto Discovery:
Set-ItemProperty 'HKCU:\Software\Classes\Local Settings\Software\Microsoft\Windows\Shell\Bags\AllFolders\Shell' -Name FolderType -Value NotSpecified -Type String -Force

关闭网络搜索:
Set-ItemProperty -Path "HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Search" -Name "BingSearchEnabled" -Value 0 -Type DWord

隐藏图库和主文件夹:
HKEY_CLASSES_ROOT\CLSID\{e88865ea-0e1c-4e20-9aa6-edcd0212c87c}
HKEY_CLASSES_ROOT\CLSID\{f874310e-b6b7-47dc-bc84-b9e6b38f5903}
System.IsPinnedToNameSpaceTree	0

Win32优先级调整
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\PriorityControl
数值	 CPU时间		 前台：后台

42(2A)   短-固定 	  3    1
38(26)   短-可变
26(1A)   长-固定
22(16)   长-可变

41(29)   短-固定 	  2    1
37(25)   短-可变
25(19)   长-固定
21(15)   长-可变

40(28)   短-固定 	  1    1
36(24)   短-可变
24(18)   长-固定
20(14)   长-可变

默认 程序38  后台24

调整电源选项
控制面板 平衡
设置 高性能

[--------------------------------------AMD显卡--------------------------------]

AMD显卡预渲染帧数:
HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Class\{4d36e968-e325-11ce-bfc1-08002be10318}\0001\UMD
Main3D_DEF	0

freesync注册表:
HKLM\SYSTEM\CurrentControlSet\Control\Class\{4d36e968-e325-11ce-bfc1-08002be10318}\0001
-DalSupportExternalPanelDrr
-DalProtectionControlDefault

[-------------------------------------Firefox--------------------------------]

security.insecure_field_warning.contextual.enabled = false
security.certerrors.permanentOverride = false
network.stricttransportsecurity.preloadlist = false
security.enterprise_roots.enabled = true
browser.download.skipConfirmLaunchExecutable = true

[-------------------------------------BoosterX--------------------------------]

关闭应用商店自动更新

[-----------------------------ContextMenuManager------------------------------]

调整不需要的右键菜单

[-------------------------------------DDU-------------------------------------]

关闭自动安装驱动

[-------------------------------------其他------------------------------------]

ExplorerPatcher
