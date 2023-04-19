# VenyX-Docs-Unofficial
## Make Window
```lua
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/KATTM1/Veny-X-Draggable-/main/BIGGEDITT.lua"))()
local getee = "Veny X | Ui Library"
local venyx = library.new(getee, 5013109572)
```
## Create Tab
```lua
local page = venyx:addPage("Test", 5012544693)
```

## Create Section
```lua
local section1 = page:addSection("Section 1")
```

## Create Toggle
```lua
section1:addToggle("Toggle", nil, function(value)
	print("Toggled", value)
end)
```

## Create Button
```lua
section1:addButton("Button", function()
	print("Clicked")
end)
```

## Create TextBox
```lua
section1:addTextbox("Notification", "Default", function(value, focusLost)
	print("Input", value)

	if focusLost then
		venyx:Notify("Title", value)
	end
end)
```

## Create Keybind
```lua
section2:addKeybind("Toggle Keybind", Enum.KeyCode.One, function()
	print("Activated Keybind")
	venyx:toggle()
end, function()
	print("Changed Keybind")
end)
```

## Create Color Picker
```lua
section2:addColorPicker("ColorPicker", Color3.fromRGB(50, 50, 50))
```

## Dropdown
```lua
section2:addDropdown("Dropdown", {"Hello", "World", "Hello World", "Word", 1, 2, 3}, function(text)
	print("Selected", text)
end)
```

## ThemeChanger
```lua
for theme, color in pairs(themes) do -- all in one theme changer, i know, im cool
	page:addColorPicker(theme, color, function(color3)
		venyx:setTheme(theme, color3)
	end)
end

```
## Notify
```lua
venyx:Notify("Title", value)
```
## Slider
```lua
section2:addSlider("Slider", 0, -100, 100, function(value)
	print("Dragged", value)
end)
```
## Detect Ui (Paste on top of the code)
```lua
local Luas = game.CoreGui:FindFirstChild(getee)
if Luas then
Luas:Destroy()
end
```

