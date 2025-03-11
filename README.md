local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local Window = Rayfield:CreateWindow({
   Name = "OXMOHA",
   Icon = 4483362458, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "WELCOME TO OXMOHA ",
   LoadingSubtitle = "by MOHA",
   Theme = "DarkBlue", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "MUSCLE LEGEND "
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = true, -- Set this to true to use our key system
   KeySettings = {
      Title = "ENTER KEY",
      Subtitle = "Key System",
      Note = "KEY IS MOHAx1", -- Use this to tell the user how to get a key
      FileName = ".", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = false, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"MOHAx1"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local HomeTab = Window:CreateTab("Home", 4483362458) -- Title, Image
HomeTab:CreateParagraph({Title = "Welcome", Content = "Welcome to the Muscle Legends Script!"})
HomeSection:CreateLabel("CREATED BY [MOHA]") 
HomeSection:CreateLabel("THIS IS V 1.0")



local MainTab = Window:CreateTab("MAIN", "rewind")
MainTab:CreateToggle({
    Name = "Auto Train",
    CurrentValue = false,
    Flag = "AutoTrain",
    Callback = function(Value)
        if Value then
            -- Auto Train Code Here
        else
            -- Stop Auto Train Code Here
        end
    end
})






local Tab = Window:CreateTab("REBIRTH", "rewind")
RebirthTab:CreateButton({
    Name = "Rebirth",
    Callback = function()
        -- Rebirth Code Here
    end
})





local Tab = Window:CreateTab("EGGS", "rewind")
EggsTab:CreateDropdown({
    Name = "Select Egg",
    Options = {"Basic Egg", "Rare Egg", "Epic Egg"},
    CurrentOption = "Basic Egg",
    Flag = "SelectedEgg",
    Callback = function(Option)
        -- Select Egg Code Here
    end
})

local TeleportTab = Window:CreateTab("Teleport", "rewind")
TeleportTab:CreateButton({
    Name = "Gym",
    Callback = function()
        -- Teleport to Gym Code Here
    end
})
TeleportTab:CreateButton({
    Name = "Beach",
    Callback = function()
        -- Teleport to Beach Code Here
    end
})

local GraphicsTab = Window:CreateTab("Graphics", 4483362458)
GraphicsTab:CreateSlider({
    Name = "Graphics Quality",
    Range = {1, 10},
    Increment = 1,
    Suffix = "",
    CurrentValue = 5,
    Flag = "GraphicsQuality",
    Callback = function(Value)
        -- Set Graphics Quality Code Here
    end
})
GraphicsTab:CreateToggle({
    Name = "Toggle Shadows",
    CurrentValue = false,
    Flag = "ToggleShadows",
    Callback = function(Value)
        -- Toggle Shadows Code Here
    end
})


Rayfield:LoadConfiguration()
