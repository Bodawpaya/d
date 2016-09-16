# Disable increase/decrease font size with ctrl and mouse wheel?

`cd ~/.config/sublime-text-3`

`vim Packages/User/Default\ \(Linux\).sublime-mousemap`

```
  [
    // Change font size with ctrl+scroll wheel
    { "button": "scroll_down", "modifiers": ["ctrl"], "command": "null" },
    { "button": "scroll_up", "modifiers": ["ctrl"], "command": "null" }
  ]
```
