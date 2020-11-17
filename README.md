# mud's secret rice stash

A collection of my personal web/browser tweaks, feel free to use and change anything.<br>
I use Firefox, so things will probably break in a disastrous way when using other browsers.

### 「 Other useful things and tips 」

#### Actually transparent background when viewing images in FF
[userContent.css](http://kb.mozillazine.org/index.php?title=UserContent.css)
```css
@namespace url("http://www.w3.org/1999/xhtml");
body > img.transparent { 
  background: transparent !important 
  }
```

#### Changing the [preferred color scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme) used on webpages indepedent from OS/User agent settings
about:config > add new property called "ui.systemUsesDarkTheme" > set to *number* 1, boolean wont't work.

#### Removing FF popup URL bar
https://github.com/WesleyBranton/Remove-Firefox-Megabar

#### Windows 10 scrollbars in FF
https://github.com/endeavoursc/firefox-overlay-scrollbars-win10
