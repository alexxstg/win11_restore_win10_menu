The default Windows 11 right-click context menu is (in my opinion) awful and was an unnecessary change.

## Switching back to Windows 10 Context Menu

If you're on Windows 11 and want the old Windows 10 right-click context menu, run the following command in a regular command prompt (NOT administrative):

```cmd
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```

Then restart `explorer.exe` or reboot

---

## Switching back to Windows 11 Context Menu

To undo this change and revert back to the default Windows 11 right-click context menu, run this (again in a regular command prompt, NOT administrative):

```cmd
reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f
```

Then restart `explorer.exe` or reboot

(Source: https://answers.microsoft.com/en-us/windows/forum/all/restore-old-right-click-context-menu-in-windows-11/a62e797c-eaf3-411b-aeec-e460e6e5a82a)
