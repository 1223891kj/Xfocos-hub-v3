-- ORION MOBILE SOLA
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/Kiwilegazin/Orion-mobile-v2/refs/heads/main/README.md')))()

-- LA ELE RECEBA CASCA DE BALA 
local Window = OrionLib:MakeWindow({
    Name = "😈xfocos hub v3🥶",
    HidePremium = false,
    SaveConfig = true,
    ConfigFolder = "OrionTest",
    IntroEnabled = false
})

-- NOSAAA
local Tab1 = Window:MakeTab({
    Name = "👨‍💻SCRIPTS👨‍💻",
    Icon = "rbxassetid://138553129773125",
    PremiumOnly = false
})

-- AI MEU CU
Tab1:AddTextbox({
    Name = "🤑COLOQUE SEU SCRIPT AQUI.🤑",
    Default = "",
    TextDisappear = false,
    Callback = function(text)
        _G.scriptCode = text
    end
})

-- BRUH
Tab1:AddButton({
    Name = "📄EXECUTAR O SCRIPT QUE TU COLOCOU.📄",
    Callback = function()
        if _G.scriptCode and _G.scriptCode ~= "" then
            local func = loadstring(_G.scriptCode)
            if func then
                func()
            else
                print("Erro ao carregar o script.")
            end
        else
            print("Bota o caralho do script certo.")
        end
    end
})

-- SCRIPTS FICA NESSE CARALHO

Tab1:AddButton({
    Name = "🤑ESP🤑",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/1223891kj/Esp-/refs/heads/main/README.md"))()
    end
})

Tab1:AddButton({
    Name = "🕹️SANDER X🕹️",
    Callback = function()
        loadstring(game:HttpGet('https://rawscripts.net/raw/Brookhaven-RP-Sander-X-Hub-Latest-Version-3-16718'))()
    end
})

Tab1:AddButton({
    Name = "✈️FLY GUI✈️",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Brookhaven-andx1F3E1RP-Fly-Gui-15924"))()
    end
})

Tab1:AddButton({
    Name = "💰WALK FLING(SOMENTE EM MAPAS COM COLISÃO DE PLAYERS)💰",
    Callback = function()
       loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Walk-Fling-Script-18573"))()
    end
})

Tab1:AddButton({
    Name = "📄INFINITE YIELD📄",
    Callback = function()
       loadstring(game:HttpGet("https://rawscripts.net/raw/Infinite-Yield_500"))()
    end
})

Tab1:AddButton({
    Name = "🌐TROLL GUI🌐",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Troll-Gui-3874"))()
    end
})

-- PEGA NO MEU PAL
local Tab2 = Window:MakeTab({
    Name = "🥳LAG SERVER/TOOLS🥳",
    Icon = "rbxassetid://127522669208877",
    PremiumOnly = false
})

Tab2:AddButton({
    Name = "🍖Equipar Todos os Itens🍖",
    Callback = function()
        equipAllItems()
    end
})
Tab2:AddButton({
    Name = "👨‍🔬TELEPORT TOOL👨‍🔬",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Teleport-Tool-27419"))()
    end
})

Tab2:AddButton({
    Name = "🤑TELEKINIS🤑",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Fe-Telekinesis-V5-21542"))()
    end
})

Tab2:AddButton({
    Name = "🔥LAG SERVER🔥",
    Callback = function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(500, 50, 500)
        local clickDetector = Instance.new("ClickDetector")
        for i = 1, 5 do
            local basketball = Instance.new("Tool", game.Players.LocalPlayer.Backpack)
            basketball.Name = "Basketball " .. i
            clickDetector.Parent = basketball
        end
        print("Multiplicando basketball até 5 tools")
    end
})

local Tab3 = Window:MakeTab({
    Name = "🤣TROLL🤣",
    Icon = "rbxassetid://111501435575860",
    PremiumOnly = false
})

Tab3:AddButton({
    Name = "🥵FLING🥵",
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/kiwi541/Mr-red-Black-V4/refs/heads/main/README.md'))()
    end
})

