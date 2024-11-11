# About EasyMovesetLibrary (EML)

**EasyMovesetLibrary (EML)** is a Lua-based framework designed to help exploiters easily implement and manage complex custom movesets for characters in the Roblox game named "The Strongest Battlegrounds" or "Saitama Battlegrounds". This library is perfect for users who want to create customizable and fluid animation sets, control character abilities, and manage move interactions seamlessly.

## Key Features
- **Flexible Moveset Management**: EML allows you to define and customize movesets for any character, making it easy to adjust abilities and animations based on game mechanics.
- **Built-In Animation Support**: With support for custom animation sets (origanims), EML helps you manage character animations with ease.
- **Configurable Settings**: Easily configure global settings via `_G.EMLSettings` to fine-tune the behavior of movesets and animations to suit your game’s needs.
- **Modular Design**: The library is modular, allowing for easy expansion and integration into different projects, enabling developers to create unique, dynamic abilities and animations.
- **Version Control**: EML uses GitHub for version control, ensuring the library remains up-to-date and ready for collaboration.

## Installation
To install EML, simply download the `EML.lua` script and include it in your Roblox game. Be sure to set up your environment by configuring the appropriate settings in `_G.EMLSettings`.

## Usage
```lua
_G.EMLSettings = { -- Example of how to change the settings
    debug = false,
    firstonly = true,
}
local EML = require(game.ServerStorage.EML)  -- Example of how to load the library
EML:Init()  -- Initialize EML with custom settings & set movesets
```
