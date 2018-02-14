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
  - [Multi-touch Web Development on HTML5Rocks](https://www.html5rocks.com/en/mobile/touch/)
  - [Video: how pseudo classes work on mobile devices](https://www.youtube.com/watch?v=SPXn4e6lh1U)
  - [Touch Events on MDN](https://developer.mozilla.org/en-US/docs/Web/API/Touch_events)

### Touch Support
  - [Add Touch to Your Site on Google Developers](https://developers.google.com/web/fundamentals/design-and-ux/input/touch/?hl=en#stateful-elements-respond-to-touch)

## Notes:
### Touch Events
Each touch event includes three lists of touches.
  - **touches**: a list of all fingers currently on the screen.
  - **targetTouches**: a list of fingers on the current DOM element.
  - **changedTouches**: a list of fingers involved in the current event. For example, in a touchend event, this will be the finger that was removed.

These lists consist of objects that contain touch information:
  - **identifier**: a number that uniquely identifies the current finger in the touch session.
  - **target**: the DOM element that was the target of the action.
  - **client/page/screen coordinates**: where on the screen the action happened.
  - **radius coordinates and rotationAngle**: describe the ellipse that approximates finger shape.

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

### Prevent text from being selected
On mobile devices by long press on the screen
```html
  <style>
    -moz-user-select: none;
    -webkit-user-select: none;
    -ms-user-select: none;
    user-select: none;
  </style>
```

### Touch Event Example
```javascript
  // Check if pointer events are supported.
  if (window.PointerEventSupport) {
    // Add Pointer Event Listener
    swipeFrontElement.addEventListener(pointerDownName, this.handleGestureStart, true);
  } else {
    // Add Touch Listener
    swipeFrontElement.addEventListener('touchstart', this.handleGestureStart, true);
    // Add Mouse Listener
    swipeFrontElement.addEventListener('mousedown', this.handleGestureStart, true);
  }
```
