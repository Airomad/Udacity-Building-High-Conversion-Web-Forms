# Udacity Building High Conversion Web Forms Notes

## Useful links:
  - [Create Amazing Forms on Google Developer](https://developers.google.com/web/fundamentals/design-and-ux/input/forms/?hl=en)
  - [Web Forms the Right Way (Presentation)](https://www.slideshare.net/greenido/web-forms-the-right-way)
  - [Datalist element on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist)
  - [Styling Calendars](https://www.tjvantoll.com/2013/04/15/list-of-pseudo-elements-to-style-form-controls/#input_date)
  - [Autocomplete attribute on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-autocomplete)
  - [Autofocus input on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-autofocus)
  - [Input validation on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-required)
  - [Learn, build, & test Regular Expressions (RegEx / RegExp) online](https://regexr.com/)
  - [Constraint Validation API with setCustomValidity() on MDN](https://developer.mozilla.org/en-US/docs/Web/API/HTMLSelectElement/setCustomValidity)
  - [The Current State of HTML5 Forms](https://www.wufoo.com/html5/)
  - [Using Geolocation on MDN](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation/Using_geolocation)

## Snippets:
### Input numbers validation example
```javascript
    // grab <input id="range-example" type="range" min="0" max="5" step="1"> from the page
    var rangeInput = document.querySelector('input#range-example');

    // grab <p id="output"></p> to display the output
    var output = document.querySelector('p#output');

    // update the display when the range changes
    rangeInput.onchange = function() {
        output.innerHTML = this.value;
    };
```
