# redz Library V4
## Library loadstring
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/REDzHUB/RedzLibV4/main/Source.lua"))()
```

library functions
```lua
Library:SetTheme("Theme Name") -- https://raw.githubusercontent.com/REDzHUB/RedzLibV4/main/Themes.lua

Library:SetTransparency(0.1) -- 0, 1

Library:GetThemes() -- void, return = table

Library:GetIcon("Icon Name")

-- ///////// 

Library.info.PlaceName

Library.info.Version
```

## Global Functions
```lua
Instance:Destroy()

Instance:Visible(false)
```

## Window
Create a Window
```lua
local Window = redzlib:MakeWindow({
  Title = "REDz HUB : Example",
  SubTitle = "by : redz9999",
  LoadText = "redz Hub",
  Flags = "redz Hub | Example.lua"
})

--[[
  Window:Set("New Title or Image")
]]
```

## Notification
Create a Notification
```lua
local Notify = Library:MakeNotify({
  Title = "Notification",
  Text = "This is a Notification",
  Time = 5
})

--[[
  Notify:Wait() -- Wait for the notification to end
]]
```

## Tab
Create a Tab
```lua
local Tab = Window:MakeTab({Name = "Tab", Icon = "Home"})

--[[
  Tab:Set("New Icon or Name")
]]
```

## Section
Create a Section
```lua
local Section = Tab:AddSection({"This is a Section"})

--[[
  Section:Set("Section")
]]
```

## Paragraph
Create a Paragraph
```lua
local Paragraph = Tab:AddParagraph({"Paragraph", "this is a Paragraph"})

--[[
  Paragraph:Set("New Text")
  
  Paragraph:Set("New Name", "New Text")
]]
```

## Label
Create a Text Label
```lua
local TextLabel = Tab:AddLabel({"Text", "This is a Text Label"})

--[[
  TextLabel:Set("New Name")
]]
```

Create a Image Label
```lua
local ImageLabel = Tab:AddLabel({"Image", "This is a Image Label", "rbxassetid://"})

--[[
  ImageLabel:Set("New Name", "New Image")
]]
```

## Button
Create a Button
```lua
local Button = Tab:AddButton({
  Name = "Button",
  Callback = function()
    
  end
})

--[[
  Button:Callback(function()
    
  end)
  
  Button:Set("New Name")
]]
```

## Toggle
Create a Toggle
```lua
local Toggle = Tab:AddToggle({
  Name = "Toggle",
  Default = false,
  Callback = function(Value)
    
  end
})

--[[
  Toggle:Set(false)
  
  Toggle:Callback(function(Value)
  
  end)
]]
```

## Dropdown
Create a Dropdown
```lua
local Dropdown = Tab:AddDropdown({
  Name = "Dropdown",
  Options = {"1", "2", "3"}
  Default = {"2"}
  MultSelect = false
  Callback = function(Value)
    
  end
})

--[[
  Dropdown:Set({New Options}, Void)
  -- Example : {
    Dropdown:Set({"one", "two", "three"}, true)
  }
  
  Dropdown:Callback(function(Value)
    
  end)
]]
```

## Slider
Create a Slider
```lua
local Slider = Tab:AddSlider({
  Name = "Slider",
  MinValue = 1,
  MaxValue = 10,
  Default = 5,
  Increase = 1,
  Callback = function(Value)
    
  end
})

--[[
  Slider:Set(7)
  
  Slider:Callback(function(Value)
    
  end)
]]
```

## Extra
Create a Discord Invite
```lua
Tab:AddDiscordInvite({
  DiscordTitle = "REDz Hub | Community",
  DiscordIcon = "rbxassetid://15298567397",
  DiscordLink = "https://discord.gg/7aR7kNVt4g"
})
```

Create a Minimize Button
```lua
Window:AddMinimizeButton({
  Button = {
    -- Button Properties
    Image = "rbxassetid://15298567397"
  },
  UICorner = {true,
    -- Corner Properties
    CornerRadius = UDim.new(0.5, 0)
  },
  UIStroke = {false, {
    -- Stroke Properties
  }}
})
```
