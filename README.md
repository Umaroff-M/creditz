# creditz
local InsertService = game:GetService("InsertService")
local Workspace = game:GetService("Workspace")

local webURL = "https://www.roblox.com/catalog/1804747/White-Shirt"
local assetId = tonumber(string.match(webURL, "%d+") or 0)  -- Extract the number
local success, model = pcall(function()
	return InsertService:LoadAsset(assetId)
end)
if success then
	model.Parent = Workspace
end
