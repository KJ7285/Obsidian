# Obsidian UI Library

| Property | Type | Default | Description |
| --- | --- | --- | --- |
| Text | string | "Button" | The button's text |
| Func | function | function() end | The function to call when clicked |
| DoubleClick | boolean | false | Whether the button needs double-click |
| Tooltip | string | nil | Tooltip text shown on hover |
| DisabledTooltip | string | nil | Tooltip shown when disabled |
| Risky | boolean | false | Displays text in red to indicate risky action |
| Disabled | boolean | false | Whether the button is disabled |
| Visible | boolean | true | Whether the button is visible |


#### Methods


| Method | Description |
| --- | --- |
| `Button:SetText(text)` | Updates the button's text |
| `Button:SetDisabled(boolean)` | Enables or disables the button |
| `Button:SetVisible(boolean)` | Shows or hides the button |


### Toggles & Checkboxes


Toggles and checkboxes allow users to toggle boolean values.


```lua
-- Always capture the reference returned by AddToggle
local MyToggle = Groupbox:AddToggle("MyToggle", {
    Text = "Example Toggle",
    Default = false,
    Tooltip = "This is a toggle",
    Callback = function(Value)
        print("Toggle changed to:", Value)
    end
})


-- You can use :OnChanged to add another callback
MyToggle:OnChanged(function(Value)
    print("Toggle changed via OnChanged:", Value)
})


-- You can also create checkboxes instead of switch-style toggles
local MyCheckbox = Groupbox:AddCheckbox("MyCheckbox", {
    Text = "Example Checkbox",
    Default = false,
    Callback = function(Value)
        print("Checkbox changed to:", Value)
    end
})
```


#### Options


| Property | Type | Default | Description |

