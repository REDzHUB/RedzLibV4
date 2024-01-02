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
```

## Global Functions
```lua
Instance:Destroy()

Instance:Visible(false)
```

## Window
Create a Window
```lua
local Window = Library:MakeWindow({"redz Library"})

--[[
  Window:Set("New Title")
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
local Tab = Window:MakeTab({
  Name = "Tab",
  Icon = "Home"
})

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
  
  Button:Set("New Name or Function")
]]
```

## Toggle
Create a Normal Toggle
```lua
local Toggle = Tab:AddToggle({
  Name = "Toggle",
  Default = false,
  Callback = function(Value)
    
  end
})

--[[
  Toggle:Set("New Name or Value or Function")
  
  Toggle:Callback(function(Value)
  
  end)
]]
```
Create a Save Toggle
```lua
local Toggle = Tab:AddToggle({
  Name = "Toggle",
  Default = false,
  Save = "Toggle Example",
  Callback = function(Value)
    
  end
})

--[[
  Toggle:Set("New Name or Value or Function")
  
  Toggle:Callback(function(Value)
  
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
