-- Fetch and initialize the Orion UI framework
local OrionLib = loadstring(game:HttpGet(('https://githubusercontent.com')))()

-- Send a custom notification upon successful injection
OrionLib:MakeNotification({
    Name = "K1NG Hub Activated",
    Content = "Welcome back. System initialized successfully.",
    Image = "rbxassetid://4483345998",
    Time = 5
})

-- Create the primary window interface
local Window = OrionLib:MakeWindow({
    Name = "K1NG Hub | made by K1NG", 
    HidePremium = false, 
    SaveConfig = true, 
    ConfigFolder = "K1NGHubConfigs"
})

-- =================================================================
-- TAB 1: TOOLS & UTILITIES
-- =================================================================
local MainTab = Window:MakeTab({
    Name = "Utilities",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

MainTab:AddButton({
    Name = "Execute SimpleSpy (Remote Spy)",
    Callback = function()
        loadstring(game:HttpGet("https://github.com"))()
    end    
})

MainTab:AddButton({
    Name = "Execute Infinite Yield (Admin)",
    Callback = function()
        loadstring(game:HttpGet('https://githubusercontent.com'))()
    end    
})

-- =================================================================
-- TAB 2: PLAYER MODIFICATIONS
-- =================================================================
local PlayerTab = Window:MakeTab({
    Name = "Player Mods",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

-- Dynamic slider to scale player movement speed safely
PlayerTab:AddSlider({
    Name = "Movement Speed (WalkSpeed)",
    Min = 16,
    Max = 200,
    Default = 16,
    Color = Color3.fromRGB(0, 170, 255),
    Increment = 1,
    ValueName = "Studs/sec",
    Callback = function(Value)
        local character = game.Players.LocalPlayer.Character
        if character and character:FindFirstChildOfClass("Humanoid") then
            character:FindFirstChildOfClass("Humanoid").WalkSpeed = Value
        end
    end    
})

-- Toggle loop configuration for continuous jumping
local InfJumpState = false
PlayerTab:AddToggle({
    Name = "Enable Infinite Jump",
    Default = false,
    Callback = function(Value)
        InfJumpState = Value
    end
})

-- Network event listener linking the physics state to the toggle
game:GetService("UserInputService").JumpRequest:Connect(function()
    if InfJumpState then
        local character = game.Players.LocalPlayer.Character
        if character and character:FindFirstChildOfClass('Humanoid') then
            character:FindFirstChildOfClass('Humanoid'):ChangeState("Jumping")
        end
    end
end)

-- =================================================================
-- TAB 3: CREDITS & INFO
-- =================================================================
local CreditsTab = Window:MakeTab({
    Name = "Credits",
    Icon = "rbxassetid://4483345998",
    PremiumOnly = false
})

CreditsTab:AddParagraph("Owner & Developer", "This entire script hub was created and compiled by K1NG.")
CreditsTab:AddParagraph("Version Status", "Version 1.0.0 - Fully Functional.")

-- Initialize and display the completed interface layout
OrionLib:Init()
