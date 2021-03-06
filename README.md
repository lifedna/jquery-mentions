jquery-mentions
===============
More stable alternative to [podio's jquery.mentionsInput](https://github.com/podio/jquery-mentions-input) plugin, which is currently unmaintained.

Advantages over jquery.mentionsInput:
- Many issues are solved
- Input styles are copied to highlighter automatically
- Support of both textarea and input tags
- Hidden-input with markuped text created automatically
- Uses jQuery UI autocomplete
- The code is much smaller

Solved issues of jquery.mentionsInput:
- Adding spaces before mention shows overlay
- Scrolling to bottom inside textarea moves text, but not highlights
- Typing email adress activates mentions
- Inserting same mentions multiple times
- Prepopulate input with text

## Usage
For this plugin to work you need to include [jQuery Autocomplete](http://jqueryui.com/autocomplete/) to your page.

```
var data = [
    {value: 'alex', uid: 'user:1'},
    {value: 'andrew', uid: 'user:2'},
    {value: 'angry birds', uid: 'game:5'},
    {value: 'assault', uid: 'game:3'}
];

$('textarea').mentionsInput({source: data});
```


## Options

### source
  Data source for the autocomplete. See [jQuery Autocomplete API](http://api.jqueryui.com/autocomplete/#option-source) for available values.
### delay
  Delay for autocomplete to start searching. Default value is 0. More info in [jQuery Autocomplete API](http://api.jqueryui.com/autocomplete/#option-delay)
### trigger
  Char which trigger autocomplete, default value is '@'
