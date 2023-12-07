--[[

       /$$                      /$$       /$$                                            
      | $$                     |__/      | $$                                            
  /$$$$$$$  /$$$$$$  /$$    /$$ /$$  /$$$$$$$ /$$  /$$  /$$  /$$$$$$   /$$$$$$   /$$$$$$ 
 /$$__  $$ |____  $$|  $$  /$$/| $$ /$$__  $$| $$ | $$ | $$ |____  $$ /$$__  $$ /$$__  $$
| $$  | $$  /$$$$$$$ \  $$/$$/ | $$| $$  | $$| $$ | $$ | $$  /$$$$$$$| $$  \__/| $$$$$$$$
| $$  | $$ /$$__  $$  \  $$$/  | $$| $$  | $$| $$ | $$ | $$ /$$__  $$| $$      | $$_____/
|  $$$$$$$|  $$$$$$$   \  $/   | $$|  $$$$$$$|  $$$$$/$$$$/|  $$$$$$$| $$      |  $$$$$$$
 \_______/ \_______/    \_/    |__/ \_______/ \_____/\___/  \_______/|__/       \_______/                                                                                                                                                                                                                                                                         

]]--


-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local big = Instance.new("Frame")
local line = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local UITextSizeConstraint = Instance.new("UITextSizeConstraint")
local TextBox = Instance.new("TextBox")

--Properties:

ScreenGui.Parent = game.Workspace
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ScreenGui.ResetOnSpawn = false

big.Name = "big"
big.Parent = ScreenGui
big.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
big.BackgroundTransparency = 0.750
big.BorderColor3 = Color3.fromRGB(0, 0, 0)
big.BorderSizePixel = 0
big.Position = UDim2.new(0.416002452, 0, 0.267719805, 0)
big.Size = UDim2.new(0.182386667, 0, 0.462962955, 0)

line.Name = "line"
line.Parent = big
line.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
line.BorderColor3 = Color3.fromRGB(0, 0, 0)
line.BorderSizePixel = 0
line.Position = UDim2.new(0.068571426, 0, 0.152139157, 0)
line.Size = UDim2.new(0.860000014, 0, -0.00800000038, 0)

TextLabel.Parent = big
TextLabel.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(0.214285716, 0, 0.0240000002, 0)
TextLabel.Size = UDim2.new(0.571428597, 0, 0.100000001, 0)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "davidware"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 59.000
TextLabel.TextWrapped = true

UITextSizeConstraint.Parent = TextLabel
UITextSizeConstraint.MaxTextSize = 59

TextBox.Parent = big
TextBox.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextBox.BackgroundTransparency = 0.750
TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextBox.BorderSizePixel = 0
TextBox.Position = UDim2.new(0.068571426, 0, 0.84526968, 0)
TextBox.Size = UDim2.new(0, 300, 0, 62)
TextBox.Font = Enum.Font.SourceSans
TextBox.PlaceholderColor3 = Color3.fromRGB(177, 177, 177)
TextBox.PlaceholderText = "player name here"
TextBox.Text = ""
TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TextBox.TextSize = 36.000

-- Scripts:

local function XCWUB_fake_script() -- TextLabel.LocalScript 
	local script = Instance.new('LocalScript', TextLabel)

	while true do
	
		script.Parent.TextColor3 = Color3.new(255/255,0/255,0/255)
	
		for i = 0,255,10 do
	
			wait()
	
			script.Parent.TextColor3 = Color3.new(255/255,i/255,0/255)
	
		end
	
		for i = 255,0,-10 do
	
			wait()
	
			script.Parent.TextColor3 = Color3.new(i/255,255/255,0/255)
	
		end
	
		for i = 0,255,10 do
	
			wait()
	
			script.Parent.TextColor3 = Color3.new(0/255,255/255,i/255)
	
		end
	
		for i = 255,0,-10 do
	
			wait()
	
			script.Parent.TextColor3 = Color3.new(0/255,i/255,255/255)
	
		end
	
		for i = 0,255,10 do
	
			wait()
	
			script.Parent.TextColor3 = Color3.new(i/255,0/255,255/255)
	
		end
	
		for i = 255,0,-10 do
	
			wait()
	
			script.Parent.TextColor3 = Color3.new(255/255,0/255,i/255)
	
		end
	
	end
end
coroutine.wrap(XCWUB_fake_script)()
local function RDIOBW_fake_script() -- ScreenGui.drag 
	local script = Instance.new('LocalScript', ScreenGui)

	local UIS = game:GetService('UserInputService')
	local frame = script.Parent.big
	local dragToggle = nil
	local dragSpeed = 0.25
	local dragStart = nil
	local startPos = nil
	
	local function updateInput(input)
		local delta = input.Position - dragStart
		local position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X,
			startPos.Y.Scale, startPos.Y.Offset + delta.Y)
		game:GetService('TweenService'):Create(frame, TweenInfo.new(dragSpeed), {Position = position}):Play()
	end
	
	frame.InputBegan:Connect(function(input)
		if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) then 
			dragToggle = true
			dragStart = input.Position
			startPos = frame.Position
			input.Changed:Connect(function()
				if input.UserInputState == Enum.UserInputState.End then
					dragToggle = false
				end
			end)
		end
	end)
	
	UIS.InputChanged:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
			if dragToggle then
				updateInput(input)
			end
		end
	end)
end
coroutine.wrap(RDIOBW_fake_script)()
local function EAHXS_fake_script() -- ScreenGui.perm 
	local script = Instance.new('LocalScript', ScreenGui)

	if game.Players.LocalPlayer.Name == "davidpuiu15" then
		script.Parent.big.Visible = true
	else
		script.Parent.big.Visible = false
	end
end
coroutine.wrap(EAHXS_fake_script)()
