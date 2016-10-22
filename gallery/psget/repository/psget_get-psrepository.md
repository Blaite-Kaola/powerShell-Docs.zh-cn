# Get-PSRepository

获取计算机上的已注册存储库。

## 说明

Get-PSRepository cmdlet 获取计算机上为当前用户注册的 PowerShell 模块存储库。

对于每个已注册存储库，Get-PSRepository 将返回 PSRepository 对象，可根据需要将其通过管道传递到 Unregister-PSRepository 以注销已注册的存储库。

## Cmdlet 语法
```powershell
Get-Command -Name Get-PSRepository -Module PowerShellGet -Syntax
```

## Cmdlet 联机帮助参考

[Get-PSRepository](http://go.microsoft.com/fwlink/?LinkID=517127)

## 示例命令

```powershell

# Properties of Get-PSRepository returned object
Get-PSRepository PSGallery | Format-List * -Force

Name                      : PSGallery
SourceLocation            : https://www.powershellgallery.com/api/v2/
Trusted                   : False
Registered                : True
InstallationPolicy        : Untrusted
PackageManagementProvider : NuGet
PublishLocation           : https://www.powershellgallery.com/api/v2/package/
ScriptSourceLocation      : https://www.powershellgallery.com/api/v2/items/psscript/
ScriptPublishLocation     : https://www.powershellgallery.com/api/v2/package/
ProviderOptions           : {}

# Get all registered repositories
Get-PSRepository

# Get a specific registered repository
Get-PSRepository PSGallery

Name                      InstallationPolicy   SourceLocation
----                      ------------------   --------------
PSGallery                 Untrusted            https://www.powershellgallery.com/api/v2/

# Get registered repository with wildcards
Get-PSRepository *Gallery*

```

<!--HONumber=Aug16_HO3-->

