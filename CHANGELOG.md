# Miscallenous Improvements 
_0.0.19_ 
July 21st, 2025 

Improvements: 

- Unread indicators in the sidebar and Mac Dock now show one notification per workspace to reduce noise
- Added zoom keyboard shortcuts (`⌘+` to zoom in, `⌘-` to zoom out, `⌘0` to reset zoom)
- Added a button in the sidebar to access the dashboard

Fixes: 

- Improved the performance of `@` file mentions in large codebases
- Fixed an issue where the `Compact conversation` button wouldn’t show up when the a workspace reached 100% context
- Fixed a bug where long branch names would hide the “Archive workspace” button
- Fixed a bug where trackpads were unable to scroll the repository list in the “Add repository” dialog
- Fixed a bug where compacting a conversation would show a loading state in all workspaces
- The feedback dialog now submits on `cmd+enter` instead of `enter`

Misc: 

- Cleaned up presentation of the “Add repository” dialog

# GitHub Integration
_0.0.17_ - _0.0.18_
July 19th, 2025

Conductor now integrates with your GitHub account. Start working on issues in one click, and easily add your private repositories.

<img width="1638" height="1036" alt="CleanShot 2025-07-19 at 09 42 50@2x" src="https://github.com/user-attachments/assets/1541d4ee-8efb-4050-9412-d7d10632b94e" />

<img width="1216" height="860" alt="CleanShot 2025-07-19 at 09 50 26@2x" src="https://github.com/user-attachments/assets/79ec33e1-ce33-4196-885e-e5e016db0949" />

Improvements: 

- Integrate with GitHub
- Refreshed design of the left sidebar 
- Terminal processes now use your native shell instead of forcing zsh
- `Ctrl+D` now force restarts the current terminal process 
- Added a button to provide feedback in-app 
- ⌘N to start a new workspace in your current repository
- Sleeker home page animation
- Added system theme

Fixes:

- Fixed the highlight color in the terminal
- Fixed the right panel closing when dismissing the settings dialog

# Terminal Improvements 
_0.0.16_  
July 18th, 2025 

We've upgraded the terminal in Conductor! 

<img width="1134" height="850" alt="CleanShot 2025-07-18 at 10 27 06@2x" src="https://github.com/user-attachments/assets/7ee30008-24d3-4b54-9567-812ff995cdab" /> 

Sessions now persist when navigating between workspaces; we also squashed several terminal bugs. 

Fixes:

- Fixed default padding in dialogs
- Fixed a bug where the composer would cover more text than necessary 
- Fixed a bug where workspaces wouldn't be reset to `idle` state on app restart
- Fixed a bug where certain workspaces wouldn't load due to an infinite rendering loop 
