---
title: Guy's Productivity Toolbelt
theme: black
controls: true
---

## Guy's <br/> Productivity <br/> Toolbelt

18/09/2022

---

## Disclaimer

- Windows <!-- .element: class="fragment" -->
- Visual Studio <!-- .element: class="fragment" -->

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

### Windows Defender Exclusions

[https://gist.github.com/Braytiner/be2497d1a06f5a9d943dc7760693d460](https://gist.github.com/Braytiner/be2497d1a06f5a9d943dc7760693d460)

---

## Visual Studio Code Tools

----

### Project Dashboard

---

## Git

----

### Aliases

----

```ini [2|3|4|5|6|7|8|9|10|11|12|13|14|15]
[alias]
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

* git worktree add -b emergency-fix ../temp master <!-- .element: class="fragment" -->
* fix things <!-- .element: class="fragment" -->
* git worktree remove ../temp <!-- .element: class="fragment" -->

</small>

----

## Browser Extensions

* Speed Dial 2 New Tab <!-- .element: class="fragment" -->
* uBlock Origin <!-- .element: class="fragment" -->
* I don’t care about cookies <!-- .element: class="fragment" -->
* Dashlane Passwordmanager <!-- .element: class="fragment" -->
* Stylus + Tampermonkey <!-- .element: class="fragment" -->

----

## Windows Terminal Extensions

* CaskaydiaCove NF font <!-- .element: class="fragment" -->
* Oh My Posh <!-- .element: class="fragment" -->
* Terminal-Icons <!-- .element: class="fragment" -->
* ZLocation <!-- .element: class="fragment" -->

Howto: [Scott Hanselman - Ultimate PowerShell prompt](https://www.hanselman.com/blog/my-ultimate-powershell-prompt-with-oh-my-posh-and-the-windows-terminal) <!-- .element: class="fragment" -->

----

### Themes

----

### Cheat Sheets

