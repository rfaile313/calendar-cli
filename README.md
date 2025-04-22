# Calendar CLI

A command-line tool for adding events to macOS Calendar using natural language.

## Overview

Calendar CLI allows you to quickly add events to your macOS Calendar directly from the terminal using natural language descriptions. No need to open the Calendar app or use a specific date/time format.

## Features

- Natural language date/time parsing
- Support for recurring events
- Support for all-day events
- Intelligent title extraction
- Test mode to preview event details

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/rfaile313/calendar-cli.git
   cd calendar-cli
   ```

2. Install the required dependency:
   ```bash
   pip3 install dateparser
   ```

3. Make the script executable:
   ```bash
   chmod +x add_event
   ```

4. Add to your PATH (optional):
   ```bash
   # Add this line to your .bashrc, .zshrc, or equivalent
   export PATH="$PATH:/path/to/calendar-cli"
   ```

I personally prefer to symlink `add_event` to `/usr/local/bin` which is already in my path :) 

## Usage

```bash
add_event "Your event description with date/time"
```

### Examples

```bash
add_event "team meeting tomorrow at 2pm"
add_event "dentist appointment on Friday at 10am"
add_event "kids birthday may 18th"
add_event "vacation next week"
```

### Test Mode

To preview how an event will be parsed without adding it to your calendar:

```bash
add_event --test "team meeting tomorrow at 2pm"
```

## Integration with icalBuddy

This tool pairs well with `icalBuddy` to display the day's events in your terminal: https://github.com/ali-rantakari/icalBuddy

You can install icalBuddy with Homebrew:

```bash
brew install ical-buddy
```

Then add something like this to your shell configuration:

```bash
# Show today's calendar events when opening terminal
icalBuddy -sd eventsToday
```

## Requirements

- macOS with Calendar app
- Python 3
- dateparser library (`pip3 install dateparser`)

## Author

[rfaile313](https://github.com/rfaile313)
