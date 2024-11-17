# About EasyMovesetLibrary (EML)

**EasyMovesetLibrary (EML)** is a Lua-based framework designed to help exploiters easily implement and manage complex custom movesets for characters in the Roblox game named "The Strongest Battlegrounds" or "Saitama Battlegrounds". This library is perfect for users who want to create customizable and fluid animation sets, control character abilities, and manage move interactions seamlessly.

## Key Features
- **Flexible Moveset Management**: EML allows you to define and customize movesets for any character, making it easy to adjust abilities and animations based on game mechanics.
- **Built-In Animation Support**: With support for custom animation sets (origanims), EML helps you manage character animations with ease.
- **Configurable Settings**: Easily configure global settings via `_G.EMLSettings` to fine-tune the behavior of movesets and animations to suit your needs.
- **Modular Design**: The library is modular, allowing for easy expansion and integration into different projects, enabling developers to create unique, dynamic abilities and animations.
- **Version Control**: EML uses GitHub for version control, ensuring the library remains up-to-date and ready for collaboration.

## Installation
To install EML, simply insert this line: `local EML = loadstring(game:HttpGet(https://raw.githubusercontent.com/aerialasf/EML.lua/refs/heads/main/Main.lua"))()` Be sure to set up your environment by configuring the appropriate settings in `_G.EMLSettings`.

## Usage
```lua
_G.EMLSettings = { -- Example of how to change the settings
    debug = false,
    firstonly = true,
}
local EML = loadstring(game:HttpGet("https://raw.githubusercontent.com/aerialasf/EML.lua/refs/heads/main/Main.lua"))()  -- Example of how to load the library

local moveset = EML:Create("ExampleMoveset") -- How to make a moveset

moveset:Set("Move1", { -- How to set a property
    "AnimationId",
    {}, -- Animation details
    function() EML:DebugPrint("Wow!") end, -- Animation callback
    "Move1", -- Move name
})


EML:Init()  -- Initialize EML with custom settings & set movesets
```

## Q/A
- **Why can't I use any other characters than Saitama?**: You can only currently use Saitama as the original character. May add more on 1.1.0
- **It errored when I used :Create()!**: You need an id for the moveset. Or you may have just used the wrong variable containing the library. I try everything to make it work.
- **The library is confusing!**: I'm continuously trying to make it easy as possible to make a moveset. Please make an issue and describe what you don't understand.
- **Why does my animations not play?**: Check if the animation id is correct. Animations will not play if it isn't made by the game's creator ("Yielding Arts"). You can get banned if the animation is a bait animation or is deprecated/others.
- **Can I add custom tools to the moveset?**: Yes, in the future. In 1.2.0 I will add :CreateTool(toolname, callback) to the movesets to create custom tools.
