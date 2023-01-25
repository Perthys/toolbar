# toolbar
simple toolbar

```lua


local Toolbar = Toolbar.new("Manage Unit")

task.delay(1, function()
    Toolbar:Toggle()

    task.wait(2)
    Toolbar:Toggle()

    for i = 1,10 do
        Toolbar:AddButton({
            Name = "TestButton"..i;
            OnClicked = function(self)
                print("Clicked Button".. self.Name)
                self:SetTitle("hello")
            end
        })
    end
    task.wait(5)

    Toolbar:SetTitle("I am dying now")
    task.wait(2)
    Toolbar:Destroy()
end)

```
