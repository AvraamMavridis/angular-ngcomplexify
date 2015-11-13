# Angular ngComplexify

version 0.2

ngComplexify is a module/directive that determines the complexity of a
given password, it emits an event on the scope with the persentance of the password complexity.
Also it has the ability to check agains 10.000 common passwords.

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
  complexify-min-length="8" <!-- optional -->
  complexify-css-attribute="background-color" <!-- optional -->
/>
```

### Event

You can listen to the `$scope.$emit('passwordComplexity', complexity)` event.

### Options

| Options       | Type          | Explanation  |
| ------------- |:-------------:| -----:|
| `ng-model` | string | required |
| `complexify-common-passwords` | boolean | Check again 10.000 common passwords (default: true) |
| `complexify-min-length`| number | Minumum password length (optional) |
| `complexify-css-attribute`| string | The css attribute of which the color will change (optional) |
