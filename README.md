# i18n-translate React Edition

Forked from [thomasbrueggemann/i18n-translate](https://github.com/thomasbrueggemann/i18n-translate)


Automatically translates react i18n javascript files into different languages via Google Translate API.

## Installation

```
npm install  --save https://github.com/rrrhys/i18n-translate/tarball/master -g
```

## Usage

You need a [Google Translate API Key](https://cloud.google.com/translate/).

```
i18n-translate apiKey startDir sourceLang targetLang1,targetLang2,.. (file1,file2,..)
```

e.g.

```
i18n-translate AIzaSyAeAABCDEFGyourapikeyQUxjMlLwuLGrKY i18n en en,fr,de
```

This would translate all the *.js files in ./i18n (relative to current folder in the shell) to translate from English to English, French and German, based on the Google Translate API language codes (We leave English in so the location of language files is consistent)

A sample language file (in ./i18n/lang.js, according to above example) looks like this:
```
export default {
	"root": {
		"pay": "Pay",
		"choosePaymentMethod": "Choose a payment method.",
	},
	"de": true,
	"en": true,
	"fr": true
};
```

Sample output would look like this (written to i18n/de/lang.js in above example):

```
export default {
	"pay": "Zahlen",
	"choosePaymentMethod": "Wählen Sie eine Bezahlungsart.",
};
```
