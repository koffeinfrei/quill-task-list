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

## TODO
* For now the click triggers a dummy update, because the css class toggle
  doesn't trigger a change in quill. The proper way would be to change the
  state of the item by using a delta directly and maybe two kinds of list item
  classes (a normal `TaskListItem` and a `CheckedTasklistItem` or something.
  Fixing this would also fix the history.  This may be easy for someone
  familiar with the internals of quill.

## License

[BSD 3-clause](LICENSE) (the same one that [Quill](https://github.com/quilljs/quill) uses)