Tab3:AddTextbox({
    Name = "🤠TELEPORTE🤠",
    Default = "Digite o nome do jogador",
    TextDisappear = true,
    Callback = function(Value)
        for _, player in pairs(game.Players:GetPlayers()) do
            if string.find(string.lower(player.Name), string.lower(Value)) then
                if player.Character and player.Character:FindFirstChild("HumanoidRootPart") and game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChild("HumanoidRootPart") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = player.Character.HumanoidRootPart.CFrame
                    print("Teleportando para: " .. player.Name)
                    break
                end
            end
        end
    end
})

Tab3:AddButton({
    Name = "🌀UTG🌀",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/1223891kj/Utg/refs/heads/main/README.md"))()
    end
})

Tab3:AddButton({
    Name = "🔪KNIFE🗡️ (FE NO PRISON LIFE)",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-Grab-knife-v4-24753"))()
    end
})

Tab3:AddButton({
    Name = "🔥COOLKID GUI🔥",
    Callback = function()
        loadstring(game:HttpGet("https://pastebin.com/raw/UPZCQ31W"))()
    end
})

Tab3:AddButton({
    Name = "🌊FLING V2 DO XFOCOS🌊",
    Callback = function()
        loadstring(game:HttpGet("https://rawscripts.net/raw/Universal-Script-FE-Fling-GUI-10927"))()
    end
})

local Tab4 = Window:MakeTab({
    Name = "😈TROLL VERSION V1😈",
    Icon = "rbxassetid://118477128531489",
    PremiumOnly = false
})

Tab4:AddButton({
    Name = "🥶ABRIR TROLL V1🥶 (V2 SENDO FEITA!)",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/1223891kj/Xfocos-Hub-troll/refs/heads/main/README.md"))()
    end
})

local Tab4 = Window:MakeTab({
    Name = "😈TROLL VERSION V2 (AMOSTRA)😈",
    Icon = "rbxassetid://118477128531489",
    PremiumOnly = false
})

Tab4:AddButton({
    Name = "😎ABRIR TROLL V2😎 (AMOSTRA DA V2!)",
    Callback = function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/1223891kj/Troll-V2-/refs/heads/main/README.md"))()
    end
})

local Tab5 = Window:MakeTab({
    Name = "💀SERVER INFO/REJOIN💀",
    Icon = "rbxassetid://88858899538480",
    PremiumOnly = false
})

Tab5:AddButton({
    Name = "⚠️REJOIN⚠️",
    Callback = function()
        game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
    end
})

local showModels = true

Tab5:AddButton({
    Name = "🏠Mostrar Modelos🏠",
    Callback = function()
        showModels = not showModels
        if showModels then
            for _, model in pairs(workspace:GetChildren()) do
                if model:IsA("Model") then
                    print("Modelo: " .. model.Name .. " - Criador: " .. tostring(model.Creator))
                end
            end
        else
            print("Exibição de modelos desligada")
        end
    end
})

local Tab6 = Window:MakeTab({
    Name = "🧠CORPO🧠",
    Icon = "rbxassetid://83307165845406",
    PremiumOnly = false
})

local spinning = false

Tab6:AddButton({
    Name = "🌀Ativar Spin🌀",
    Callback = function()
        spinning = true
        while spinning do
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.Angles(0, math.rad(10), 0)
            wait(0.1)
        end
        print("Spin ativado")
    end
})

Tab6:AddButton({
    Name = "💣Desativar Spin💣",
    Callback = function()
        spinning = false
        print("Spin desativado")
    end
})

local speed = 16
local jumpPower = 50

Tab6:AddTextbox({
    Name = "Velocidade",
    Default = tostring(speed),
    TextDisappear = false,
    Callback = function(text)
        local newSpeed = tonumber(text)
        if newSpeed then
            speed = newSpeed
            game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = speed
            print("Velocidade alterada para: " .. speed)
        else
            print("Por favor, insira um valor numérico válido para a velocidade.")
        end
    end
})

