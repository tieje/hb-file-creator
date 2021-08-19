# hb-file-creator

`hb <holberton_project_url>`

This project creates files for holberton projects in your current directory.
The first argument needs to the url of the project.

##Installation

1. Run `pip3 install selenium`

2. Type your email and password used for your holberton login in the `login-info.json` file

3. Download [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/) that matches your version of chrome browser \(Options > Help > About Chrome\).
#### Move chromedriver to this folder

## Create an alias

### For Linux

Edit and run the following:

`printf "alias hb=\'python3 /path/to/hb-scraper.py \"\$PWD\"'\n" >> "$HOME"/.bashrc`
### For M1 Mac

Edit and run the following:

`printf "alias hb=\'python3 /path/to/hb-scraper.py \"\$PWD\"'\n" >> "$HOME"/.zshrc` 

For reference check out [MyAlias](https://github.com/tieje/MyAliases) repo.
### For Windows

Maybe I'll put this in someday.

## Troubleshooting

For mac users, you might have additional chrome browsers running in the background, especially if headless is False. Unfortunately, you'll need to close them yourself.

- If it's not working, try changing the headless option on line 28 to `False`. This used to happen on Windows but hopefully Selenium fixed it since the last time I used it.
- The chromedriver version does not need to be exact but it needs to be "close enough"
