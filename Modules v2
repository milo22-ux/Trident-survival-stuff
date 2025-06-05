local modules = {}
for _, v in ipairs(getgc(true)) do
    if typeof(v) == "function" and islclosure(v) then
        local src = debug.info(v, "s")
        local name = debug.info(v, "n")
        if src:find(".BowSpecial") and name == "update" then
            modules.Character = debug.getupvalue(v, 13)
            modules.Camera = debug.getupvalue(v, 15)
            modules.Network = debug.getupvalue(v, 19)
        elseif src:find(".Character") and name == "getGroundCastResult" then
            modules.FPS = debug.getupvalue(v, 2)
            modules.FPS2 = debug.getupvalue(v, 3)
        elseif src:find(".Character") and name == "updateCharacter" then
            modules.Player  = debug.getupvalue(v, 4)
            modules.Player2 = debug.getupvalue(v, 6)
            modules.Player3 = debug.getupvalue(v, 14)
            modules.Player4 = debug.getupvalue(v, 15)
            modules.Player5 = debug.getupvalue(v, 21)
            modules.Player6 = debug.getupvalue(v, 28)
            modules.Player7 = debug.getupvalue(v, 32)
        end
    end
end
--
local OsClock = os.clock()
local drawing = getgenv().Drawing
local workspace,camera = cloneref(game:GetService("Workspace")),workspace.CurrentCamera
local UIS, RS, ReplicatedStorage = cloneref(game:GetService("UserInputService")), cloneref(game:GetService("RunService")), cloneref(game:GetService("ReplicatedStorage"))
