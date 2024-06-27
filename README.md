local Library = loadstring(game:HttpGet("https://pastebin.com/raw/KNBp0LRy"), "Coastified UI")()
repeat wait() until game:IsLoaded()
game:GetService("Players").LocalPlayer.Idled:connect(function()
game:GetService("VirtualUser"):ClickButton2(Vector2.new())
end)
local Window = Library:NewWindow("Get $R for Win")

local Section = Window:NewSection("AutoFarm")

local Toggle = Section:CreateToggle("Auto [Stage-Finish]", function(Value)
_G.Obby = Value
while _G.Obby do
wait(0.1)  -- Wait for 1 second before checking for enemies
for _,v in pairs(workspace.Checkpoints:GetDescendants()) do
if v:IsA("TouchTransmitter") then
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 0) --0 is touch
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 1) -- 1 is untouch
end
end
wait(0.1)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-334.064697, 264.728699, 949.115906, 0.673954606, 0, -0.73877275, 0, 1, 0, 0.73877275, 0, 0.673954606)
   end
end)
local Section = Window:NewSection("GiveItem")
local Dropdown = Section:CreateDropdown("Select ! Items", {"TacoGiver", "Speed Coil Giver", "RadioGiver", "BikeGiver", "HoverboardGiver", "CloudGiver", "TeddyGiver", "BloxyColaGiver", "DogeGiver", "SprayGiver", "PaintGiver"}, Selected, function(Value)
    Selected = Value
end)
Section:CreateButton("Get", function(Value)
for _,v in pairs(workspace.Model[Selected]:GetDescendants()) do
if v:IsA("TouchTransmitter") then
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 0) --0 is touch
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 1) -- 1 is untouch
end
end    
end)
local Section = Window:NewSection("Path!")
local Dropdown = Section:CreateDropdown("Select ! Path!", {"Path1", "Path2", "Path3", "Path4", "Path5"}, Selected1, function(Value)
    Selected1 = Value
end)
Section:CreateButton("Get", function(Value)
for _,v in pairs(workspace.Model[Selected1]:GetDescendants()) do
if v:IsA("TouchTransmitter") then
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 0) --0 is touch
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 1) -- 1 is untouch
end
end    
end)
local Section = Window:NewSection("Speed")
local Dropdown = Section:CreateDropdown("Select ! Speeds", {"Speed1", "Speed2", "Speed3", "Spedd4"}, Selected2, function(Value)
    Selected2 = Value
end)
Section:CreateButton("Get", function(Value)
for _,v in pairs(workspace.Model[Selected2]:GetDescendants()) do
if v:IsA("TouchTransmitter") then
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 0) --0 is touch
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 1) -- 1 is untouch
end
end    
end)
Section:CreateButton("Reset-Speed!", function(Value)
for _,v in pairs(workspace.Model.ResetSpeed:GetDescendants()) do
if v:IsA("TouchTransmitter") then
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 0) --0 is touch
firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart, v.Parent, 1) -- 1 is untouch
end
end    
end)
