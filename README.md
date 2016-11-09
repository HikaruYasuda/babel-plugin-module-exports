# babel-plugin-module-exports

```javascript
export const abc = 'abc'
export default {
  beef: 'beef'
}
```

Babel@6 transforms to

```javascript
'use strict';
Object.defineProperty(exports, "__esModule", {
  value: true
});
exports.abc = 'abc';
exports.default = {
  beef: 'beef'
};
```

And adding this plugin transforms to

```javascript
'use strict';
Object.defineProperty(exports, "__esModule", {
  value: true
});
exports.abc = 'abc';
exports.default = {
  beef: 'beef'
};
module.exports = exports.default
module.exports['abc'] = 'abc'
```
