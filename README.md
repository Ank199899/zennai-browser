# Zennai Browser

A professional Chromium-based browser.

## Building for Windows

### Prerequisites (on your Windows PC)
- Windows 10/11 (64-bit)
- Visual Studio 2022 with "Desktop development with C++" workload
- Git for Windows
- 16 GB RAM minimum (32 GB recommended)
- 150 GB free disk space

### Step 1 - Install depot_tools
```powershell
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git C:\depot_tools
# Add C:\depot_tools to your PATH (System Environment Variables)
```

### Step 2 - Get Chromium source
```cmd
mkdir C:\zennai-build
cd C:\zennai-build
gclient config https://chromium.googlesource.com/chromium/src.git
gclient sync --no-history
```

### Step 3 - Setup GitHub Actions self-hosted runner
1. Go to: `https://github.com/YOUR_USERNAME/zennai-browser/settings/actions/runners`
2. Click **New self-hosted runner** → Windows → x64
3. Follow the commands shown on screen to register your PC

### Step 4 - Trigger a build
```
git tag v1.0.0
git push origin v1.0.0
```
The .exe will appear automatically in GitHub Releases.

## Branding
All branding files are in the `branding/` folder.
Custom strings are in `strings/`.
