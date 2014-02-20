*This repository is a mirror of the [component](http://component.io) module [component/join](http://github.com/component/join). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/component-join`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*

# join

  Join a list in a nice human friendly way.

## Installation

    $ component install component/join

## API

   - [join(arr)](#joinarr)
   - [join(arr, str)](#joinarr-str)
   - [join(arr, str) with Oxford comma](#joinarr-str-with-oxford-comma)
<a name=""></a>

<a name="joinarr"></a>
# join(arr)
should default to "and".

```js
join(['foo', 'bar']).should.equal('foo and bar');
```

<a name="joinarr-str"></a>
# join(arr, str)
should join.

```js
join([], 'and').should.equal('');
join(['foo'], 'and').should.equal('foo');
join(['foo', 'bar'], 'and').should.equal('foo and bar');
join(['foo', 'bar', 'baz'], 'or').should.equal('foo, bar or baz');
```

<a name="joinarr-str-with-oxford-comma"></a>
# join(arr, str) with Oxford comma
should remove comma with less than 3 items.

```js
join([], ', or').should.equal('');
join(['foo'], ', or').should.equal('foo');
join(['foo', 'bar'], ', or').should.equal('foo or bar');
```

should join with 3 or more items.

```js
join(['foo', 'bar', 'baz'], ', and').should.equal('foo, bar, and baz');
```

## License

  MIT
