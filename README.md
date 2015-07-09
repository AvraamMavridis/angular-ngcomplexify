# Angular ngComplexify

version 0.1

ngComplexify is a module/directive (485 bytes minified) that determines the complexity of a
give password and change the color of a css property of the input

### Installation
Download and place the script before your angular application script and after the core angular module.
```html
    <script src="angular.min.js"></script>
    <script src="angular-ngcomplexify.min.js"></script>
    <script src="yourApp.js"></script>
```
Then inject the module into your application:

```js
angular.module('yourApp',['ngComplexify']);
```

Include the `complexify` attribute directive in your password input.
e.g.
```html
<input
  type="password"
  ng-model="somemodel"
  complexify
  complexify-common-passwords="true"
  complexify-min-length="8"
  complexify-css-attribute="background-color"
/>
```

### Options


| Options       | Type          | Explanation  |
| ------------- |:-------------:| -----:|
| `ng-model` | string | required |
| `complexify-common-passwords` | boolean | Check again common passwords (default: true) |
| `complexify-min-length`| number | Minumum password length |
| `complexify-css-attribute`| string | The css attribute of which the color will change, default background-color |
