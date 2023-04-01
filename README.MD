# System Tray Menu for Windows - no dependencies

## pip install traymenu

### Tested against Windows 10 / Python 3.10 / Anaconda 

# ![](https://github.com/hansalemaos/screenshots/blob/main/traymenu.png?raw=true)

```python

from traymenu import TrayMenu,quitsystray

if __name__ == "__main__":
    # Adapted from: https://gist.github.com/jasonbot/5759510 (Python 2)
    tm = TrayMenu(
        icon=r"C:\Users\hansc\Downloads\pinpng.com-anime-girl-face-png-6144106.ico",
        functions=(
            ("Men1", lambda: print(331)),
            ("Men2", False), # not clickable
            ("!Default", lambda: print(22)), # default [bold]
            "--", # Separator
            ("Men3", lambda: print(str(1))),
            ("Quit", lambda: quitsystray()),
        ),
    )
    tm.letsgo()


```