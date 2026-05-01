# Alfred Workflows

A small collection of Alfred workflows for macOS.

These workflows were made for Alfred, but some of the ideas and command surfaces were inspired by open-source Raycast extensions. This repository is not affiliated with Raycast, Alfred, Bob, Tana, Ghostty, Jina AI, or yt-dlp.

## Workflows

### Bob Control

Control the [Bob](https://bobtranslate.com/) translation app from Alfred.

Actions include:

- Input to Translate
- Translate Clipboard
- Capture Text with OCR
- Capture Text Silently with OCR
- Capture File's Text from Finder
- Translate Selected
- Translate Captured
- Show Translate Window
- Show OCR Window

Requirements:

- Alfred
- Bob 1.5.0 or later

Keyword:

```text
bob
```

### Terminal Finder for Ghostty

Move quickly between Finder, clipboard paths, and terminal apps.

The default terminal is Ghostty, but the workflow also supports Terminal, iTerm, Warp, WezTerm, kitty, and cmux.

Commands:

- `tf`: choose a route from a menu
- `f2t`: open the current Finder or Path Finder location in the default terminal
- `t2f`: open the current terminal directory in Finder
- `c2t`: open the clipboard path in the default terminal

Requirements:

- Alfred
- macOS Automation permissions for Alfred when prompted
- Ghostty or another supported terminal app

### Tana Paste

Convert Markdown from the clipboard into [Tana Paste](https://tana.inc/) format.

Behavior:

- Adds the `%%tana%%` header
- Converts Markdown headings to Tana heading nodes with `!!`
- Converts Markdown lists and paragraphs to Tana nodes
- Converts Markdown italic markers to Tana-style double underscores
- Preserves Markdown bold markers
- Copies the converted output back to the clipboard

Keyword:

```text
tana
```

Requirements:

- Alfred
- Tana, if you want to paste the converted output directly into Tana

### Webpage to Markdown

Convert a public webpage to Markdown through Jina Reader, save the result as a `.md` file, and copy the Markdown to the clipboard.

Commands:

- `mdurl <URL>`: convert the URL you type
- `mdclip`: convert the URL currently in the clipboard

Options are configurable in Alfred workflow variables:

- `include_metadata`
- `prepend_front_matter`
- `include_links_summary`
- `jina_api_key`
- `output_folder`

Privacy note: this workflow sends the target URL to Jina Reader for conversion.

### Video Downloader

Download videos, extract MP3 audio, or save transcripts through `yt-dlp`.

Requirements:

- Alfred
- `yt-dlp`
- `ffmpeg`

Install command-line dependencies with Homebrew:

```bash
brew install yt-dlp ffmpeg
```

Keyword:

```text
vd
```

Please use this workflow only for content you have the right to download and in accordance with each site's terms.

### Currency Exchange

Convert between currencies from Alfred using public exchange-rate data.

Examples:

```text
fx 100 usd eur
fx 100美元 人民币
fx 250 eur to gbp
```

The workflow supports common English and Chinese currency aliases and caches recent exchange-rate responses briefly.

## Installation

Download the `.alfredworkflow` file you want from the [`workflow`](workflow/) folder and open it with Alfred.

If macOS asks for Automation or Accessibility permissions, allow Alfred to control the relevant apps. Some workflows need this to read Finder windows, operate terminal apps, or trigger app-specific actions.

## Acknowledgements

These workflows were built as Alfred-native implementations inspired by the following Raycast extensions:

- Bob Control was inspired by Raycast's Bob extension: <https://github.com/raycast/extensions/tree/870667fc671801a467deb7c4c7fc72992efe3820/extensions/bob/>
- Tana Paste was inspired by Raycast's Tana Paste extension: <https://github.com/raycast/extensions/tree/b8c8fcd7ebd441a5452b396923f2a40e879565ba/extensions/tana-paste/>
- Terminal Finder for Ghostty was inspired by Raycast's Terminal Finder extension: <https://github.com/raycast/extensions/tree/186d955eda64f9e956b25a3fdf5566b1d38f57f2/extensions/terminalfinder/>

The Raycast extensions repository is open source under the MIT License. This repository keeps the attribution explicit because the original Raycast workflows shaped the feature choices and interaction design.

## License

MIT License.
