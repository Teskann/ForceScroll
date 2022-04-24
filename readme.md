# 🦊 ForceScroll

Firefox extension to automatically enable scrolling on all webpages.

[](mdtoc)
## Table of Contents

* [🖱 Why this project ?](#-why-this-project-)
* [📥 How to Get it ?](#-how-to-get-it-)
	* [✅ Official release](#-official-release)
	* [📦 Pack the Extension and Install it Yourself](#-pack-the-extension-and-install-it-yourself)
* [⚙ How it Works](#-how-it-works)
* [📖 References](#-references)
[](/mdtoc)

## 🖱 Why this project ? 

European laws force websites to ask user consent to accept cookies. If you enable
the Firefox option to delete cookies every time you close the window, the cookies
pop-ups will annoy you at every browser restart. One solution is to block these pop-ups
with an ad blocker like uBlock Origin. However, some websites disable scrolling
on their page until you accept/refuse cookies. This extension re-enables
scrolling.

## 📥 How to Get it ?

### ✅ Official release

The add-on is currently under acceptance from Mozilla team.

### 📦 Pack the Extension and Install it Yourself

Run :

```bash
./pack.sh
```

Then, check the documentation of Firefox about how to install zip extensions.

## ⚙ How it Works

The extension injects a simple script in every page to enable scrolling:

```javascript
var r = 'html,body{overflow:auto !important;}';
var s = document.createElement('style');
s.type = 'text/css';
s.appendChild(document.createTextNode(r));
document.body.appendChild(s);
void 0;
```

## 📖 References

1. [Mozilla Firefox Extensions Development](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension)
2. [Script source](https://support.mozilla.org/en-US/questions/1132323)
3. [Icon source](https://pixabay.com/vectors/scroll-parchment-paper-note-bill-35683/)