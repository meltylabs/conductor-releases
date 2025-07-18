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
