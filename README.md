# Slack dark theme injector tool
This tool writes a dark theme to the Slack desktop application.
Dark theme was taken from the generated [Dark Reader](https://darkreader.org)
theme that was applied when I visited the web version of slack, like so:
```
Array.from(document.querySelectorAll('.darkreader')).map((n) => n.textContent).join('\n');

```

### Prerequisites

Install [python](https://www.python.org/)

You _really_ should take the css file from this site, and host it somewhere _you_ control. It's
not a great idea to have a script inject an arbitrary CSS file from a domain outside of your control,
into an application like Slack that could have sensitive data.

Don't trust me - fork the repo.

### Running

Unix
```bash
sudo python makeitdark.py
```
```bash
sudo python3 makeitdark.py
```

Windows
```bash
python makeitdark.py
```
### Sidebar

Use the following custom Slack sidebar theme to make it consistent:
```
#000000,#000000,#00ff00,#00ff00,#00ff00,#00ff00,#31f700,#ff0000
```

Or use this one which kinda makes it look like Mojave dark mode, from [slackthemes.net](https://slackthemes.net):
```
#333336,#2e2e31,#666668,#ffffff,#277df6,#d7d5d4,#277df6,#277df6
```

### Reverting

If you want to uninstall the dark Slack theme you can run with the `makeitlight` option:
```
makeitdark.py makeitlight
```
