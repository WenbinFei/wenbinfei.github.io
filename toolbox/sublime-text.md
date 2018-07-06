---
layout: page
title: Sublime text
modified: 
excerpt: "sublime text skills"
comments: false
share: false
image:
  feature: 
  credit: 
  creditlink: 
---
## Proofreading
[**Language tool**](https://www.languagetool.org/) is an open source proofreading software for Engilish, French, German and more than 20 other languages.

Language tool for Sublime Text 2/3 can be found at https://github.com/gtarawneh/languagetool-sublime .

### Installation
`ctrl+shift+p` open command palette, type `install`, press Enter then type `languagetool`.

To get the latest updates before they get released, install via `Package
Control: Add Repository`. This will update your plugin with new commits as
they are being pushed to the repo.

#### Usage

Open the file you want to proof-read then:

1. Run a language check (<kbd>ctrl+shift+c</kbd>). Any problems identified by LanguageTool will be highlighted.
2. Move between the problems using <kbd>alt+down</kbd> (next) and <kbd>alt+up</kbd> (previous).
3. A panel at the bottom will display a brief description  of the highlighted problem and suggest corrections if available.
4. Begin typing to correct the selected problem or press <kbd>alt+shift+f</kbd> to apply the suggested correction.
5. To ignore a problem, press <kbd>alt+d</kbd>.
6. Auto-correcting a problem or ignoring it will move focus to the next problem.

All commands and their keyboard shortcuts are in the command palette with the
prefix `LanguageTool:`.

#### Configuration

The settings file for the plugin can be opened from the `Preferences` menu
(`Preferences` &rarr; `Package Settings` &rarr; `LanguageTool` &rarr;
`Settings - User`). Default settings are in the corresponding submenu item
`Settings - Default`. Note that default settings are provided for reference
and should not be edited as they may be overwritten when the plugin is updated
or reinstalled. Instead, copy and modify any settings you wish to override to
`Settings - User`.

#### Local vs. Remote Checking

The adapter supports local and remote LanguageTool servers. Remote checking is
the default and works by submitting text over https to an api endpoint on
https://languagetool.org (this can be changed in plugin settings). This public
service is subject to usage constraints including:

1. Maximum text size of 50Kb
2. Access limited to 20 requests/minute per IP

(See http://wiki.languagetool.org/public-http-api for full details.)

Instead of using the public (remote) LanguageTool service, text can be checked
using a local LanguageTool Installation. A local LanguageTool server can be
started by the plugin itself using the command `LanguageTool: Start Local
Server` (this requires the settings entry `languagetool_jar` to point to the
local languagetool JAR file), or from the command line following the
instructions in http://wiki.languagetool.org/http-server.

The settings file contains remote and local server URL entries. A third option
`default_server` indicates which of these is used when the command
`LanguageTool: Check Text` is ran. As an added convenience, two more commands:

* `LanguageTool: Check Text (Local Server)`
* `LanguageTool: Check Text (Remote Server)`

are provided, which can be used to check text using the local/remote servers
regardless of `default_server`. This can be used for one-off checks when it's
desirable to use a particular server with certain pieces of text.

## Spell check for markdown

Open a markdown file and go to `Preferences > Settings-Syntax specific`

and 

```
{
	"spell_check": true
}
```

