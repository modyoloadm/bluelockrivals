local KeyGuardLibrary = loadstring(game:HttpGet("https://cdn.keyguardian.org/library/v1.0.0.lua"))()
local trueData = "ec2e5bea09ac42988712d01625eed808"
local falseData = "1f598a9796724d0eb5a1c41fe3e8cf72"

KeyGuardLibrary.Set({
  publicToken = "a7ce122b04a94bc79dc8c8f04f746f54",
  privateToken = "7772dd595c2945d7903ee7569b7182fe",
  trueData = trueData,
  falseData = falseData,
})

local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local key = ""

local Window = Fluent:CreateWindow({
    Title = "Key System",
    SubTitle = "Modyolo Hub",
    TabWidth = 160,
    Size = UDim2.fromOffset(580, 340),
    Acrylic = false,
    Theme = "Dark",
    MinimizeKey = Enum.KeyCode.LeftControl
})

local Tabs = {
    KeySys = Window:AddTab({ Title = "Key System", Icon = "key" }),
}

local Entkey = Tabs.KeySys:AddInput("Input", {
    Title = "Enter Key",
    Description = "Enter Key Here",
    Default = "",
    Placeholder = "Enter key…",
    Numeric = false,
    Finished = false,
    Callback = function(Value)
        key = Value
    end
})

local Checkkey = Tabs.KeySys:AddButton({
    Title = "Check Key",
    Description = "Enter Key before pressing this button",
    Callback = function()
        local response = KeyGuardLibrary.validateDefaultKey(key)
        if response == trueData then
           print("Key is valid")
           if game.PlaceId == 9872472334 then
local CoreGui = game:GetService("StarterGui")

CoreGui:SetCore("SendNotification", {
    Title = "Script Made By",
    Text = "GhostPlayer",
    Icon = "rbxassetid://29819383",
    Duration = 2.5,
})

local Library = loadstring(Game:HttpGet("https://raw.githubusercontent.com/bloodball/-back-ups-for-libs/main/wizard"))()

local PhantomForcesWindow = Library:NewWindow("Evade")

local Folder1 = PhantomForcesWindow:NewSection("Main")
local Folder2 = PhantomForcesWindow:NewSection("Auto Farm")

Folder1:CreateButton("No Camera Shake", function()
print("HI")
NoCamShake = true
end)

Folder1:CreateButton("Walk Speed", function()
print("HI")
tpwalking = true
end)

Folder1:CreateButton("Inf Jump", function()
print("HI")
local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
end)

Folder1:CreateButton("Super Zoom", function()
print("HI")
SuperZoom = true
end)


Switch1 = false
Folder2:CreateToggle("Auto Respawn", function(value)
print(value)
if Switch1 == false then
Switch1 = true
AutoRespawn = true
else
Switch1 = false
AutoRespawn = false
end
end)

Switch2 = false
Folder2:CreateToggle("Auto Revive Player", function(value)
print(value)
if Switch2 == false then
Switch2 = true
AutoRevive = true
else
Switch2 = false
AutoRevive = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,10,0)
end
end)



--No Camera Shake Operator
game:GetService('RunService').Heartbeat:connect(function()
if NoCamShake == true then
game.Players.LocalPlayer.PlayerScripts.CameraShake.Value = CFrame.new(0,0,0) * CFrame.new(0,0,0)
end
end)
--


--Walk Speed Operator
game:GetService('RunService').Stepped:connect(function()
if game.Players.LocalPlayer.Character.Humanoid.MoveDirection.Magnitude > 0 and tpwalking == true then 
   game.Players.LocalPlayer.Character:TranslateBy(game.Players.LocalPlayer.Character.Humanoid.MoveDirection * 1) 
end
end)
--


--Super Zoom Operator
game:GetService('RunService').Heartbeat:connect(function()
if SuperZoom == true then
game.Players.LocalPlayer.CameraMaxZoomDistance = 100000
game.Players.LocalPlayer.CameraMinZoomDistance = -1
end
end)
--




--Auto Respawn Operator
AutoRespawn = false

game:GetService('RunService').Heartbeat:connect(function()
if AutoRespawn == true and game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:GetAttribute("Downed") then
   game:GetService("ReplicatedStorage").Events.Respawn:FireServer()
end
end)
--




--Auto Revive Player Operator
AutoRevive = false

game:GetService('RunService').Heartbeat:connect(function()
if AutoRevive == true then
local WorkspacePlayers = game:GetService("Workspace").Game.Players
local Players = game:GetService('Players')
local localplayer = Players.LocalPlayer
		
local GetDownedPlr = function()
	for i,v in pairs(WorkspacePlayers:GetChildren()) do
		if v:GetAttribute("Downed") then
			return v
		end
	end
end

local downedplr = GetDownedPlr()
	if downedplr ~= nil and downedplr:FindFirstChild('HumanoidRootPart') then
		task.spawn(function()
			while task.wait() do
				if localplayer.Character then
					workspace.Game.Settings:SetAttribute("ReviveTime", 2.2)
					localplayer.Character:FindFirstChild('HumanoidRootPart').CFrame = CFrame.new(downedplr:FindFirstChild('HumanoidRootPart').Position.X, downedplr:FindFirstChild('HumanoidRootPart').Position.Y -5, downedplr:FindFirstChild('HumanoidRootPart').Position.Z)
					task.wait()
					game:GetService("ReplicatedStorage").Events.Revive.RevivePlayer:FireServer(tostring(downedplr), false)
					task.wait(4.5)
					game:GetService("ReplicatedStorage").Events.Revive.RevivePlayer:FireServer(tostring(downedplr), true)
					game:GetService("ReplicatedStorage").Events.Revive.RevivePlayer:FireServer(tostring(downedplr), true)
					game:GetService("ReplicatedStorage").Events.Revive.RevivePlayer:FireServer(tostring(downedplr), true)
					break
				end
			end
		end)
	end
end
end)
--

-----------------------
else

local FakeDisconnect = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Frame1 = Instance.new("Frame")
local Line = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local Page1 = Instance.new("TextLabel")
local Page2 = Instance.new("TextLabel")
local Page3 = Instance.new("TextLabel")
local Bt1 = Instance.new("TextButton")
local Bt2 = Instance.new("TextButton")

FakeDisconnect.Parent = game.CoreGui

Frame.Parent = FakeDisconnect
Frame.BackgroundColor3 = Color3.new(0,0,0)
Frame.Transparency = 0.5
Frame.BorderColor3 = Color3.new(1,1,1)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0,0,-0.2)
Frame.Size = UDim2.new(1,0,1.2)
Frame.Active = true
Frame.Draggable = false

