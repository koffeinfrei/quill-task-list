# Task list for quill

Adds a task / todo list to the quill editor. Behaves as the built-in bullet
list.
Includes a toolbar item.

The list items are clickable. A click on an item toggles the item as checked.

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

## TODO
* For now the click triggers a callback, where the change is handled. The
  proper way would be to trigger the change internally. Probably by using a
  delta and maybe two kinds of list item classes (a normal `TaskListItem` and a
  `CheckedTasklistItem` or something. Fixing this would also fix the history.
  This may be easy for someone familiar with the internals of quill.

## License

[BSD 3-clause](LICENSE) (the same one that [Quill](https://github.com/quilljs/quill) uses)
