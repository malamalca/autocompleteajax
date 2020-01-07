# autocompleteajax
materializecss autocomplete with ajax data load

Here you can send ajax & get data with ajax, set delay and min input value length if you need, can set custom data for send request & cal callback function if need.

Check demo here:
https://jsfiddle.net/z6xdncq1/

usage example code:

```js
$(document).ready(function() {
    $("#street").autocompleteajax({
        "source": "url",
        "onSelect": function(item) {
            console.log(item);
        }
    });
})
```

```html
<div class="input-field">
  <input id="street" type="text" autocomplete="off" name="street" placeholder="Enter something...">
  <label id="street_label" for="street" style="width: 100%">Street</label>
  <input type="hidden" class="autocomplete-id" name="autocomplete-id" value="">
</div>
```

Ajax request is executed with ?term=XXX parameter. Server should return json response in form below:

```js
[
    {"id":1,"value":1,"label":"First Item"},
    {"id":2,"value":2,"label":"Second Item"}
]
```
