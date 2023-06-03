# Windows Bootloader

## Native monitor resolution during boot

On most Installations of Windows the boot logo and animation are distorted due to the Windows bootloader stretching a low resolution image to your monitor's native resolution. In order to resolve
this issue, you need to fire up either a command prompt or a powershell and set your monitors highest resolution.

Run Windows Command (cmd.exe) with administrator rights (`CTRL+SHIFT+ENTER`):

```cmd
bcdedit /set {globalsettings} highestmode on
```

For Windows Powershell it is slightly different:

```powershell
bcdedit /set "{globalsettings}" highestmode on
```
