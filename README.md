<h1 align=center>Journey</h1>
<p align=center>
  <img src="https://img.shields.io/badge/OS-linux-orange.svg?style=flat-square">
</p>

>  Persist

Track Days automatically for `X` days of `Y` challenges

>  Make sure to install dependencies
> install `gum` "https://github.com/charmbracelet/gum?tab=readme-ov-file#installation"

## Installation

```bash
git clone https://github.com/Singularity0x00/Journey.git
cd Journey
chmod +x journey

#INSTALL FOR USER
cp journey ~/.local/bin/

# INSTALL GLOBALLY
sudo cp journey /usr/bin/
```

## Instruction

```bash
journey <days> <Challenge>
#OR
journey
```

This will create a config file at `$HOME/.config/countdown/`

#### To view tracker

```bash
journey -o
```

> Add `journey -o` to shell config like `.bashrc` or `config.fish` to show tracker whenever terminal opens.

### Customisation

This script takes colors from pywal `.cache/wal` directory if it exists.
Otherwise feel free to change colors to your liking in `print_default()` function

```bash
print_default() {
    X=$(gum style \
      ....\
      --foreground "#f38ba8" \
      --border-foreground "#7287fd" \
      ...\
  )
    Y=$(gum style \
      .....\
      --foreground "#7287fd" \
      --border-foreground "#f38ba8" \
      ....\

```

## Troubleshooting

Deleting `.config/countdown/countdown.conf` will fix most issues and can be written to manually.
