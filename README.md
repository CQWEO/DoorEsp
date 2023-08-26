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
                        frame.BackgroundColor3 = Color3.new(2, 1, 2)
                    end 
                end 
            end 
        end 
