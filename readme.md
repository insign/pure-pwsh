# pure-pwsh

> PowerShell implementation of the [pure prompt](https://github.com/sindresorhus/pure).

![](screenshot.svg)

## Dependencies

- Terminal with ANSI colour support
  (e.g. any modern version of Windows 10, ConEmu, Hyper, ansicon, etc.)
- PSReadLine for async prompt updates and colour scheme integration
  (tested against 2.0, should mostly work on 1.x too)
- posh-git _and_ git executable on `$env:path` for git features

## Options

Set options on the `$pure` global.

| Option                | Description                                            | Default value                                       |
| :-------------------- | :----------------------------------------------------- | :-------------------------------------------------- |
| **`PwdColor`**        | Colour of the current directory name.                  | <img src="https://placehold.it/16/0000aa?text=+" /> |
| **`BranchColor`**     | Colour of the current branch.                          | <img src="https://placehold.it/16/aaaaaa?text=+" /> |
| **`RemoteColor`**     | Colour for remote status (up and down arrows).         | <img src="https://placehold.it/16/00aaaa?text=+" /> |
| **`ErrorColor`**      | Colour for the error prompt and long running commands. | <img src="https://placehold.it/16/aa0000?text=+" /> |
| **`PromptColor`**     | Colour for the main prompt.                            | <img src="https://placehold.it/16/aa00aa?text=+" /> |
| **`PromptChar`**      | Prompt character.                                      | `❯`                                                 |
| **`UpChar`**          | Up arrow.                                              | `⇡`                                                 |
| **`DownChar`**        | Down arrow.                                            | `⇣`                                                 |
| **`SlowCommandTime`** | Timespan beyond which a command is considered 'slow'.  | `00:00:05`                                          |
| **`FetchInterval`**   | Interval to check remote for updates. (0 to disable.)  | `00:05:00`                                          |

## Installation

Install from the [gallery](https://www.powershellgallery.com/packages/pure-pwsh) or clone this repository:

```shell
Install-Module pure-pwsh
```

and import it in your profile _after_ posh-git:

```shell
Import-Module pure-pwsh
```

# Not currently included

- Does not display username and host for remote sessions
- Does not set window title
- No vi mode indicator
