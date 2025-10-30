# Automating Browser Cache Clear with Task Scheduler + Script

---

## 🧩 Scenario
A shared classroom PC was filling up with browser junk over time. Students reported sluggish performance and odd login issues (old sessions, cached redirects). Staff wanted a lightweight way to automatically clear browser caches so each logon felt “fresh” without manual maintenance.

---

## 🔍 Problem
Manually clearing caches is inconsistent on shared machines, and users often forget. We needed:
- A **reliable, automatic** cleanup at **logon** (and optionally at **startup**).
- A solution that works across **Chrome**, **Microsoft Edge (Chromium)**, and **Firefox**.
- Minimal disruption (no breaking profiles, no elevated prompts for normal users).

---

## 🛠️ Steps Taken

### 1) Decide on Script Type
I created two versions so the environment could choose:
- **PowerShell** (preferred for readability and control)
- **Batch (.cmd)** (for older setups)

> Note: These scripts target cache directories only, not the whole profile.

---

### 2) PowerShell Script (recommended)
Save as: `Clear-BrowserCache.ps1`

```powershell
# Clear-BrowserCache.ps1
# Run in user context at Logon (Task Scheduler). No admin required for user-level cache paths.

$ErrorActionPreference = "SilentlyContinue"

function Clear-Folder($path) {
    if (Test-Path $path) {
        Get-ChildItem -Path $path -Recurse -Force | Remove-Item -Recurse -Force -ErrorAction SilentlyContinue
    }
}

# Chrome
$chromeCache     = Join-Path $env:LOCALAPPDATA "Google\Chrome\User Data\Default\Cache"
$chromeCodeCache = Join-Path $env:LOCALAPPDATA "Google\Chrome\User Data\Default\Code Cache"
$chromeGPUCache  = Join-Path $env:LOCALAPPDATA "Google\Chrome\User Data\Default\GPUCache"
Clear-Folder $chromeCache
Clear-Folder $chromeCodeCache
Clear-Folder $chromeGPUCache

# Edge
$edgeCache     = Join-Path $env:LOCALAPPDATA "Microsoft\Edge\User Data\Default\Cache"
$edgeCodeCache = Join-Path $env:LOCALAPPDATA "Microsoft\Edge\User Data\Default\Code Cache"
$edgeGPUCache  = Join-Path $env:LOCALAPPDATA "Microsoft\Edge\User Data\Default\GPUCache"
Clear-Folder $edgeCache
Clear-Folder $edgeCodeCache
Clear-Folder $edgeGPUCache

# Firefox
$ffProfilesPath = Join-Path $env:APPDATA "Mozilla\Firefox\Profiles"
if (Test-Path $ffProfilesPath) {
    Get-ChildItem $ffProfilesPath -Directory | ForEach-Object {
        $ffCache = Join-Path $_.FullName "cache2"
        Clear-Folder $ffCache
    }
}

# Optional: legacy IE/Edge cleanup
# rundll32.exe InetCpl.cpl,ClearMyTracksByProcess 255
