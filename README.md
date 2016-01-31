# aimer [![NPM version](https://img.shields.io/npm/v/aimer.svg)](https://npmjs.com/package/aimer) [![NPM downloads](https://img.shields.io/npm/dm/aimer.svg)](https://npmjs.com/package/aimer) [![Build Status](https://img.shields.io/circleci/project/egoist/aimer/master.svg)](https://circleci.com/gh/egoist/aimer)

> Remote web content crawler done right.

## Motivation

Sometime I want grab some nice images from a url like http://bbs.005.tv/thread-492392-1-1.html, so I made this little program to combine `node-fetch` and `cheerio` to make my attempt fulfilled.

## Install

```
$ npm install --save aimer
```

## Usage

```js
const aimer = require('aimer')

aimer('http://some-url.com/a/b/c')
	.then($ => {
		$('img.nice-images').each(function () {
			const url = $(this).attr('src')
			console.log(url)
		})
	})
```

## API

### aimer(url, opts)

**opts**

[cheerio](https://github.com/cheeriojs/cheerio) options.

## License

MIT © [EGOIST](https://github.com/egoist)