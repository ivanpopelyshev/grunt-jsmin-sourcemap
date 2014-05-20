# Fork of [grunt-jsmin-sourcemap](https://github.com/twolfson/grunt-jsmin-sourcemap)

## Synopsis
[Grunt](https://github.com/gruntjs/grunt/) is a node.js based CLI build tool.

[JSMin](http://www.crockford.com/javascript/jsmin.html) is a JavaScript minifier that removes whitespace and comments.

[Source maps](http://www.html5rocks.com/en/tutorials/developertools/sourcemaps/) enables developers to view and interact with minified JavaScript as if it were unminified (providing useful line errors and easier debugging).

My point is that *.dev.js file enables developers to add original scripts dynamically in dev mode. That's better than sourcemaps in a few ways.

## Documentation

```js
grunt.initConfig({
'jsmin-sourcemap': {
		all: {
			src: ['js/script1.js', 'js/script2.js', 'js/lib/library1.js'],
			dest: 'target-script.js',
			destMap: 'target-script.min.js.map',
			destScript: 'target-script.dev.js'
		}
	}
})
```

target-script.dev.js :

```js
<script src='js/script1.js'></script>
<script src='js/script2.js'></script>
<script src='js/library1.js'></script>
```

When you combine all three of these, you get a grunt plugin that is your new best debugging friend.

## Demos
The demos in the [node-jsmin-sourcemap](https://github.com/twolfson/node-jsmin-sourcemap), what makes this tick, are hosted on Plunker for your testing and enjoyment.

- Basic [http://embed.plnkr.co/mGHUpe](http://embed.plnkr.co/mGHUpe)
- jQuery [http://embed.plnkr.co/JyNn5e](http://embed.plnkr.co/JyNn5e)
- Multi [http://embed.plnkr.co/FPkQx6](http://embed.plnkr.co/FPkQx6)

## Getting Started
Add  this line into your package.json dependencies section

```js
"grunt-jsmin-sourcemap": "git://github.com/ivanpopelyshev/grunt-jsmin-sourcemap"
```

## License
As of Dec 05 2013, Todd Wolfson has released grunt-jsmin-sourcemap and its contents to the public domain.

It has been released under the [UNLICENSE][].

[UNLICENSE]: UNLICENSE