Frame1.Parent = Frame
Frame1.BackgroundColor3 = Color3.fromRGB(35,35,35)
Frame1.BorderColor3 = Color3.new(1,1,1)
Frame1.BorderSizePixel = 0
Frame1.Position = UDim2.new(0.27,0,0.28)
Frame1.Size = UDim2.new(0.43,0,0.48)
Frame1.Active = true
Frame1.Draggable = false

Line.Parent = Frame1
Line.BackgroundColor3 = Color3.new(0,0,0)
Line.BorderColor3 = Color3.new(1,1,1)
Line.BorderSizePixel = 2
Line.Position = UDim2.new(0.1,0,0.28)
Line.Size = UDim2.new(0.78,0,0.0000001)
Line.Active = true

Title.Parent = Frame1
Title.BackgroundColor3 = Color3.fromRGB(35,35,35)
Title.BackgroundTransparency = 1
Title.Position = UDim2.new(0.1,0,0.07)
Title.TextColor3 = Color3.new(1,1,1)
Title.Size = UDim2.new(0.8,0,0.15)
Title.Font = Enum.Font.SourceSansLight
Title.FontSize = Enum.FontSize.Size14
Title.TextScaled = true
Title.TextSize = 8
Title.TextWrapped = true

Page1.Parent = Frame1
Page1.BackgroundColor3 = Color3.fromRGB(35,35,35)
Page1.BackgroundTransparency = 1
Page1.Position = UDim2.new(0.1,0,0.34)
Page1.TextColor3 = Color3.new(1,1,1)
Page1.Size = UDim2.new(0.8,0,0.1)
Page1.Font = Enum.Font.SourceSansLight
Page1.FontSize = Enum.FontSize.Size14
Page1.TextScaled = true
Page1.TextSize = 8
Page1.TextWrapped = true

Page2.Parent = Frame1
Page2.BackgroundColor3 = Color3.fromRGB(35,35,35)
Page2.BackgroundTransparency = 1
Page2.Position = UDim2.new(0.1,0,0.43)
Page2.TextColor3 = Color3.new(1,1,1)
Page2.Size = UDim2.new(0.8,0,0.1)
Page2.Font = Enum.Font.SourceSansLight
Page2.FontSize = Enum.FontSize.Size14
Page2.TextScaled = true
Page2.TextSize = 8
Page2.TextWrapped = true

Page3.Parent = Frame1
Page3.BackgroundColor3 = Color3.fromRGB(35,35,35)
Page3.BackgroundTransparency = 1
Page3.Position = UDim2.new(0.1,0,0.55)
Page3.TextColor3 = Color3.new(1,1,1)
Page3.Size = UDim2.new(0.8,0,0.1)
Page3.Font = Enum.Font.SourceSansLight
Page3.FontSize = Enum.FontSize.Size14
Page3.Text = "(Error Code: 267)"
Page3.TextScaled = true
Page3.TextSize = 8
Page3.TextWrapped = true

Bt1.Parent = Frame1
Bt1.BackgroundColor3 = Color3.new(1,1,1)
Bt1.BackgroundTransparency = 0
Bt1.Position = UDim2.new(0.1,0,0.7)
Bt1.TextColor3 = Color3.new(0,0,0)
Bt1.Size = UDim2.new(0.37,0,0.15)
Bt1.Font = Enum.Font.SourceSansLight
Bt1.FontSize = Enum.FontSize.Size14
Bt1.TextScaled = true
Bt1.TextSize = 8
Bt1.TextWrapped = true

Bt2.Parent = Frame1
Bt2.BackgroundColor3 = Color3.new(1,1,1)
Bt2.BackgroundTransparency = 0
Bt2.Position = UDim2.new(0.52,0,0.7)
Bt2.TextColor3 = Color3.new(0,0,0)
Bt2.Size = UDim2.new(0.37,0,0.15)
Bt2.Font = Enum.Font.SourceSansLight
Bt2.FontSize = Enum.FontSize.Size14
Bt2.TextScaled = true
Bt2.TextSize = 8
Bt2.TextWrapped = true

Bt1.MouseButton1Click:connect(function()
FakeDisconnect:Destroy()
--on Button1 Clicked
game:GetService("TeleportService"):Teleport(9872472334)
end)

Bt2.MouseButton1Click:connect(function()
FakeDisconnect:Destroy()
--on Button2 Clicked

end)


---------Filtering Text
Bt1.Text = "Join"
Bt2.Text = "No"

Title.Text = "GhostPlayer"
Page1.Text = "This Script is not Allowed in this Game"
Page2.Text = "Do you want to Teleport in the game Script?"
end
           print("Key is invalid")
        end
    end
})

local Getkey = Tabs.KeySys:AddButton({
    Title = "Get Key",
    Description = "Get Key here",
    Callback = function()
       setclipboard(KeyGuardLibrary.getLink())
    end
})

Window:SelectTab(1)
