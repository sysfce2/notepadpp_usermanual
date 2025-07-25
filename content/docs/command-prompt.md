---
title: Command Line Arguments
linktitle: Command Line Arguments
weight: 130
---

Notepad++ supports various case-sensitive command line arguments
to control its startup and affect its behavior.

## Help usage

```
notepad++ [--help] [-multiInst] [-noPlugin]
  [-l<Language>] [-udl="My UDL Name"]
  [-L<langCode>]
  [-n<line>] [-c<column>] [-p<pos>] [-x<left-pos>] [-y<TopPos>]
  [-monitor] [-nosession] [-notabbar] [-ro] [-systemtray] [-loadingTime]
  [-alwaysOnTop] [-openSession] [-r]
  [-qn="Easter Egg Name" | -qt="Text to Type" | -qf="D:\path to\file"]
  [-qSpeed(1|2|3)] [-quickPrint]
  [-settingsDir="d:\your settings dir\"] [-openFoldersAsWorkspace]
  [-titleAdd="additional title bar text"]
  [-pluginMessage="text for plugin(s)"]
  [filepath]
```

* `--help`: The help message for command line arguments. It will be shown before
  Notepad++'s launch.
* `-multiInst`: Launch another Notepad++ instance, so user can have several
  Notepad++ simultaneously.
* `-noPlugin`: Launch Notepad++ without loading any plugin.
* `-l`: Open file or display ghost typing with syntax highlighting of choice.
  *Language* is a short identifier string: the full list can be found in `langs.model.xml`
  (as the names of each `<Language name="...">` element).
  {{< details "show example Programming Language identifiers" >}}
  `normal`, `actionscript`, `ada`, `asm`, `asn1`, `asp`, `autoit`, `avs`,
  `baanc`, `bash`, `batch`, `blitzbasic`, `c`, `caml`, `cmake`, `cobol`,
  `coffeescript`, `cpp`, `cs`, `csound`, `css`, `d`, `diff`, `erlang`,
  `escript`, `forth`, `fortran`, `fortran77`, `freebasic`, `gdscript`, `go`,
  `gui4cli`, `haskell`, `hollywood`, `html`, `ihex`, `ini`, `inno`, `java`,
  `javascript`, `javascript`, `json`, `json5`, `jsp`, `kix`, `latex`, `lisp`,
  `makefile`, `matlab`, `mmixal`, `mssql`, `nfo`, `nim`, `nncrontab`, `nsis`,
  `objc`, `oscript`, `pascal`, `perl`, `php`, `postscript`, `powershell`,
  `props`, `purebasic`, `python`, `r`, `raku`, `rc`, `rebol`, `registry`,
  `ruby`, `rust`, `sas`, `scheme`, `smalltalk`, `spice`, `sql`, `srec`,
  `swift`, `tcl`, `tehex`, `tex`, `toml`, `txt2tags`, `typescript`, `vb`,
  `verilog`, `vhdl`, `visualprolog`, `xml`, `yaml`.
 {{< /details >}}
* `-udl="My UDL Name"`: Open file with User Defined Language (UDL) syntax
  highlighting `My UDL Name` active.  If the UDL name does not conain spaces, the
  quote marks aren't required around the name (like `-udl=MyUDL`). The UDL name
  should match an existing UDL.  Mutually exclusive with `-l` (UDL will take priority
  over standard syntax highlighter).  (new to v8.1.2)
* `-L`: Apply indicated localization, *langCode* maps to the localization file name:
    {{< details "show Language Codes" >}}
