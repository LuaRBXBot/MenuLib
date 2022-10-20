# MenuLib
Base Menu For Scripts (Not my) small changed

### Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/LuaRBXBot/MenuLib/main/Menu.lua", true))()
```
### Menu styles
* RJTheme 1
* RJTheme 2
* RJTheme 3/4/5/6/7
or create your own style
```lua
colorss = {
    SchemeColor = Color3.fromRGB(192, 18, 26),
    Background = Color3.fromRGB(15,15,15),
    Header = Color3.fromRGB(15,15,15),
    TextColor = Color3.fromRGB(255,255,255),
    ElementColor = Color3.fromRGB(20, 20, 20)
    }
```
### Window
```lua
local Window = Library.CreateLib("Window", colorss)
```

### Tab
```lua
local Tab = Window:NewTab("TabName")
```

### Section
```lua
local Section = Tab:NewSection("Section name", --[[true/false]] )
```

### Button
```lua
Section:NewButton("Button name", "Info", function()
 --// body script
end)
```

### Checkbox
```lua
Section:NewCheckBox("Checkbox","info checkbox",function(checkbox)
  if checkbox then
  --// Enable
  else
  --// Disable
end)
```

### Keybind
```lua
Section:NewKeybind("Keybind name","Info",Enum.KeyCode.F,functions()
print("You pressed on key")
end)
```

### Label
```lua
Section:NewLabel("Text label")
```

### Slider
```lua
Section:NewSlider("Slider","Info",250,0,function(slider)
game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = slider
end)
```

### Text box
```lua
Section:NewTextBox("Text box","Info",function(txt)
    game:GetService("Players").LocalPlayer.Character.Humanoid.JumpPower = txt
end)
```

### DropDown
```lua
Section:NewDropdown("DropDown (speed)", "Info", {"Standart", "Small", Big}, function(dropdown)
if dropdown == "Standart" then
game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = 16
elseif dropdown == "Small" then
game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = 8
elseif dropdown == "Big" then
game:GetService("Players").LocalPlayer.Character.Humanoid.WalkSpeed = 100
end
end)
```

### ColorPicker
```lua
Section:NewColorPicker("ColorPickerName", "Info", Color3.fromRGB(191,245,67), function(color)
game:service("Players").LocalPlayer.Character.Head.Color3 = color
end)
```

### Copy paste
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/LuaRBXBot/MenuLib/main/Menu.lua", true))()
theme = {
    SchemeColor = Color3.fromRGB(255, 255, 255),
    Background = Color3.fromRGB(124, 115, 115),
    Header = Color3.fromRGB(124, 115, 115),
    TextColor = Color3.fromRGB(255,255,255),
    ElementColor = Color3.fromRGB(141, 141, 141)
    }

    
local Window = Library:NewWindow("Your name script hub", theme)
local Tab = Window:NewTab("Your Tab Name")
local Section = Tab:NewSection("Section name")
Section:NewCheckbox("ToggleName","info",function(state)
  if state then
    --// Enable
    else
    --// Disable
    end
end)
Section:NewLabel("Slider:")
Section:NewSlider("SliderName","Info",150,0,function(count) --// 150 max | 16 min
    game:service("Players").LocalPlayer.Character.Humanoid.WalkSpeed = count
end)

--// And so on, the above listed buttons, sliders, selecting options(Dropdown), labels, tabs, sections.

--// if you not know how add new tab just add
local Tab = Window:NewTab("Your Tab Name2")
local Section = Tab:NewSection("Section name2")

--// And then write new functions in another tab
```











