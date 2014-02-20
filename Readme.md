*This repository is a mirror of the [component](http://component.io) module [yields/extensible](http://github.com/yields/extensible). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/yields-extensible`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# extensible

  extensible constructors.

## Installation

  Install with [component(1)](http://component.io):

    $ component install yields/extensible

## Example

```js
function View(){}
function FormView(){}
function TabView(){}
function ComplexFormView(){}

// => Make the view extensible

extensible(View);

// => FormView extends View

View.extend(FormView);

// => ComplexFormView extends FormView

FormView.extend(ComplexFormView);
```

## API

### extensible(Constructor)

Add recursive `.extend(Other)` method to `Constructor`.

## component/inherit

extensible uses component/inherit to do the inheritance,
but it's different from inherit since it adds `.extend()` static
method to your constructor.

this means you can have a single `extensible(View)` and do `View.extend(OtherView)`
instead of installing `component/inherit` on each view component.

## License

  MIT
