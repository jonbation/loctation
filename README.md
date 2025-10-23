# Loctation

Loctation removed launchpad,and it's so hard to use, it's doesn't use your Bio GPU, please apple, at least give people an option to switch back. Before that, here is LaunchNext

*Huge thanks to the original project! I hope this enhanced version can be merged back to the original repository*

*LaunchNow has chosen the GPL 3 license. LaunchNext follows the same licensing terms.*

⚠️ **If macOS blocks the app, run this in Terminal:**
```bash
sudo xattr -r -d com.apple.quarantine /Applications/LaunchNext.app
```
**Why**: I can't afford Apple's developer certificate ($99/year), so macOS blocks unsigned apps. This command removes the quarantine flag to let it run. **Only use this command on apps you trust.**

### What LaunchNext Delivers
- ✅ **One-click import from old system Launchpad** - directly reads your native Launchpad SQLite database (`/private$(getconf DARWIN_USER_DIR)com.apple.dock.launchpad/db/db`) to perfectly recreate your existing folders, app positions, and layout
- ✅ **Classic Launchpad experience** - works exactly like the beloved original interface
- ✅ **Multi-language support** - full internationalization with English, Chinese, Japanese, French, Spanish, German, and Russian
- ✅ **Hide icon labels** - clean, minimalist view when you don't need app names

### Data Storage
Application data is safely stored in:
```
~/Library/Application Support/LaunchNext/Data.store
```

### Native Launchpad Integration
Reads directly from the system Launchpad database:
```bash
/private$(getconf DARWIN_USER_DIR)com.apple.dock.launchpad/db/db
```

## Installation

### Requirements
- macOS 26 (Tahoe) or later
- Apple Silicon or Intel processor
- Xcode 26 (for building from source)

### Build from Source

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/LaunchNext.git
   cd LaunchNext
   ```

2. **Open in Xcode**
   ```bash
   open LaunchNext.xcodeproj
   ```

3. **Build and run**
   - Select your target device
   - Press `⌘+R` to build and run
   - Or `⌘+B` to build onl

### Command Line Build

**Regular Build:**
```bash
xcodebuild -project LaunchNext.xcodeproj -scheme LaunchNext -configuration Release
```

**Universal Binary Build (Intel + Apple Silicon):**
```bash
xcodebuild -project LaunchNext.xcodeproj -scheme LaunchNext -configuration Release ARCHS="arm64 x86_64" ONLY_ACTIVE_ARCH=NO clean build
```

## Usage

### Getting Started
1. **First Launch**: LaunchNext automatically scans all installed applications
2. **Select**: Click to select apps, double-click to launch
3. **Search**: Type to instantly filter applications
4. **Organize**: Drag apps to create folders and custom layouts

### Import Your Launchpad
1. Open Settings (gear icon)
2. Click **"Import Launchpad"**
3. Your existing layout and folders are automatically imported


### Display Modes
- **Windowed**: Floating window with rounded corners
- **Fullscreen**: Full-screen mode for maximum visibility
- Switch modes in Settings
