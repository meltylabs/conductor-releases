## Performance Improvements
_0.14.3_ 
Oct 8th, 2025 

We’ve fixed a regression that could leave zombie `claude` processes on user systems. 

Improvements 

- Updated right sidebar empty state
- Better error handling for the Anthropic Consumer Terms and Privacy Policy October 8th deadline error 

Fixes 

- Fixed MCP documentation link

We’ve also temporarily removed plan mode from Conductor due to bugs in the Anthropic Agent SDK. For now, we’re getting good results by asking Sonnet 4.5 to make a plan.

# New Diff Viewer 
_0.14.1_ - _0.14.2_
Oct. 7th, 2025 

We've revamped the diff UI! 

<img width="2048" height="1319" alt="image" src="https://github.com/user-attachments/assets/237c299b-87e3-4631-bd85-aa671a623827" /> 

We’ve also fixed a performance degradation associated with having many workspaces. Conductor should be much faster now! 

Improvements 

- New sound effects on workspace completion
- Added an `escape` shortcut to cancel git diff comments
- Converted the repository details page to a simpler dialog
- Added UI treatment for `/login` errors
- Show full branch name on hover in workspace sidebar

Fixes 

- Disabled font ligatures in git diffs
- Fixed binary file detection for untracked files
- Fixed line detection for untracked files
- Fixed a bug where comments and line numbers could become misaligned in the git diff
- Added drag regions to the git diff sheet
- Fixed input not resetting on linear search palette close

New in 0.14.2:

- Performance improvements
- Option to set AWS_PROFILE


# One Click Revert, Faster Diffs
_0.14.0_
Oct 3rd, 2025

<img width="712" height="246" alt="CleanShot 2025-10-03 at 10 49 27@2x" src="https://github.com/user-attachments/assets/40495a22-54e2-4d81-b570-de1345c967e6" />

You can now revert Claude’s changes in one click! Claude will be notified that you made a change so you don’t have to explain yourself.

We’ve also changed the sidebar ordering. Workspaces are now ordered by last user message sent, so you can see the most recent chats at the top.

<img width="460" height="720" alt="image" src="https://github.com/user-attachments/assets/9b23ae17-8ff5-4cf0-a74e-d93dd89487c1" />

We’ve made the diff viewer faster, and now show structural in-line diffs.

<img width="394" height="226" alt="image" src="https://github.com/user-attachments/assets/50580d50-d8c9-42d1-bdfb-9410b763ffdf" />

Also, we added a new “refresh” button for when changes occur while the diff viewer is open.

<img width="948" height="440" alt="image" src="https://github.com/user-attachments/assets/0bf82ede-bd44-4a18-aacf-98dbcb03cea0" />


Fixes

- Faster syntax highlighting in diff viewer
- Large files will no longer slow down the diff viewer
- Structural diffs are now highlighted in the diff viewer
- Text selections now render properly in the diff viewer
- Moved files will now render properly in the diff viewer
- Improved conductor.json Claude prompt

# Fixes for Fish Users
_0.13.8_
Oct 1st, 2025

- We now always use zsh for internal shell commands so you can continue to use Conductor with fish
- Increased `gh` CLI auth timeout and potential bug with authentication. If Conductor is not recognizing your `gh` login, please let us know at humans@conductor.build!


# Run on Bedrock, Vertex, or custom provider
_0.13.6_-_0.13.7_
Sept 30th, 2025

<img width="1644" height="1454" alt="image" src="https://github.com/user-attachments/assets/d9888c2a-1849-4dc1-8ddb-0d9ef8c1e3f0" />

You can now setup Claude Code to run via an alternate provider, like Bedrock, Vertex, or any Anthropic compatible URL. 

Fixes