code | file
---|---
`ab`, `abk` | `abkhazian.xml`
`af` | `afrikaans.xml`
`an` | `aragonese.xml`
`ar`, `ar-dz`, `ar-bh`, `ar-eg`, `ar-iq`, `ar-jo`, `ar-kw`, `ar-lb`, `ar-ly`, `ar-ma`, `ar-om`, `ar-qa`, `ar-sa`, `ar-sy`, `ar-tn`, `ar-ae`, `ar-ye` | `arabic.xml`
`az` | `azerbaijani.xml`
`be` | `belarusian.xml`
`bg` | `bulgarian.xml`
`bn` | `bengali.xml`
`br-fr` | `breton.xml`
`bs` | `bosnian.xml`
`ca` | `catalan.xml`
`co`, `co-fr` | `corsican.xml`
`cs` | `czech.xml`
`cy-gb` | `welsh.xml`
`da` | `danish.xml`
`de`, `de-at`, `de-de`, `de-li`, `de-lu`, `de-ch` | `german.xml`
`el` | `greek.xml`
`eo` | `esperanto.xml`
`es-ar` | `spanish_ar.xml`
`es`, `es-bo`, `es-cl`, `es-co`, `es-cr`, `es-do`, `es-ec`, `es-sv`, `es-gt`, `es-hn`, `es-mx`, `es-ni`, `es-pa`, `es-py`, `es-pe`, `es-pr`, `es-es`, `es-uy`, `es-ve` | `spanish.xml`
`et` | `estonian.xml`
`eu` | `basque.xml`
`exy` | `extremaduran.xml`
`fa` | `farsi.xml`
`fi` | `finnish.xml`
`fr`, `fr-be`, `fr-ca`, `fr-fr`, `fr-lu`, `fr-mc`, `fr-ch` | `french.xml`
`fur` | `friulian.xml`
`ga` | `irish.xml`
`gl` | `galician.xml`
`gu` | `gujarati.xml`
`he` | `hebrew.xml`
`hi` | `hindi.xml`
`hr` | `croatian.xml`
`hu` | `hungarian.xml`
`id` | `indonesian.xml`
`it`, `it-ch` | `italian.xml`
`ja` | `japanese.xml`
`ka` | `georgian.xml`
`kab` | `kabyle.xml` (spelling fixed to `kab` in v8.7.5; must use `keb` instead of `kab` in v8.7.4 and earlier)
`kk` | `kazakh.xml`
`kn` | `kannada.xml`
`ko`, `ko-kp`, `ko-kr` | `korean.xml`
`ku` | `kurdish.xml`
`ky` | `kyrgyz.xml`
`lb` | `luxembourgish.xml`
`lij` | `ligurian.xml`
`lt` | `lithuanian.xml`
`lv` | `latvian.xml`
`mk` | `macedonian.xml`
`mn` | `mongolian.xml`
`mr` | `marathi.xml`
`ms` | `malay.xml`
`ne`, `nep` | `nepali.xml`
`nl`, `nl-be` | `dutch.xml`
`nn` | `nynorsk.xml`
`no`, `nb` | `norwegian.xml`
`oc-aranes` | `aranese.xml`
`oc` | `occitan.xml`
`pa`, `pa-in` | `punjabi.xml`
`pl` | `polish.xml`
`pt-br` | `brazilian_portuguese.xml`
`pt`, `pt-pt` | `portuguese.xml`
`ro`, `ro-mo` | `romanian.xml`
`ru`, `ru-mo` | `russian.xml`
`sc` | `sardinian.xml`
`sgs` | `samogitian.xml`
`si` | `sinhala.xml`
`sk` | `slovak.xml`
`sl` | `slovenian.xml`
`sq` | `albanian.xml`
`sr-cyrl-ba`, `sr-cyrl-sp` | `serbianCyrillic.xml`
`sr` | `serbian.xml`
`sv` | `swedish.xml`
`ta` | `tamil.xml`
`te` | `telugu.xml`
`tg-cyrl-tj` | `tajikCyrillic.xml`
`th` | `thai.xml`
`tl` | `tagalog.xml`
`tr` | `turkish.xml`
`tt` | `tatar.xml`
`ug-cn` | `uyghur.xml`
`uk` | `ukrainian.xml`
`ur`, `ur-pk` | `urdu.xml`
`uz-cyrl-uz` | `uzbekCyrillic.xml`
`uz` | `uzbek.xml`
`vec` | `venetian.xml`
`vi`, `vi-vn` | `vietnamese.xml`
`yue` | `hongKongCantonese.xml`
`zh-tw`, `zh-hk`, `zh-sg` | `taiwaneseMandarin.xml`
`zh`, `zh-cn` | `chineseSimplified.xml`
`zu`, `zu-za` | `zulu.xml`
    {{< /details >}}
