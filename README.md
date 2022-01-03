_G.Up = false
_G.Down = false
_G.Red = false
_G.Green = false

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()

local Window = Library.CreateLib("Cart Ride Into Rdite!", "Serpent")

local MainTab = Window:NewTab("Main")

local MainSection = MainTab:NewSection("Main")

MainSection:NewToggle("Fast Cars", "makes the cars so fast that they crash!", function(state)
    if state then
        _G.Up = true
        if _G.Up == true then
            while true do wait()
                if _G.Up == true then
                    for i,part in pairs(game.Workspace.Carts:GetDescendants()) do
                        if part.Name == "Up" then
                            fireclickdetector(part.Click)
                        end
                    end 
                end
            end
        end
    else
       _G.Up = false
    end
end)

MainSection:NewToggle("Slow Cars", "makes the cars so slow that they can't drive!", function(state)
    if state then
        _G.Down = true
        if _G.Down == true then
            while true do wait()
                if _G.Down == true then
                    for i,part in pairs(game.Workspace.Carts:GetDescendants()) do
                        if part.Name == "Down" then
                            fireclickdetector(part.Click)
                        end
                    end 
                end
            end
        end
    else
       _G.Down = false
    end
end)

MainSection:NewToggle("Turn Carts On!", "turn all the carts on!", function(state)
    if state then
        _G.Red = true
        if _G.Red == true then
            while true do wait()
                if _G.Red == true then
                    for i, part in pairs(game.Workspace.Carts:GetDescendants()) do
                        if part.Name == "On" and part.Color == Color3.fromRGB(196, 40, 28) then
                            fireclickdetector(part.Click) 
                        end
                    end
                end
            end
        end
    else
       _G.Red = false
    end
end)

MainSection:NewToggle("Turn Carts Off!", "turn all the carts off!", function(state)
    if state then
        _G.Green = true
        if _G.Green == true then
            while true do wait()
                if _G.Green == true then
                    for i, part in pairs(game.Workspace.Carts:GetDescendants()) do
                        if part.Name == "On" and part.Color == Color3.fromRGB(40, 127, 71) then
                            fireclickdetector(part.Click) 
                        end
                    end
                end
            end
        end
    else
       _G.Green = false
    end
end)