-- Botão Anti Sit
Tab6:AddButton({
    Name = "🪑ANTI SIT🪑",
    Callback = function()
        local humanoid = game.Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            humanoid.Sit = false
            humanoid.Changed:Connect(function(property)
                if property == "Sit" then
                    humanoid.Sit = false
                end
            end)
            print("Anti Sit ativado")
        end
    end
})

-- Botão para voltar a conseguir sentar
Tab6:AddButton({
    Name = "🪑VOLTAR A CONSEGUIR SENTAR🪑",
    Callback = function()
        local humanoid = game.Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
        if humanoid then
            humanoid.Changed:Connect(function() end) -- Para remover o bloqueio de sentar
            print("Agora você pode sentar novamente")
        end
    end
})

Tab6:AddTextbox({
    Name = "Pulo",
    Default = tostring(jumpPower),
    TextDisappear = false,
    Callback = function(text)
        local newJumpPower = tonumber(text)
        if newJumpPower then
            jumpPower = newJumpPower
            game.Players.LocalPlayer.Character.Humanoid.JumpPower = jumpPower
            print("Pulo alterado para: " .. jumpPower)
        else
            print("Por favor, insira um valor numérico válido para o pulo.")
        end
    end
})

function equipAllItems()
    local character = game.Players.LocalPlayer.Character
    if character and character:FindFirstChildOfClass("Humanoid") then
        local humanoid = character:FindFirstChildOfClass("Humanoid")
        for i, tool in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
            if tool:IsA("Tool") then
                humanoid:EquipTool(tool)
                print("Item equipado: " .. tool.Name)
            end
        end
    else
        print("Personagem não encontrado ou não possui um Humanoid.")
    end
end

local Tab7 = Window:MakeTab({
    Name = "🤳TIK TOK🤳",
    Icon = "rbxassetid://133426623974922",
    PremiumOnly = false
})

Tab7:AddButton({
    Name = "👨‍💻TIK TOK DO XFOCOS👨‍💻",
    Callback = function()
        setclipboard("DJ_XFOCOS")
    end
})

Tab7:AddButton({
    Name = "😈YOUTUBE DO XFOCOS😈",
    Callback = function()
        setclipboard("@Dj_dhthais")
    end
})

Tab7:AddButton({
    Name = "🤪POLICE BROOKHAVEN OFC🤪",
    Callback = function()
        setclipboard("policebrookhavenofficial")
    end
})

Tab7:AddButton({
    Name = "👨‍💻MR POLICE👨‍💻",
    Callback = function()
        setclipboard("policebrookhaven99")
    end
})

local Tab8 = Window:MakeTab({
    Name = "👨‍💻OWNER SCRIPT👨‍💻",
    Icon = "rbxassetid://108619014641303",
    PremiumOnly = false
})

Tab8:AddLabel("🎩THE MR RED BLACK OWNER🎩")
Tab8:AddLabel("💀MOLENGA COM CASPA💀")
Tab8:AddLabel("🥵MR POLICE🥵")
Tab8:AddLabel("👨‍🔬SR NESCAU👨‍🔬")
Tab8:AddLabel("👨‍💻FRAGIOTA👨‍💻")
Tab8:AddLabel("🤖CHATGPT AI🤖")
Tab8:AddLabel("🤖BING AI🤖")
Tab8:AddLabel("🤣XFOCOS THAIS CARLA🤣")


local Tab9 = Window:MakeTab({
    Name = "⚙️NOVIDADES⚙️",
    Icon = "rbxassetid://79994606808372",
    PremiumOnly = false
})

Tab9:AddLabel("O Xfocos hub v4, vai vir com a troll version v2!")
Tab9:AddLabel("Xfocos hub v4 vai ter muito mais abas e opções!")
Tab9:AddLabel("Está gostando do xfocos hub v3? então me siga no ttk!")

local Tab10 = Window:MakeTab({
    Name = "👮‍♂️PRISON LIFE HUB👮‍♂️",
    Icon = "rbxassetid://74896161958894",
    PremiumOnly = false
})

Tab10:AddButton({
    Name = "🔥PRIZZLIFE SCRIPT🔥",
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/elliexmln/PrizzLife/main/pladmin.lua'))()
    end
})
