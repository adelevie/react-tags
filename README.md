# react-tags

A simple wrapper around `React.DOM`. 

Write `a({href: 'http://github.com'}, 'hello')` instead of `React.DOM.a({href: 'http://github.com'}, 'hello')`.

Experimental.

Synopsis:

```javascript
var React = require('React');
var SiteBoilerPlate = require('../core/SiteBoilerPlate.js'); // customize
require('react-tags').pollute(this, React);  // explicitly pollute scope with tags

var content = function() {
  return div({}, 
    p({}, "A paragraph!"),
    ul({}, 
      li({}, "one"),
      li({}, "two"),
      li({}, a({href: "http://github.com"}, "three"))
    ),
    div({}, 
      h3({}, "Hello world"),
      p({}, "some content")
    )
  );
};

var hello = React.createClass({
  render: function() {
    return SiteBoilerPlate({
      children: content()
    });
  }
});
```

For a non-React flavor of this library, check out [`wut`](http://github.com/adelevie/wut).