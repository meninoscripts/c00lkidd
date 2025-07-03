bodyGyro.MaxTorque = Vector3.new()
bodyGyro.D = 10
bodyGyro.Parent = hrp

script.Parent.MouseButton1Click:Connect(function()
	isFlying = not isFlying
end)

script.Parent.MouseButton2Click:Connect(function()
	isFlying = false
end)

game:GetService("RunService").RenderStepped:Connect(function()
	if isFlying then
		bodyPos.MaxForce = Vector3.new(math.huge, math.huge,math)
		bodyGyro.MaxTorque = Vector3.new(math.huge, math.huge, math.huge)
		bodyPos.Position = hrp.Position +((hrp.Position - camera.CFrame.Position).Unit * 10)
		bodyGyro.CFrame = CFrame.new(camera.CFrame.Position, hrp.Position)
	else
		bodyPos.MaxForce = Vector3.new()
		bodyGyro.MaxTorque = Vector3.new()
	end
end)
