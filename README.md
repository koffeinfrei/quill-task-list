# Task list for quill

Adds a task / todo list to the quill editor. Behaves as the built-in bullet
list.
Includes a toolbar item.

![Toolbar icon and task list](screenshot.png)

## Usage

1. Require the JavaScript (ES6) and the CSS (SASS) file in your interwebs page
1. Configure the module when instantiating quill

```javascript
this.editor = new Quill('#editor', {
  modules: {
    'toolbar': [ 'task-list' ],
    'task-list': true
  }
});
```

There is also an optional option to provide a callback after a click on a task
list item.

```javascript
this.editor = new Quill('#editor', {
  modules: {
    'toolbar': [ 'task-list' ],
    'task-list': {
      // optional callback
      onClick: function() { /* ... */ }
    }
  }
});
```

## License

[BSD 3-clause](LICENSE) (the same one that [Quill](https://github.com/quilljs/quill) uses)
