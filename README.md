# @advertol/control-element-classes

[![Build Status][ci-img]][ci] [![BrowserStack Status][browserstack-img]][browserstack]

Add HTML classes to zone DOM elements based on zone state.

## Install

```sh
npm install @advertol/control-element-classes --save
```

## Usage

```js
import advertol from '@advertol/core';
import ElementClassesControl from '@advertol/control-element-classes';

const instance = advertol({
	// …
	control: [
		new ElementClassesControl({
			isHidden: 'is-hidden',
			isLoaded: 'is-loaded',
			isEmpty: 'is-empty'
		})
	]
});

instance.resolve();
```

## API

### elementClassesControl(classes)

#### classes

Type: `Object`

HTML classes to apply on zone DOM element based on current state.

| Property | Type | Description |
| --- | --- | --- |
| `isHidden` | `string` | HTML class when zone is hidden. |
| `isLoaded` | `string` | HTML class when zone is loaded. |
| `isEmpty` | `string` | HTML class when zone is empty. |

## Browser support

Tested in IE9+ and all modern browsers, assuming `Element.prototype.classList` is available.

## Test

For automated tests, run `npm run test:automated` (append `:watch` for watcher support).

## License

MIT © [Ivan Nikolić](http://ivannikolic.com)

[ci]: https://travis-ci.com/niksy/advertol-control-element-classes
[ci-img]: https://travis-ci.com/niksy/advertol-control-element-classes.svg?branch=master
[browserstack]: https://www.browserstack.com/
[browserstack-img]: https://www.browserstack.com/automate/badge.svg?badge_key=UnJSTkFwM2hQUERjcUEyeFpFRCsxYkZKcStGRW5pVjVUNHZMV0NqdHhwTT0tLWg3VmVKd21CSmlMMmk3aVRTNHliTEE9PQ==--fd9507488539f9e39711098948279e659d3d73ad
