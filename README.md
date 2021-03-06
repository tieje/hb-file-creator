# hb-file-creator

## Command line usage:

`hb <holberton_project_url>`

This project creates files for holberton projects in your current directory.
The first argument needs to be the url of the project.

## Installation

1. Run `pip3 install selenium`

2. Type your email and password used for your holberton login in the `login-info.json` file

3. Download [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/) that matches your version of chrome browser \(Options > Help > About Chrome\).
### Move chromedriver to this folder

## Create an alias

### For Linux

Edit the `path/to/` part of the following command and run it:

`printf "alias hb=\'python3 /path/to/hb-scraper.py \"\$PWD\"'\n" >> "$HOME"/.bashrc`

### For M1 Mac

Edit the `path/to/` part of the following command and run it:

`printf "alias hb=\'python3 /path/to/hb-scraper.py \"\$PWD\"'\n" >> "$HOME"/.zshrc` 

Unfortunately, you'll need to delete the `\` after `hb=` I can't get around this.
For reference check out [MyAlias](https://github.com/tieje/MyAliases) repo.

### For Windows

Maybe I'll put this in someday.

## Troubleshooting

Make sure that the URL you're using strictly only contains the default URL, not the containing the task:
Use: https://intranet.hbtn.io/projects/288
Don't use: https://intranet.hbtn.io/projects/288/#6872

For mac users, you might have additional chrome browsers running in the background, especially if headless is False. Unfortunately, you'll need to close them yourself.

- If it's not working, try changing the headless option on line 28 to `False`. This used to happen on Windows but hopefully Selenium fixed it since the last time I used it.
- The chromedriver version does not need to be exact but it needs to be "close enough"

## Alternatives

[keysmusician](https://github.com/keysmusician) has created a chrome extension HTML GUI alternative called [holberton-file-downloader-chrome-extension](https://github.com/keysmusician/holberton-file-downloader-chrome-extension) that basically achieves the same result with less configuration. Both methods rely on the chrome browser.
