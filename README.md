# Prompts

#PromptEvents

local ProximityPromptService = game:GetService("ProximityPromptService")
local ServerScriptService = game:GetService("ServerScriptService")
local ObjectActions = require(ServerScriptService.ObjectActions)

local function onPromptTriggered(promptObject, player)
	ObjectActions.promptTriggeredActions(promptObject, player)
end


local function onPromptHoldBegan(promptObject, player)
	ObjectActions.promptHoldBeganActions(promptObject, player)
end

local function onPromptHoldEnded(promptObject, player)
	 ObjectActions.promptHoldEndedActions(promptObject, player)
end



ProximityPromptService.PromptTriggered:Connect(onPromptTriggered)
ProximityPromptService.PromptButtonHoldBegan:Connect(onPromptHoldBegan)
ProximityPromptService.PromptButtonHoldEnded:Connect(onPromptHoldEnded)



Video Tutorial: https://www.youtube.com/watch?v=6wZLOqdPcAo

