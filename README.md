local playerName = game.Players.LocalPlayer.Name
if game.Players.LocalPlayer.PlayerGui:FindFirstChild("TestGui") then
    game.Players.LocalPlayer.PlayerGui.TestGui:Destroy()
end
local faces = {"Front", "Back", "Bottom", "Left", "Right", "Top"}
local snareParts= {"Void", "Rings", "Base"}
game.Lighting.GlobalShadows = false
game.Lighting.OutdoorAmbient = Color3.new(1, 1, 1)
local text1 = Instance.new("TextLabel")
local text2 = Instance.new("TextLabel")
local text3 = Instance.new("TextLabel")
local gui = Instance.new("ScreenGui")
gui.Name = "TestGui"
gui.Parent = game.Players.LocalPlayer.PlayerGui
while true do
for i, o in pairs(game.Workspace.CurrentRooms:GetChildren()) do
        if o:FindFirstChild("Door") then
            if o.Door:FindFirstChild("Door") then
                if not o.Door.Door:FindFirstChild("SurfaceGui") then
                    for a = 1, 6 do
                        local surface = Instance.new("SurfaceGui")
                        surface.Parent = o.Door.Door
                        surface.AlwaysOnTop = true
                        surface.Face = Enum.NormalId[faces[a]]
                        local frame = Instance.new("Frame", surface)
                        frame.Size = UDim2.new(5, 9, 5, 9)
                        frame.BorderSizePixel = 5
                        frame.BackgroundTransparency = 2.5
                        frame.BackgroundColor3 = Color3.new(9, 1, 1)
                end
            end
        end
    end
    wait()
end