- More reliable auto-updater
- Fixed width of “Open In” buttons
- Added privacy link to onboarding
- Added some tips on using [Conductor with Cursor/VSCode](https://docs.conductor.build/guides/use-with-cursor).


# RIP _0.13.3_ - _0.13.6_
Don't ask. Our intern went wild.

# Sonnet 4.5 + new workspace page
_0.13.2_
Sept 29th, 2025

<img width="3840" height="2160" alt="image" src="https://github.com/user-attachments/assets/0536fa4e-38b7-4f32-879d-f6d4f7f5d4d5" />

Sonnet 4.5, the best coding model in the world, is now live in Conductor!

Introducing our new workspace page! We’ve made making new workspaces faster and easier to understand.

<img width="2048" height="1567" alt="image" src="https://github.com/user-attachments/assets/44d6a6e6-2619-41c8-9b3e-929c7af99819" />

Name your workspace/branch with the inline editor and see at a glance what happened during workspace setup.

<img width="836" height="254" alt="image" src="https://github.com/user-attachments/assets/29e6baa4-4a7d-45d3-a294-ca2ca2e64db0" />

We’ve also made it more intuitive to link Linear issues. Press ⌘I to link from the composer.

<img width="804" height="338" alt="image" src="https://github.com/user-attachments/assets/ddba9e61-05fb-4581-9c8c-8b77c8fbe1c9" />

Finally, we've made cancellations much more reliable. It should work instantly wherever you are in the chat.

Fixes

- Detect conductor.json in repo root
- Reliable cancellation
- ⌘R to focus run tab



# Improved Plan Mode 
_0.12.1_ 
Sept 27th, 2025 

We’ve improved plan mode! Claude no longer thinks it’s still in plan mode when it’s not. We’ve also updated the controls to respond to Claude’s plans: 

<img width="1268" height="450" alt="image" src="https://github.com/user-attachments/assets/2fedcbfa-dac9-4903-bd87-2766302876c6" /> 

Claude will also no longer forget that its read files across turns. Response times should be faster across chats too. 

Improvements: 

- We now only update the MacOS notification badge when Claude completes
- Improved the `Resolve merge conflicts` button prompt
- Added keyboard shortcut `⌘+⇧+P` to create a PR
- Show the number of pending checks in the git status bar
- Better notifications when scripts fail

Fixes: 

- Fixed a bug sourcing initialization script
- Prevented upstream tracking of new workspace branches
- Fixed compact button height

# Forward Failing Checks to Claude 
_0.12.0_ 
Sept 25th, 2025 

You can now forward your failing CI checks to Claude to fix! 

<img width="866" height="344" alt="image" src="https://github.com/user-attachments/assets/ef5e62cd-3e0e-4af2-9469-a308d38fb1bc" />

You can now search your chats in the command palette (⌘+K):

<img width="2048" height="1218" alt="image" src="https://github.com/user-attachments/assets/dac35e52-f39b-4873-beeb-6fb310190e25" />

**Fish users, rejoice!** We’ve also revamped how we run terminal commands. The terminal will now use your default SHELL and PATH, as well as any terminal commands we run on your behalf (setup scripts, git commands, etc). 

<img width="1830" height="292" alt="image" src="https://github.com/user-attachments/assets/af5e2cf6-1f43-4265-a0c9-87b661987f09" />

# Improved Cancelling 
_0.11.6_ 
Sept 23rd, 2025 

Cancelling is now much more reliable in Conductor! 

Improvements: 

- Improvements to `conductor.json` files generated via Claude Code
- Improved markdown display for agent output
- Added app icons to the “Open” dropdown

Fixes: 

- Fixed slowness when sending attachments in the UI
- Fixed comment whitespace getting trimmed while drafting
- Claude Code now stops when you archive a workspace

# The Return of Big Terminal Mode 
_0.11.4_ - _0.11.5_
Sept 23rd, 2025 

We’ve brought back big terminal mode! Enable it in `Settings` → `Terminal` 

<img width="2048" height="1218" alt="image" src="https://github.com/user-attachments/assets/acf61848-1830-4c82-859f-ecbcda848e79" />

Improvements: 

- Preview what Claude will see when sending comment attachments

Fixes: 

- Removed an unnecessary error toast when closing the “Add a local repo” dialog

In 0.11.5, added debug tools for the conductor.json migration

# New Onboarding 
_0.11.3_ 
Sept 22nd, 2025 

We’ve revamped the onboarding flow in Conductor to make it easier and more beautiful to get started:

<img width="1806" height="1020" alt="image" src="https://github.com/user-attachments/assets/ecd9bac7-0f09-40c1-bf2b-cdb9e14aa81d" />


We’ve made it easier to setup your repo to work well with Conductor. You can now create your setup scripts with Claude:

<img width="1554" height="950" alt="CleanShot 2025-09-22 at 15 43 52@2x" src="https://github.com/user-attachments/assets/52beafc5-6802-45b3-9553-33ffc071a0f2" />

Improvements: 

- Added a `Report Bug` button when Claude Code returns errors
- Linear attachments are now rendered as markdown
- The `Open In` menu no longer defaults to Finder
- A new workspace will be automatically created when a repository is added

Fixes: 

- Retrying an error’ed message will now retry with the failed message’s attachments
- The entire top bar is now draggable

# conductor.json
_0.11.0_ - _0.11.2_
Sept 19th, 2025 

To make it easier to share configurations, Conductor now
stores your setup and run scripts in a `conductor.json` file.

<img width="1387" height="893" alt="image" src="https://github.com/user-attachments/assets/5db0d284-4d32-4cd6-b6fe-583f06ce5805" />

To learn more, [check out our documentation](https://docs.conductor.build/core/scripts). 

If you have any issues migrating, reach out to us at [humans@conductor.build](mailto:humans@conductor.build)! We’re happy to help.

Improvements: 

- New onboarding flow
- Default to terminal if no run script exists
- Added workspace lifecycle logs to the top bar of each workspace

New in 0.11.2:

- Confirm before creating a conductor.json migration PR

  
# Terminal Performance Pt. 2
_0.10.5_ - _0.10.6_
Sept 17th, 2025 

We’ve refactored the terminal. This should reduce crashing and lag, and improve performance for long running tasks. 

Archiving is also now instant:
![ConductorArchive](https://github.com/user-attachments/assets/bef4ffcc-b72e-433a-bc9a-4034c2930821)


Improvements: 

- Simplified signing in with GitHub (we now rely on a local `gh` installation)

Fixes: 

- Fixed `/clear`
- Fixed comments appearing multiple times in certain git diffs
- Fixed appending `.conductor` to `.git/info/exclude`

New in 0.10.6:

- Support for gh login for `bash` shell users

# Terminal Performance
_0.10.3_ 
Sept 11th, 2025 

Terminal now uses WebGL rendering. It should be much snappier.

![TerminalAmp](https://github.com/user-attachments/assets/c3253d2f-55a3-47ca-a9d8-fca8a194e231)


Improvements: 

- Display API key source in top bar
- Render agent output as markdown
- Auto expand files clicked in the git panel

Fixes: 

- Fixed message queueing
- Fixed binary files showing up incorrectly in the git diff

# Toggle Big Terminal Mode
_0.10.2_ 
Sept 10th, 2025 

<img width="486" height="310" alt="image" src="https://github.com/user-attachments/assets/11177c6c-cdd8-4732-aa76-84e46cfae4bd" />

Improvements: 

- Switch to Big Terminal mode within a workspace
- Focus on the composer when the diff viewer closes
- Unified view for added/deleted files in the diff viewer
- Faster Linear issue loading
- Improved diff viewer code theme
- New “thinking” interface

Fixes: 

- Fix binary file line counting

# Checkout PRs in Conductor 
_0.10.1_ 
Sept 9th, 2025 

You can now checkout an existing PR directly from the Dispatcher! 

<img width="1216" height="1058" alt="image" src="https://github.com/user-attachments/assets/a1d5f6f9-0927-4c23-8673-6bcd1fc8215a" />

Improvements: 

- Added support for file level comments in the diff viewer
- Added options to open a workspace in an external application to the command palette

Fixes: 

- Fixed inaccuracies in large diffs
- Fixed a bug where draft comments could get reset due to re-renders
- Fixed UI overflow in setup scripts

# Code Review
_0.10.0_ 
Sept 8th, 2025 

You can now comment on a diff and we’ll send your feedback straight to Claude! 

<img width="2048" height="1323" alt="image" src="https://github.com/user-attachments/assets/d1c0356a-eef2-41de-8de0-56c6a2cb5384" /> 

Fixes: 

- Fixed a bug where setup scripts failing would leave workspaces stuck in a “setting up” state 
- Fixed a bug where rows could sometimes not be selected in the Dispatcher 

# New Diff Review Panel, Faster Claude
_0.9.3_
Sept 6th, 2025

We’ve upgrade the diff review panel. It’s now much more performant and easy to read.

<img width="3024" height="1824" alt="CleanShot 2025-09-06 at 14 08 23@2x" src="https://github.com/user-attachments/assets/9dfeb99a-c08f-4930-8eb5-2f8844f72728" />

Claude’s response times are now just as fast as in the CLI! Conductor now installs Claude Code via the native binary installation, so Claude responds faster and you no longer need `npm`. 

Improvements: 

- Open files in preferred editor from the file preview
- Send messages with attachments only
- Added bash syntax highlighting to setup/run/archive scripts
- Ready to run empty state is now clickable
- Detect agents in nested folders within ~/.claude/agents

Fixes: 

- Added docs and feedback links to help menu button

# Bug Fixes!
_0.9.2_
Sept 3rd, 2025

Improvements: 

- Added Settings to the macOS menu bar
- Show when Claude Code will next be usable when users hit their usage limit
- New workspace names are validated to prevent duplicate branch names

Fixes: 

- Fixed sort order of Linear search results
- Only show error retry buttons on the most recent chat turn
- Terminal processes exiting will not automatically close the respective terminal tab
- Capitalization is now preserved in new workspace names

  
# Open dev scripts and more performant long chats
_0.9.1_
Sept 2nd, 2025

Conductor now detects when a localhost URL is running. Open it in your browser by clicking `Open` or ⌘+Shift+O.

<img width="998" height="586" alt="image" src="https://github.com/user-attachments/assets/85d8953e-6136-495c-8b51-1be510cc75a2" />

Improvements: 

- Long chats now render much faster (we virtualized!)
- ⌘+Enter shortcut to submit dialogs
- We now show a `Compact and Retry` button when your session runs out of context
- Add docs to command palette

Fixes: 

- Fixed a bug where thinking output would show excessive newlines
- Focus the run tab on run button click
- Updated terminal button styles for consistency
- Fix “Open In” menu apps not showing for some users
- Fix auto scroll not working on new messages received from the AI
- Fixed a bug where files selected in the filepicker with NextJS slugs wouldn’t render properly
- Fixed a bug where archiving a workspace would not terminate its run script

# Run script, hooks, and custom fonts
_0.9.0_
Sept 1st, 2025

Add a run script to create a one-click shortcut (or ⌘R) to your tests or development server.

<img width="914" height="892" alt="image" src="https://github.com/user-attachments/assets/3869a0a7-535f-49d8-b00c-8e121893f11c" />

Project level slash commands and agents are now usable in Conductor! 

<img width="502" height="566" alt="image" src="https://github.com/user-attachments/assets/44a72d5c-df75-4c9f-80ef-31a9ea6e320e" />

Global hooks and memory are now configurable in Conductor! 

<img width="1530" height="1394" alt="image" src="https://github.com/user-attachments/assets/6868d227-ffcf-459d-a637-ae87b6accec0" />

You can now set a custom terminal font in settings! 

<img width="1664" height="1526" alt="image" src="https://github.com/user-attachments/assets/f5303c5c-14fa-4a48-b61c-cd91e59d9f38" />

We’ve also added the PR status to the sidebar:

<img width="622" height="666" alt="image" src="https://github.com/user-attachments/assets/b98c2078-061d-4d87-a91f-a55160743e69" />

Improvements: 

- Conductor’s doc site is now live at [https://docs.conductor.build](https://docs.conductor.build/)
- Added support for opening draft PRs in the git panel
- Added support for manually opening PRs via the git panel
- Auto-convert long text snippet pastes into attachments for better readability

Fixes: 

- Fixed loading icon animations throughout the app that would wobble off axis
- Fixed a bug where `/clear` would not clear the session
- Fixed popover border radius inconsistencies
- Fixed composer border radius inconsistencies
- Fixed referenced files not being truncated and highlighted in user messages
- Fixed a bug where multi-line `$ARGUMENTS` wouldn’t register with slash commands

Misc: 

- Telemetry improvements





# Performance Improvements 
_0.8.2_ - _0.8.3_
August 26th, 2025 

Improvements: 

- Linear issues are now sorted by status
- Searched Linear issues are now filtered by the teams you belong to 
- Reduced letter spacing for smaller text sizes
- Increased the spacing of the git panel title 

Fixes: 

- Fixed a bug where workspaces would fail to load and crash the app if the MultiEdit write tool had errors
- Fixed a bug where Bash tool calls could not be expanded
- Fixed a bug where the Read tool would show “Read 0 lines"
- Fixed part of the composer being unclickable 
- Fixed part of the terminal being unclickable 
- Fixed a performance issue in the git diff dialog that would crash the app
- Fixed a bug where the “Merge” button was inaccurately showing for GitHub repositories with multiple CI checks

Misc: 

- Increased the minimum width of the right sidebar
- cmd+A will no longer incorrectly select all of the visible text in the app

New in 0.8.3:

- Support for slashes in Linear branch names

# Suggested Git Actions 
_0.8.1_ 
August 25th, 2025 

Conductor now recommends each step on the way to merging your PR. Click the button in the top right to take the next action.

<img width="1250" height="1006" alt="image" src="https://github.com/user-attachments/assets/39c8081c-9827-4e2d-ad73-63eab3c81016" />

Improvements: 

- Auto focus the terminal when opening and closing tabs
- Updated font weights and styles
- Add Sublime Text to the “Open In” menu

Fixes: 

- Show the correct creation time for workspaces in the sidebar
- Better performance when fetching Linear issues
- Switching between custom providers in a workspace is more reliable
- Updated the compact icon used in the chat 

# Integrate with Linear, Faster Claude
_0.8.0_
August 25th, 2025 

Introducing the Dispatcher, a new way to create workspaces. You can now choose a branch name when creating a new workspaces, or create a new workspace from one of your Linear issues.

<img width="1324" height="962" alt="image" src="https://github.com/user-attachments/assets/b3dac156-2096-4c38-af2c-8e31a1aed87f" />

We’ve also added a new Auto mode, where Opus plans and Sonnet implements.

<img width="572" height="390" alt="image" src="https://github.com/user-attachments/assets/4a6cf899-4093-4f41-ab9c-cc589ab54dac" />

For CLI fans, we’ve added Big Terminal Mode™. Go to settings → Big Terminal Mode to change the center pane to a terminal. (Warning: not for the faint of heart. This will replace the chat interface!)

<img width="2048" height="1337" alt="image" src="https://github.com/user-attachments/assets/82e50dac-1129-42b3-82f5-81cd837880a0" />

We’ve made some performance improvements. The app should run faster overall, and Claude will respond a few seconds faster to every message.

Improvements: 

- Opus plan mode
- ⌘⇧[1-5] keyboard shortcut to change terminal tabs
- ⌘W to close focused terminal tab
- ⌘T to create a new terminal tab when focused on the terminal
- Refined tooltip + font rendering
- ⇧Tab to toggle plan mode (replacing ⌘P)
- Big terminal mode
- Open in XCode

Fixes: 

- Border styling
- Attachments no longer included in Create PR message

# Plan Mode
_0.7.3_
August 22nd, 2025 

<img width="1174" height="334" alt="image" src="https://github.com/user-attachments/assets/08a3e637-9c21-403a-b523-b610328310ba" />

Plan mode (⌘P) tells the AI to make a plan before editing files.

Improvements: 

- ⌘O to open a repository from the repository page

Fixes: 

- Fixed a bug where the `@` file picker wouldn’t populate in new workspaces
- The loading indicator no longer jumps around in the chat
- Fixed a bug where the git panel and diff dialog used different sort orders for displaying files

Misc: 

- Feedback dialog now supports image uploads

# Add terminal context to chat
_0.7.2_
August 19th, 2025 

You can now send terminal context to chat by highlighting output and ⌘L to add it to chat. 

Also, creating a workspace is now much faster.

<img width="1474" height="686" alt="CleanShot 2025-08-18 at 11 38 01@2x" src="https://github.com/user-attachments/assets/a87ce9aa-0cc1-4d34-a556-7ed36792a46a" />

Improvements: 

- Select text in terminal and press ⌘L to send it to chat
- Workspace creation is faster
- Clicking a file in the diff panel now auto-scrolls to the diff
- You can now press ⌘W to close a focused terminal window
- Button styling is more consistent throughout the app
- There’s now a … icon in the sidebar that points to the repository settings page
- Added more apps to the Open In button

Fixes:

- Fixed an issue with positioning of the `@` file picker
- Fixed an issue where `@` file picker highlights wouldn’t scroll with the text
- Fixed an issue where some items wouldn’t appear in command palette search results
- Fixed an issue with scroll-to-bottom when switching workspaces
- Fixed the background color of the Conductor logo on the login page

# We no longer burn your CPU (hopefully)
_0.7.0_ - 0.7.1
August 14th, 2025 

Before

<img width="756" height="108" alt="CleanShot 2025-08-14 at 13 39 03@2x" src="https://github.com/user-attachments/assets/e81fcc29-eb0a-4f05-b628-826d8fa6db07" />

After

<img width="748" height="106" alt="CleanShot 2025-08-14 at 13 40 03@2x" src="https://github.com/user-attachments/assets/fd98b248-2271-445a-8f45-187c368f765f" />

We've also standardized our color palette for rendering code diffs.

<img width="1290" height="816" alt="CleanShot 2025-08-14 at 14 51 20@2x" src="https://github.com/user-attachments/assets/968733c0-f68e-4016-a688-190864c2d901" />


Improvements: 

- Added a close button to the git diff dialog
- Consistent syntax highlighting colors for diffs
- New sound effect: Choo-Choo!

Fixes: 

- Fixed a resource leak that would happen when a terminal shut down

Misc: 

- Clicking a file name in the chat will now open the file in your preferred editor
- Improved error message when the same repository is imported twice to Conductor
- Improved error message for repositories that don’t have a remote named `origin`


# Bug Fixes! 
_0.6.1_ - _0.6.2_
August 12th, 2025 

Improvements: 

- Added a sound effect that plays on workspace completion
- Added special styling for context7 and Linear MCPs
- Added an option to view only uncommitted changes in the git diff dialog
- Added the “X” icon to all terminals so they’re easier to quit

Fixes:

- Fixed a bug where text could be inadvertently selected in the sidebar
- Fixed the system theme selection not being respected
- Fixed a bug where the model selection popover could go off screen
- Fixed a bug where the educational tooltip would appear briefly on startup for all users
- Fixed a resource leak when closing terminal tabs
- Fixed a case where Claude Code could make edits outside of your workspace’s directory
- Fixed a bug where typing a space would close the file suggestions popover in the composer
- Fixed an overflow issue in the “Archive Anyway?” dialog
- Disabled Git stats from updating while a workspace is archiving
- Fixed a bug where the “Compact and Retry” button would re-send the incorrect message

Misc: 

- Claude Code is now aware of your repository’s default branch

New in 0.6.2:

- Fixed a bug causing new workspaces to fail
- Improved repository details page

# A New Look
_0.6.0_ 
August 9th, 2025 

We’ve overhauled Conductor’s design. It’s now sleeker, more intuitive, and feels right at home on your Mac.

<img width="2972" height="1758" alt="CleanShot 2025-08-09 at 13 49 21@2x" src="https://github.com/user-attachments/assets/036c1352-3d84-4989-95df-91edd3a22347" />

The sidebar is now easier to parse. Get a clear view of what your agents are working on at a glance.

<img width="480" height="1282" alt="CleanShot 2025-08-09 at 14 23 55@2x" src="https://github.com/user-attachments/assets/7da2fa87-22ad-4287-8dc6-3a194101bdef" />

Messages display more consistently and are easier to read. We auto-collapse Claude’s tools, but you can always peek under the hood.

<img width="1092" height="762" alt="CleanShot 2025-08-09 at 14 02 32@2x" src="https://github.com/user-attachments/assets/95f43b66-ca6b-4457-b34c-b98f244a25e6" />

We’ve also redesigned the repository details page and added a configurable archive script:

<img width="2926" height="1728" alt="CleanShot 2025-08-09 at 14 22 31@2x" src="https://github.com/user-attachments/assets/eb957581-1633-4929-8649-c193f77d7100" />

And you can now make multiple tabs in your terminal.

<img width="824" height="796" alt="CleanShot 2025-08-09 at 14 06 11@2x" src="https://github.com/user-attachments/assets/d090d73b-d4d1-47ab-b011-7b4144b63e40" />

Improvements: 

- Support for multiple terminal tabs
- Added optional archive script
- Added a max height for composer
- Support for .log file attachments
- Added JetBrains Rider to the "Open" menu
- New workspaces are now prefixed with your git username instead of `conductor/`

Fixes:

- Fixed issue where GitHub repos failed to load

# GPT-5 

_0.5.0_ 
August 7th, 2025 

GPT-5 is live in Conductor! 

<img width="686" height="386" alt="image" src="https://github.com/user-attachments/assets/d39527bd-9a7b-4560-bca0-c1454708c0f1" />

To enable GPT-5, go to Settings → Provider → Select OpenAI as the provider, then add your API key. 

We’ve also refreshed the design of the sidebar! Each workspace now includes relevant Git status. 

<img width="662" height="1834" alt="no-bg-CleanShot 2025-08-07 at 09 39 06@2x" src="https://github.com/user-attachments/assets/ec83a39f-e559-4bd3-9f8b-a7c7b16b3ad9" />

Improvements: 

- Added IntelliJ as an “Open In IDE” option

Fixes: 

- Made several performance improvements to the main chat window to reduce lag
- Fixed the repository click area in the sidebar
- Fixed several performance issues with the git diff dialog
- Fixed the “Add thinking” popover from clipping off screen for some users

# Opus 4.1 
_0.3.2_
August 5th, 2025 

Claude Opus 4.1 is now available in Conductor! 

<img width="1200" height="632" alt="image" src="https://github.com/user-attachments/assets/762894c3-a0e6-4b5a-9685-e9047d365cc8" />

Improvements: 

- Added drag and drop to reorder repositories in the left sidebar
- Added PyCharm as an “Open In IDE” option
- Conductor now remembers where you last cloned a repo and defaults to that location for new clones. Also, the initial default path is now `~/conductor`.

Fixes: 

- Fixed a bug where the “Add Repository” popover was not visible on some screens

Misc: 

- Improved error message when failing to authenticate with `gh`
- Added the full URL that was fetched to the top of the WebFetch tool call

# Bug Fixes! 
_0.3.1_ 
August 4th, 2025 

Improvements: 

- When you add a new file, it will now show up in the `@` autocomplete list
- Added a “scroll to bottom” button in long workspaces

Fixes: 

- Fixed a bug where pressing `escape` to close a modal could cancel the current chat session
- Fixed a bug where clicking a commit shown in the chat would not open it in the git diff dialog
- Fixed a bug where stats would not display correctly for commits in the git diff dialog
- Fixed spacing in the auto-compact warning message

# Git Diff View
_0.3.0_
August 2nd, 2025

You can now see your up-to-date git status directly in the sidebar!

<img width="3184" height="2050" alt="CleanShot 2025-08-01 at 19 50 38@2x" src="https://github.com/user-attachments/assets/772fdf5a-b276-4c21-8e4d-6d65a3a31cb9" />

We've also improved diff rendering and added an option to filter by commit: 

<img width="2872" height="1852" alt="CleanShot 2025-08-01 at 19 51 21@2x" src="https://github.com/user-attachments/assets/b6da7db7-94af-40b9-8067-d1cd82bdeb3b" />

Other improvements: 

- When Claude returns an error, there's a new “Retry Message” button
- You can now collapse repos in the sidebar
- You can now drag-and-drop to add a new repo on the home page
- When you resize the right sidebar panels, Conductor will now remember your settings
- Conductor will now auto-detect your repository’s default branch when you first clone it
- Cleaned up the UI for adding new repositories
- Added keyboard shortcuts for toggling the theme (⌘⇧T) and sending feedback (⌘⇧F)

Fixes: 

- Fixed a bug where `@` autocomplete suggestions would be hidden behind suggested git actions
- Fixed a styling issue with hover state in the sidebar

Misc:

- We’ve removed the “% context used” indicator because the numbers Anthropic gives us don’t let us estimate this reliably
- We have a new email address: [humans@conductor.build](mailto:humans@conductor.build). The feedback, bug reports, and suggestions have been super helpful—please keep them coming!

# Bugfixes
_0.2.2_ - _0.2.4_
July 31th, 2025

We're experimenting with automatically collapsing Claude's responses. Long chats should also now be much more performant. 

<img width="1522" height="770" alt="CleanShot 2025-07-31 at 22 53 50@2x" src="https://github.com/user-attachments/assets/78e57a8b-f6c3-4067-95ea-936092763df4" />

You can also now `@` agents to explicitly call them. 

<img width="624" height="358" alt="CleanShot 2025-07-31 at 22 52 02@2x" src="https://github.com/user-attachments/assets/e683aa0c-f02a-4325-9f69-26fbfa7925cd" />

Improvements: 

- Performance improvements on long chats
- Long messages from Claude Code now collapse automatically
- Show when a workspace is compacting in the sidebar
- Added syntax highlighting for setup scripts
- Right click to mark workspace as unread
- `@` Agents to explicitly call them

Fixes:

- Long chats are faster to render
- Fixed a bug where archiving workspaces would fail unrecoverably
- Fixed an issue where hover states became invisible in dark mode
- Fixed a bug where you could add the same directory twice
- We now validate that the chosen directory exists before cloning a repo
- Fixed typography discrepancies throughout the UI
- Fixed an issue that could lead to a double slash // in the clone target path
- Fixed a missing space between tool names and the files they affected
- Fixed a bug where system theme changes would not be recognized by Conductor

Misc: 

- Updated the command menu to include recently added features
- Added Windsurf to the “Open In” menu
- Added support for `.xlsx` attachments

New in 0.2.3:

- Agents in Conductor can now help the user out with understanding Conductor’s workspace system, and will follow the system better.
- This will help prevent an occasional issue where Claude would mistakenly edit files in the root directory.

New in 0.2.4:

- Fixed a bug where certain messages would appear out of order

# Local Repositories + Agents
_0.2.0_ - _0.2.1_ 
July 29th, 2025

Conductor now supports local repositories! You can add a new repository from your local filesystem, GitHub, or any Git URL.

<img width="1234" height="748" alt="CleanShot 2025-07-29 at 21 46 34@2x" src="https://github.com/user-attachments/assets/7d7b21c1-3b16-4667-bbec-075d429da05b" />

We’ve also added [agents](https://docs.anthropic.com/en/docs/claude-code/sub-agents). Conductor can now call custom agents to perform specialized tasks like code review and test automation. Create one in Settings → Agents.  

<img width="1690" height="1030" alt="CleanShot 2025-07-29 at 23 12 10@2x" src="https://github.com/user-attachments/assets/7ea6bce3-55b9-4fdd-a38f-7c145a014059" />

Improvements: 

- Revamped repository page
- Added `/compact` and `/clear` commands
- Model configurations are now stored per workspace instead of globally
- Simplified API key configuration and added HTTP proxy support
- Added copy button to all chat messages
- Repositories are now highlighted when selected in the sidebar 
- URLs are now clickable in terminal output

Fixes:

- Fixed a bug where Conductor wouldn’t check for auto-compaction between each message in the queue
- Fixed a bug where cancelling would leave queued messages in a bad state
- Fixed a bug where session notifications would be sent while there are queued messages
- Composer buttons are now accessible while sending queued messages
- Fixed Bash commands rendering overlapping content
- Several stability improvements to sending and persisting user messages
- Always use local Git authentication 
- Fixed a bug where workspaces couldn’t be archived due to PATH issues

Misc: 

- Updated the shortcut to cancel a message from `⌘+Del` to `esc`.
- Show minutes on the loading indicator

# Slash Commands + Custom Providers 
_0.1.1_ 
July 25th, 2025 

Slash commands are live in Conductor! Manage your commands in Settings. 

<img width="1660" height="600" alt="image" src="https://github.com/user-attachments/assets/d939180a-b086-4b57-8e4c-da5d770f30ca" />

You can now also customize your Claude provider.

<img width="1776" height="746" alt="image" src="https://github.com/user-attachments/assets/774601ae-5545-4fc0-ba2c-03b1533c117b" />

Improvements: 

- Messages can now be queued during compaction
- Added a confirmation dialog when removing MCP servers
- Included the repo’s default branch in the message generated by the “Create PR” button

Fixes: 

- Disabled the compact and clear buttons while Claude Code is streaming responses
- Include dotfiles in `@` file mentions
- Fixed the workspace sidebar overlapping with the Mac traffic lights on scroll
- Fixed long tool names overflowing
- Fixed certain tool outputs not being scrollable
- Fixed a bug where the “system” theme was not being respected throughout the app

# MCPs + Message Queues
_0.1.0_ 
July 24th, 2025 

MCPs are live in Conductor! Add popular servers in one click from the MCP tab.

<img width="1732" height="450" alt="image" src="https://github.com/user-attachments/assets/9fad1f74-b5fb-4ed2-89cb-3c7bb94d7c0e" />

Conductor also now supports message queues! Submit multiple messages and they will be processed in order. 

<img width="1606" height="778" alt="image" src="https://github.com/user-attachments/assets/5f61cc93-d888-44f0-aaa3-8170a0875bbc" />

Improvements: 

- Performance improvements (if Conductor is running slowly for you, [please let us know](mailto:founders@melty.sh?subject=Conductor%20perf%20issues)!)
- Add a setting to customize the auto-compact threshold
- The `Compact and Continue` error button now re-sends your last message
- Navigate between workspaces easily with shortcuts (`⌘+1→9`)
- Add a setting to change message submit shortcut
- Keyboard shortcut for archiving (`⌘⇧A`)
- Redesigned the onboarding experience for new users
- Bundle size is now 5mb smaller

Fixes: 

- Fixed a bug causing GitHub permissions to not fail on push
- Fixed a bug where archiving a workspace would force you back to the home if you’ve already navigated away
- Fixed a bug where the Close button would not exit the app
- Fixed GitHub PRs showing as issues on the home page


# Fine-grained GitHub permissions
_0.0.21_
July 22nd, 2025 

You can now give Conductor fine-grained GitHub repository access. You can also choose to skip the GitHub integration and add repositories using your SSH/HTTPs authentication.


<img width="1374" height="842" alt="CleanShot 2025-07-22 at 17 53 01@2x" src="https://github.com/user-attachments/assets/3d5d206d-1fac-41ae-a72a-44df85a059ec" />

To manage the GitHub integration, go to settings (`⌘+,`) and click Connect GitHub app:

<img width="1100" height="152" alt="CleanShot 2025-07-22 at 17 54 19@2x" src="https://github.com/user-attachments/assets/19104eed-01e1-46dd-856b-c4632a119d21" />




# Attachments 
_0.0.20_ 
July 22nd, 2025 

Conductor now supports attachments! 

<img width="1754" height="478" alt="image" src="https://github.com/user-attachments/assets/73322103-6874-4eac-a2d9-16da5692586e" />

Upload files by pasting (`⌘+V`), dragging and dropping, or clicking the paperclip icon in the Composer. 

Improvements: 

- The default branch can now be configured per repository
    - Select a repository in the sidebar to configure its default branch, or use “More Options” when adding a new repository
- Added an option to open a workspace in Warp
- Added a button to copy a chat compaction summary
- Added a list of all in-app shortcuts accessible via `Cmd+/`
- The archive confirmation dialog now closes immediately when “Archive Anyway” is clicked

Fixes: 

- Optimized the rendering performance of workspaces with long chat histories
- Fixed a bug where workspace setup scripts wouldn’t run when creating a workspace from a GitHub Issue

Misc: 

- Disabled the “Create PR” button while Claude is sending messages

# Misc Improvements
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
