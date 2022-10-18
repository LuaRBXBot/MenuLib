# MenuLib
BaseMenuForScripts (Not my)

###Library
```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/LuaRBXBot/MenuLib/main/Menu.lua", true))()

###Menu styles
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

###Window
```lua
local Window = Library.CreateLib("Window", colorss)

###Tab
```lua
local Tab = Window:NewTab("TabName")

###Section
```lua
local Section = Tab:NewSection("Section name")

###Button
```lua
Section:NewButton("Button name", "Info", function()

end)

###CheckBox
```lua
Section:NewToggle("Checkbox","info checkbox",function(checkbox)
  if checkbox then
  print("Checkbox on")
  else
  print("Checkbox off")
end)

###Keybind
```lua
Section:NewKeybind("Keybind name","Info",Enum.KeyCode.F,functions()
print("You pressed on key")
end)

###Label
```lua
Section:NewLabel("Text label")

###Slider
```lua
Section:NewSlider("Slider","Info",250,0,function(slider)
game:GetService("Players").LocalPlayer.Humanoid.WalkSpeed = slider
end)

###Text box
```lua
Section:NewTextBox("Text box","Info (x - number [ x,x,x ])",function(txt)
    game:GetService("Players").LocalPlayer.Humanoid.JumpPower = txt
end)

###DropDown
```lua
Section:NewDropdown("DropwDown name", "Info", {"Option 1", "Option 2", Option 3}, function(dropdown)
if dropdown == "Option 1" then
--//function
elseif dropdown == "Option 2" then
--//function
elseif dropdown == "Option 3 then
--//function
end
end)












