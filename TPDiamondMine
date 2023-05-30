repeat wait() until not game.Players.LocalPlayer.PlayerGui:FindFirstChild("__INTRO")

local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Library = require(ReplicatedStorage:WaitForChild("Library"))
local Client = require(ReplicatedStorage:WaitForChild("Library"):WaitForChild("Client"))
local Audio = require(ReplicatedStorage:WaitForChild("Library"):WaitForChild("Audio"))
local Network = Client.Network


hookfunction(debug.getupvalue(Network.Fire, 1) , function(...) return true end)
hookfunction(debug.getupvalue(Network.Invoke, 1) , function(...) return true end)

hookfunction(Audio.Play, function(...)
    return {
        Play = function() end,
        Stop = function() end,
        IsPlaying = function() return false end
    }
end)



function attemptTeleport()
    if Library.WorldCmds.Get() ~= "Diamond Mine" and Library.WorldCmds.HasArea("Diamond Mine") then
        Library.WorldCmds.Load("Diamond Mine")
    end
end

attemptTeleport()
