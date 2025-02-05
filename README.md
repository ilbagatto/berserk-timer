```
███   ▄███▄   █▄▄▄▄   ▄▄▄▄▄   ▄███▄   █▄▄▄▄ █  █▀
█  █  █▀   ▀  █  ▄▀  █     ▀▄ █▀   ▀  █  ▄▀ █▄█
█ ▀ ▄ ██▄▄    █▀▀▌ ▄  ▀▀▀▀▄   ██▄▄    █▀▀▌  █▀▄
█  ▄▀ █▄   ▄▀ █  █  ▀▄▄▄▄▀    █▄   ▄▀ █  █  █  █
███   ▀███▀      █             ▀███▀     █     █
                ▀                       ▀     ▀

             █▄
           ▄     █▀▄▀█
       ▄▄▄▀▀ ▄█  █ █ █  ▄███▄   █▄▄▄▄
    ▀▀▀ █    ██  █ ▀ █  █▀   ▀  █  ▄▀
        █    ██  █   █  ██▄▄    █▀▀█▌
       █     ▐█      █  █▄   ▄▀ █   █
      ▀       ▐     ▀   ▀███▀      █
                                 ▀

```

# Berserk Timer 1.0.0

Berserk Timer – a CLI timer with witness mode, and flexible duration input.
The goal was to create a simple Windows CLI timer that asks you what were you doing for the last N-minutes. I couldn't find any free tool that suits my needs: flexibility, simplicity and no-adds in one. That's why I decided to create Berserk Timer. It helps me managing my time a lot so I decided to share it.

The tool provides:

- **CLI support**.
- **Customizable timers** with presets, and _witness_ mode.
- **Easy logging** for your activities.
- **Quick access** via the `brsrk` command, which can be used from any directory.

I hope this tool will make it easier for others to track time and stay productive. Enjoy Berserk Timer and feel free to contribute!

## Features

- **Flexible Duration Input:**
  - By default, the duration is entered in minutes (either whole or fractional, e.g., `1.5` means 1 minute 30 seconds).
  - The `--seconds` flag allows you to input the duration in seconds.
- **Presets:**
  Use the flags `-x`, `-s`, `-m`, `-l`, `-X`, or `-t` to select predefined durations (in minutes). You can add the presets into config.json
- **Witness Mode:**
  After the timer finishes (whether it was paused, quit, or stopped in another way), the user will be asked the question "What were you doing?" – you can enter text in any language (or type 'skip' to cancel) and in the end of the week there are a list of your activities for each day and hour.
- **Interfaces:**
  Both CLI and GUI modes are supported, but I personally prefer to use CLI whenerever it is possible, so GUI is still very experimental and rude. Use the `-g` flag to start the graphical interface for your own risk.
- **Logging:**
  All events are recorded in the `logs` folder:
  - Main log – `logs/berserk.log`
  - Witness mode responses – `logs/witness_log_YYYY-MM-DD.txt`

## Running

### Windows

From the root directory, run:

- Example: 1.5 minutes (i.e., 1 minute 30 seconds):

  ```cmd
  python -m src.main 1.5
  ```

  or just run `brsrk` command.

### Linux

From the root directory, run:

- Example: 1.5 minutes (i.e., 1 minute 30 seconds):

  ```bash
  python3 -m src.main 1.5 "$@"
  ```

  or just run `brsrk` command.

### MacOS
From the root directory, run:

- Example: 1.5 minutes (i.e., 1 minute 30 seconds):

  ```bash
  python3 -m src.main 1.5 "$@"
  ```

  or just run `brsrk` command.

