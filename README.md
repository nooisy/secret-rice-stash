# mud's secret rice stash

A collection of my personal web/browser tweaks, feel free to use and change anything.<br>
I use Firefox, so things will probably break in a disastrous way when using other browsers.

### 「 Other useful things and tips 」

#### Actual transparent background when viewing transparent images in FF
[userContent.css](http://kb.mozillazine.org/index.php?title=UserContent.css)
```css
@namespace url("http://www.w3.org/1999/xhtml");
body > img.transparent { 
  background: transparent !important;
  }
```

#### Changing the [preferred color scheme](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme) used on webpages indepedent from OS/User agent settings
about:config > add new property called "ui.systemUsesDarkTheme" > set to *number* 1, boolean wont't work.

#### Overflow menu tweaks
Horizontal overflow menu with buttons, no text:<br>
https://github.com/TinyRaindrop/Firefox-UI-customization/blob/master/Navbar/overflow_menu_horizontal.css<br>

Some add-ons are too wide to be displayed in the overflow menu. You can change its width like this:<br>
[userChrome.css](https://www.userchrome.org/how-create-userchrome-css.html)
```css
@namespace url("http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul");
#widget-overflow panelview {
  min-width: 710px !important;
  }
```
Let me know if there's a dynamic/responsive way.

#### Removing FF "popout" URL bar
https://github.com/WesleyBranton/Remove-Firefox-Megabar

#### Windows 10 scrollbars in FF
https://github.com/endeavoursc/firefox-overlay-scrollbars-win10

#### YT sign in popup
Add the following lines to your adblocker filter:
```js
youtube.com##+js(set, ytInitialPlayerResponse.auxiliaryUi.messageRenderers.upsellDialogRenderer.isVisible, false)
youtube.com##+js(set, ytInitialData.overlay.upsellDialogRenderer.isVisible, false)
youtube.com##+js(json-prune, [].playerResponse.auxiliaryUi.messageRenderers.upsellDialogRenderer)
youtube.com##+js(json-prune, auxiliaryUi.messageRenderers.upsellDialogRenderer)
youtube.com##+js(set, ytInitialData.topbar.desktopTopbarRenderer.interstitial.consentBumpRenderer.forceConsent, false)
youtube.com##+js(json-prune, [].response.topbar.desktopTopbarRenderer.interstitial.consentBumpRenderer)
```
