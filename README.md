local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")


local function dançar()
    
    local anim = Instance.new("Animation")
    anim.AnimationId = "rbxassetid://4211409027"  
    
    
    local animTrack = humanoid:LoadAnimation(anim)
    animTrack:Play()
end


game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.E then
        dançar()
    end
end)
