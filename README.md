script.Parent.MouseButton1Click:Connect(function()
	local sky = Instance.new("Sky")
	sky.Parent = game.Lighting

	-- change the ids
	sky.SkyboxBk = "rbxassetid://433517917" -- idk
	sky.SkyboxDn = "rbxassetid://433517917" -- down
	sky.SkyboxFt = "rbxassetid://433517917" -- idk
	sky.SkyboxLf = "rbxassetid://433517917" -- left
	sky.SkyboxRt = "rbxassetid://433517917" -- right
	sky.SkyboxUp = "rbxassetid://433517917" -- top
end)
