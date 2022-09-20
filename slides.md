---
title: Guy's Productivity Toolbelt
theme: black
controls: true
---

## Guy's <br/> Productivity <br/> Toolbelt

---

## Disclaimer

- Windows <!-- .element: class="fragment" -->
- Visual Studio <!-- .element: class="fragment" -->

---

### Cheat Sheets

<!-- .element -->

- Atlassian Git Cheat Sheet
- HTTP Error Codes Cheat Sheet
- Resharper - Visual Studio Scheme
- Resharper - IntelliJ IDEA Scheme
- The Ultimate Markdown Cheat Sheet
- Azure Periodic Table of Resource Naming Convention Shorthands

<!-- .element: class="fragment" -->

---

### Themes

[Dracula Theme](https://draculatheme.com/) <!-- .element: class="fragment" -->

---

## Browser Extensions

- Speed Dial 2 New Tab <!-- .element: class="fragment" -->
- uBlock Origin <!-- .element: class="fragment" -->
- I don’t care about cookies <!-- .element: class="fragment" -->
- Dashlane Passwordmanager <!-- .element: class="fragment" -->
- Stylus + Tampermonkey <!-- .element: class="fragment" -->
- Environment Marker <!-- .element: class="fragment" -->
- JSON Formatter <!-- .element: class="fragment" -->

---

## Windows Tools

----

### Ditto Clipboard

----

### Everything

----

### Agent Ransack

----

### Bulk Rename Utility

----

### Microsoft PowerToys

----

### DevToys

----

### Simplenote

----

### Seq

[Centralized structured logging](https://datalust.co/seq) <!-- .element: class="fragment" -->

----

### TaskbarX

----

### AutoHotkey

----

Example Script

```ahk[6|8-10|12-17]
#NoEnv  ; Recommended for performance and compatibility with future AutoHotkey releases.
; #Warn  ; Enable warnings to assist with detecting common errors.
SendMode Input  ; Recommended for new scripts due to its superior speed and reliability.
SetWorkingDir %A_ScriptDir%  ; Ensures a consistent starting directory.

InReplaceMode := false

^+u::
InReplaceMode := !InReplaceMode
return

#if InReplaceMode
{
  $Space::SendInput _
  $Return::InReplaceMode := false
}  
return
```

----

Activate AutoHotkey on Startup

```shell
schtasks 
 /create 
 /tn "Start AutoHotkey script SpaceToUnderscore"
 /tr 'C:\Program Files\AutoHotkey\AutoHotkey.exe C:\Tools\SpaceToUnderscore.ahk' 
 /sc onlogon
```

----

### Chocolatey

[Install applications and keep them up to date](https://community.chocolatey.org/packages) <!-- .element: class="fragment" -->

----

Create Scheduled Task to upgrade all applications

```shell
schtasks 
 /create 
 /tn "Choco Upgrade All Daily" 
 /tr 'choco upgrade all' 
 /sc daily 
 /st 09:00 
 /rl HIGHEST
```

----

#### Export installed applications

```shell
choco export "c:\temp\packages.config"
```

#### Install applications from config file

```shell
choco install "c:\temp\packages.config"
```

---

## Visual Studio Tools

----

### Resharper

----

### CodeMaid

----

### VSColorOutput

----

### Rainbow Braces

----

### Help Menu

----

### Windows Defender Exclusions

[Braytiner/Windows Defender Exclusions VS 2022.ps1](https://gist.github.com/Braytiner/be2497d1a06f5a9d943dc7760693d460) <!-- .element: class="fragment" -->

---

## Visual Studio Code Tools

----

### Project Dashboard

----

### Rainbow Brackets

---

## Windows Terminal Extensions

- CaskaydiaCove NF font <!-- .element: class="fragment" -->
- Oh My Posh <!-- .element: class="fragment" -->
- Terminal-Icons <!-- .element: class="fragment" -->
- ZLocation <!-- .element: class="fragment" -->

<!-- .element -->
How to: [Scott Hanselman - Ultimate PowerShell prompt](https://www.hanselman.com/blog/my-ultimate-powershell-prompt-with-oh-my-posh-and-the-windows-terminal)
<!-- .element: class="fragment" -->

---

## Git

----

### Aliases

----

```ini
aa = add --all
aliases = config --get-regexp alias
branches = branch
cm = commit -m
configure = config --global --edit
fm = fetch origin master:master
fn = fetch origin main:main
h = log --graph --all --pretty=format:'%C(auto)%d %s %C(yellow)%ad %C(cyan)<%an> %C(green)%h' --date='format-local:%Y-%m-%d %H:%M:%S'
login = git config credential.helper store
mm = merge master
mn = merge main
pushit = push --no-verify
pushup = push -u origin HEAD
s = status
uncommit = reset --soft HEAD^
unstage = reset HEAD --
```

----

### Worktree

<small>

- git worktree add -b emergency-fix ../temp master <!-- .element: class="fragment" -->
- fix things <!-- .element: class="fragment" -->
- git worktree remove ../temp <!-- .element: class="fragment" -->

</small>

----

[git-removed-branches](https://www.npmjs.com/package/git-removed-branches)

---

### The End

[https://github.com/guyvdn/toolbelt](https://github.com/guyvdn/toolbelt) <!-- .element: class="fragment" -->
