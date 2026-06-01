# Intune Autopilot Setup Process (Shift + F10)

## 1. Network Setup (Ethernet)

Plug in Ethernet cable during OOBE.

WinPE detects network adapter  
- DHCP assigns IP address  
- DNS is configured  
- Internet becomes available  

---

## 2. Open Command Prompt

```cmd
SHIFT + F10
```

Opens:
```cmd
X:\Sources>
```

---

## 3. Start PowerShell

```cmd
powershell.exe
```
Switches to PowerShell environment.

---

## 4. Enable Script Execution
```cmd
Set-ExecutionPolicy RemoteSigned -Scope Process -Force
```
Allows scripts to run in current session only.

---

## 5. Install Autopilot Tool
```cmd
Install-Script -Name Get-WindowsAutopilotInfo -Force
```
Downloads Microsoft tool used to capture device identity.

---

## 6. Upload Device to Intune
```cmd
Get-WindowsAutopilotInfo -Online
```
- Collects hardware hash
- Sends device to Intune Autopilot
- Registers device for zero-touch deployment

---

## 7. Completion

Sign-in screen will appear for a Microsoft Entra ID (Azure AD) admin account.

Admin must:
- Authenticate with the tenant admin credentials
- Verify the device in Microsoft cloud
- Complete enrollment into Intune Autopilot

Once completed:
- Device is registered in Intune
- Linked to Autopilot profile
- Ready for automated provisioning on next boot