# Gruvbox colorscheme for tmux

Retro groove colorscheme for [tmux](https://github.com/tmux/tmux), based on the excellent [gruvbox](https://github.com/morhetz/gruvbox) theme for vim.

![](https://files.catbox.moe/e8utrq.jpg)

![](https://files.catbox.moe/cmh8tl.jpg)

This is a modified fork of [tmux-gruvbox-truecolor](https://github.com/LawAbidingCactus/tmux-gruvbox-truecolor).

## Installation

### Manual

Just clone this repo and add `tmux-colorscheme.conf` to your `.tmux.conf`:

```bash
cat tmux-colorscheme.conf >> ~/.tmux.conf
```

Or move `tmux-colorscheme.conf` to your home directory and source it in `.tmux.conf`:

```tmux
source-file ~/tmux-colorscheme.conf
```

### Tmux Plugin Manager

Add this repo to the list of [TPM](https://github.com/tmux-plugins/tpm) plugins in your `.tmux.conf`:

```tmux
set -g @plugin 'ndpm13/tmux-gruvbox-truecolor'
```

Press `<prefix> + I` to reload tmux with the plugin.

## Troubleshooting

### tmux's colors look weird

Try adding the following to your `.tmux.conf`:

```tmux
set-option -as terminal-overrides ",xterm*:RGB"
```

### Pane separator lines look weird

Something isn't correctly handling UTF-8 line drawing characters.