* `-n`: Scroll to indicated line (*LineNumber*) on `filepath`.
* `-c`: Scroll to indicated column (*ColumnNumber*) on `filepath`.
* `-p`: Scroll to indicated 0 base position (*Position*) on `filepath`.
* `-x`: Move Notepad++ to indicated left side position (*LeftPos*) on the screen.
* `-y`: Move Notepad++ to indicated top position (*TopPos*) on the screen.
* `-monitor`: Open file with [file monitoring](../views/#live-file-monitoring) enabled.
* `-nosession`: Launch Notepad++ without previous session.
* `-notabbar`: Launch Notepad++ without tabbar.
* `-ro`: Make the `filepath` read only.
* `-systemtray`: Launch Notepad++ directly in [system tray](../user-interface/#system-tray).
* `-loadingTime`: Display Notepad++ loading time.
    - Starting in v8.6.1, it shows millisecond precision using the `##:##:##.###` (hour:minute:second.millisecond) format.  It separates the loading time into Notepad++ initialization, plugins loading time, session loading time, command-line-parameter parsing time, and the total loading time.
    - In v8.6 or earlier, it just showed the total number of seconds for Notepad++ to load, without millisecond precision and without the listing of the times for individual loading stages.
* `-alwaysOnTop`: Make Notepad++ always on top.
* `-openSession`: Open a session. `filepath` must be a session file.
* `-r`: Open files recursively. This argument will be ignored if `filepath` contain no wildcard character.
* `-qn="Easter Egg Name"`: Launch [ghost typing](../ghost-typing/) to display easter egg via its *Easter Egg Name*.
* `-qt="Text to Type"`: Launch [ghost typing](../ghost-typing/) to display a text via the given *Text to Type*.
* `-qf="D:\path to\file"`: Launch [ghost typing](../ghost-typing/) to display a file content via the file path *D:\path to\file*.
* `-qSpeed(1|2|3)`: [Ghost typing](../ghost-typing/) speed. Value from 1 to 3 for slow, fast, and fastest.
* `-quickPrint`: Print the file given as argument `filepath` then quit Notepad++.
* `-settingsDir="d:\your settings dir\"`: Override the default settings dir.
* `-openFoldersAsWorkspace`: Any folders listed as arguments will be opened as a workspace, rather than opening all the contained files individually.
* `-titleAdd="additional title bar text"`: Add a dash and a space and the supplied text to the right side of the application title bar (new to v8.0.0).
* `-pluginMessage="text for plugin(s)"`: If plugin developers need extra command line arguments, then users can add this option, and the plugin will be [notified](../plugin-communication/#NPPN_CMDLINEPLUGINMSG "NPPN_CMDLINEPLUGINMSG") that it can parse that string for extra information (new to v8.4.2).
    - You can only give Notepad++ _one_ `-pluginMessage` argument.  If you have multiple pieces of information you want to pass to one or more plugins, they have to be joined together, such as, `-pluginMessage="arg1=Val1;arg2=Val2"`, and the plugin has to know how to split the contents of that message into the pieces that the plugin needs.
* `filepath`: File or folder name to open (absolute or relative path name).

The order of the options is not important.  Brackets indicate that the options
are not required, and are _not_ part of the command-line argument.  The number
of hyphens is significant, and the options are case sensitive.

For compatibility, Notepad++ will first try to identify the entire command line
as a filename, even if it is unquoted. It is however not recommended to do this,
as you should always quote the filename.

This help usage list can be accessed inside Notepad++ using the `--help` command
line argument, or using the **?**-menu's **Command Line Arguments** entry.


### Additional Options

There are other Notepad++ command-line options which aren't included in the help
usage list.  These are intended for advanced usage or other special circumstances.

* `-notepadStyleCmdline`: When you follow the instructions in
  [Other Resources > Notepad Replacement](../other-resources/#notepad-replacement),
  to replace Windows' builtin `notepad.exe` with Notepad++, Windows will try to pass `/p` or `/P` as
  a command-line option when you try to print the file from the Explorer Context menu.
  Enabling this option allows Notepad++ to recognize that option, and convert it internally
  to the official `-quickPrint` option.
* `-z`: Causes Notepad++ to ignore the next command line argument (a single word, or a phrase in quotes).
    - The only intended and supported use for this option is for the [Notepad Replacement](../other-resources/#notepad-replacement) syntax.  Any other use for this option is unsupported and not guaranteed to work.
    - There can only be one `-z` per command-line, because that is all that is required for [Notepad Replacement](../other-resources/#notepad-replacement).

## Installer Options

The Notepad++ [installer executable](../getting-started/#install-notepad-using-the-installer) accepts the [three NSIS command-line options](https://nsis.sourceforge.io/Which_command_line_parameters_can_be_used_to_configure_installers):

- `/S` : Enables silent installation.
- `/NCRC`: Skips the installer's CRC check.
- `/D=c:\blah` or `/D=c:\path with spaces\blah` : Overrides the default installation directory.
    - Do _not_ put quotes around the path, even when there are spaces.
    - Because it allows spaces in the path, this option **must** be the last argument on the installer command line, if included.

It also implements additional Notepad++\-specific options:

- `/noUpdater`: Disables the N++ inherent automatic updates (it does not install the WinGUP & PluginsAdmin updating components).
- `/closeRunningNpp`: Will (try to) close existing Notepad++ before installing the new version.  (New to v8.6.9.)
    - It will first try a "nice" close request (using [WM_CLOSE](https://learn.microsoft.com/en-us/windows/win32/winmsg/wm-close)).
    - If the "nice" request wasn't successful after 5 seconds, it will kill the underlying process.
    - If Notepad++ has multiple instances opened, it will close all instances.
- `/runNppAfterSilentInstall`: After a silent install, it will automatically run the newly-installed Notepad++. (New to v8.6.9.)
    - Only works if `/S` is also specified.
- `/relaunchNppAfterSilentInstall`: If Notepad++ was running when silent install was initiated, it will automatically run the newly-installed Notepad++ after installation is complete. (New to v8.8.2.)
    - Only works if `/S` is also specified.

*Note* : The installer options are case sensitive: `/S` will do a silent installation, whereas `/s` will _not_.
