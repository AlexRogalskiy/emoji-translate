## emoji-translate

You know how sometimes you type English and it has all these letters and words and no emoji? Yeah, emoji-translate fixes that.

## Packaged demos
![omg emoji](https://cloud.githubusercontent.com/assets/1369170/8635052/e333474e-27c7-11e5-8af8-5b0bc2281095.gif)

This is what you actually want, right? Can't blame you. [Here](http://meowni.ca/emoji-translate) you go. 👏

There's also a Chrome  [extension](https://chrome.google.com/webstore/detail/emoji-translate/kkkfndlpdajmbgofkidemhkjoinhmojl) that lets you translate any page on the internet to emoji. Your nightmares are finally over.

## Emoji-translate as a library
You can also use this as a standalone library for your own translation purposes.

### Install
```
npm install emoji-translate
```

### Usage
```
translate = require('emoji-translate');
```

The `emoji-translate` api has 5 methods:

module.exports.isMaybeAlreadyAnEmoji = isMaybeAlreadyAnEmoji;
module.exports.getAllEmojiForWord = getAllEmojiForWord;
module.exports.getEmojiForWord = getEmojiForWord;
module.exports.translateForDisplay = translateForDisplay;
module.exports.translate = translate;
  * `isMaybeAlreadyAnEmoji` -- returns true if a character is very likely already an emoji (i.e. it exists as a key in `emojilib`)
  * `getAllEmojiForWord(word)` -- returns a list of possible emoji translations
  * `getEmojiForWord(word)` -- returns a random translation from the list
  returned by `getAllEmojiForWord(word)`
  * `translate(chunk, onlyEmoji)` -- returns a translation of the whole chunk of text. If `onlyEmoji` is true, then the untranslatable words are removed.
  * `translateForDisplay` -- calls `translate` but returns a `<span>` element that contains either the original word, or the emoji translation, ready for display (either as a span, or a `<select>` if multiple translations are
  available).

## 💪
This was made as part of an ⚡️emoji hackday⚡️ and  is powered by [emojilib](https://github.com/muan/emojilib), a magical `json` file of emoji names and keywords y'all should use in all your projects.
