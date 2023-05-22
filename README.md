local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "demon slayer tower defense simulator", HidePremium = false, lntroText = "Goldenhub", SaveConfig = true, ConfigFolder = "OrionTest"})

local Tab = Window:MakeTab({
	Name = "OP script",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})


OrionLib:MakeNotification({
	Name = "",
	Content = "ขอให้สนุก🥰",
	Image = "rbxassetid://4483345998",
	Time = 5
})


Tab:AddButton({
	Name = "KII ALL",
	Callback = function()
      	  -- Variables
local code = require(game.ReplicatedStorage.DataSource.EnumType).clientRemoteEvent.DamageMonster
local unit = (function()
    for i,v in pairs(workspace.PlaceHero:GetChildren()) do
        if v.Name:find(game.Players.LocalPlayer.Name) and not v.Name:find("Doctor") then
            return v.Name
        end
    end
end)()
 
-- Yes
while true do
    for i,v in pairs(workspace.Monsters:GetChildren()) do
        game.ReplicatedStorage.RemoteEvent["RemoteEvent_Notice"]:FireServer(code, {unit,{v}})
    end
    wait()
end
  	end    
})

