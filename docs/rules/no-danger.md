# Prevent usage of dangerous JSX properties (no-danger)

Dangerous properties in React are those whose behavior is known to be a common source of application vulnerabilities. The properties names clearly indicate they are dangerous and should be avoided unless great care is taken.

See https://facebook.github.io/react/tips/dangerously-set-inner-html.html

## Rule Details

The following patterns are considered warnings:

```js
var React = require('react');

var Hello = <div dangerouslySetInnerHTML={{ __html: "Hello World" }}></div>;
```

The following patterns are not considered warnings:

```js
var React = require('react');

var Hello = <div>Hello World</div>;
```

## When Not To Use It

If you are certain the content passed to dangerouslySetInnerHTML is sanitized HTML you can disable this rule.
