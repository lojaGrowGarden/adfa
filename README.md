local Rayfield = loadstring(game:HttpGet("https://sirius.menu/rayfield"))()

local Window = Rayfield:CreateWindow({
   Name = "Hebreus Hub",
   LoadingTitle = "Carregando interface",
   LoadingSubtitle = "by anonimo",
   Theme = "Amethyst",
})

local Tab = Window:CreateTab("Main", 4483362458)

-- SUPER VELOCIDADE
Tab:CreateToggle({
   Name = "Super Velocidade",
   CurrentValue = false,
   Flag = "SpeedToggle",
   Callback = function(Value)
      local humanoid = game.Players.LocalPlayer.Character.Humanoid
      if Value then
         humanoid.WalkSpeed = 50
      else
         humanoid.WalkSpeed = 16
      end
   end,
})

-- SUPER PULO
Tab:CreateToggle({
   Name = "Super Pulo",
   CurrentValue = false,
   Flag = "JumpToggle",
   Callback = function(Value)
      local humanoid = game.Players.LocalPlayer.Character.Humanoid
      if Value then
         humanoid.JumpPower = 150
      else
         humanoid.JumpPower = 50
      end
   end,
})

-- FAST ATTACKS
Tab:CreateToggle({
   Name = "Fast Attacks",
   CurrentValue = false,
   Flag = "FastAttacks",
   Callback = function(Value)
      _G.FastAttacks = Value
   end,
})
