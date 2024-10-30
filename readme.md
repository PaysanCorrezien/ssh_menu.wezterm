# 🔌 WezTerm SSH Menu Plugin

A simple plugin that creates an interactive SSH host selector from your known_hosts file for WezTerm.

## ⭐ Features

- 📋 Lists SSH hosts from your known_hosts file
- 🔍 Fuzzy search support
- 🖥️ Cross-platform compatibility (Windows/Unix)
- 🚀 Quick SSH connections in new tabs

## 🚀 Installation

```lua
local wez = require('wezterm')
local ssh_menu = wez.plugin.require("https://github.com/PaysanCorrezien/ssh_menu.wezterm")
```

## 💡 Usage

Add to your WezTerm configuration:

```lua
local config = {
  keys = {
    {
      key = "s",
      mods = "LEADER",
      action = wezterm.action_callback(function(window, pane)
        ssh_menu.ssh_menu(window, pane)
      end),
    },
  }
}
```

### Navigation

- Use number keys (1-9) to select hosts
- Press `/` to activate fuzzy search
- `ESC` to cancel

## 🤝 Contributing

Contributions are welcome! Please note:

- This project is maintained as time permits
- Focus on meaningful improvements that don't add unnecessary complexity

## 📄 License

This project follows the MIT License conventions. Feel free to use, modify, and distribute as per MIT License terms.
