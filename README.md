if game.PlaceId ~= 537413528 then
    return
end

task.spawn(function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/TranMyNhi/TranMyNhi/refs/heads/main/isseua'))()
end)

if not isfolder("BABFT") then
    makefolder("BABFT")
end

if not isfolder("BABFT/Image") then
    makefolder("BABFT/Image")
end

if not isfolder("BABFT/Build") then
    makefolder("BABFT/Build")
end

local FcMaster = true
local folderName = "ImagePreview"
local previewFolder = Workspace:FindFirstChild(folderName) or Instance.new("Folder", Workspace)
previewFolder.Name = folderName

for _, v in ipairs(previewFolder:GetChildren()) do
    v:Destroy()
end

task.delay(10, function()
    if game:GetService("CoreGui"):FindFirstChild("MSGISSUE") then
        game:GetService("CoreGui").MSGISSUE:Destroy()
    end
end)

local Rayfield
local success

success, Rayfield = pcall(function()
    return loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
end)

if not success then
    success, Rayfield = pcall(function()
        return loadstring(game:HttpGet('https://raw.githubusercontent.com/SiriusSoftwareLtd/Rayfield/ab965bf9a6f9890e6447c9b377678f5bffd8a379/source.lua'))()
    end)
end

if not success then
    success, Rayfield = pcall(function()
        return loadstring(game:HttpGet('https://github.com/SiriusSoftwareLtd/Rayfield/blob/28c7c270669c16a2ae1526eaaac1dbf927aa881e/source.lua'))()
    end)
end

local HttpService = cloneref(game:GetService("HttpService"))
local TeleportService = cloneref(game:GetService("TeleportService"))
local Players = game:GetService("Players")
local Workspace = game:GetService("Workspace")
local VirtualUser = game:GetService("VirtualUser")
local httprequest = (syn and syn.request) or (http and http.request) or http_request or (fluxus and fluxus.request) or request
local JobId = game.JobId
local PlaceId = game.PlaceId
local queueteleport = (syn and syn.queue_on_teleport) or queue_on_teleport or (fluxus and fluxus.queue_on_teleport)
local RunService = game:GetService("RunService")

local Window = Rayfield:CreateWindow({
    Name = "Mouse Hub🇻🇳",
    Icon = 85108798400826,
    LoadingTitle = "Mouse Hub🇻🇳",
    LoadingSubtitle = "Made With Mouse Hub",
    Theme = "BlackBlue",
 
    DisableRayfieldPrompts = true,
    DisableBuildWarnings = true,
 
    ConfigurationSaving = {
       Enabled = false,
       FolderName = nil,
       FileName = "Big Hub"
    },
 
    Discord = {
       Enabled = true,
       Invite = "3eyRTcsn",
       RememberJoins = true
    },
 
    KeySystem = true,
    KeySettings = {
       Title = "discord.gg/3eyRTcsn",
       Subtitle = "Mouse Hub",
       Note = "Hãy Vào Discord Để Lấy Mật Khẩu",
       FileName = "ASUBABFTKey",
       SaveKey = true,
       GrabKeyFromSite = false,
       Key = {"MouseHub"} -- yes there is a keysystem but my script is not obfuscated lol
    }
})

local Global = Window:CreateTab("Cày Tiền", 125428076789049)
local ImageLoader = Window:CreateTab("Tải Ảnh", 91865122737183)
local AutoBuild = Window:CreateTab("Tự Build", 128207976113050)
local BlockNeeded = Window:CreateTab("Cần Block", 138460602231983)
local Miscellaneous = Window:CreateTab("Chức Năng Cá Nhân", 90305619538335)
local Information = Window:CreateTab("Mô Tả", 84130531909418)
local Credit = Window:CreateTab("Tác Giả", 103654977021797)

local Section = Credit:CreateSection("Discord")
Section = Information:CreateSection("Discord")

local Button = Credit:CreateButton({
    Name = "Tham Gia Discord",
    Callback = function()
        setclipboard("https://discord.gg/3eyRTcsn")
        Rayfield:Notify({
            Title = "Sao Chép!",
            Content = "Sao Chép Thành Công",
            Duration = 6.5,
            Image = 124144713366592,
         })
    end,
 })

local yjdtjf = Global:CreateButton({
    Name = "Dừng HUB",
    Callback = function()
        for _, v in ipairs(previewFolder:GetChildren()) do
            v:Destroy()
    end
        FcMaster = false
        Rayfield:Destroy()
        local GameStuff = {
            "Blocks",
            "Challenge",
            "TempStuff",
            "Teams",
            "MainTerrain",
            "OtherStages",
            "BlackZone",
            "CamoZone",
            "MagentaZone",
            "New YellerZone",
            "Really blueZone",
            "Really redZone",
            "Sand",
            "Water",
            "WhiteZone",
            "WaterMask"
        }
            for _, v in ipairs(GameStuff) do
                local object = game:GetService("ReplicatedStorage"):FindFirstChild(v)
                if object then
                    if v == "OtherStages" then
                        game:GetService("ReplicatedStorage").OtherStages.Parent = workspace.BoatStages
                    else
                        object.Parent = workspace
                    end
                end
            end
    end,
 })

local qzdqzd = Global:CreateDivider()

Section = Credit:CreateSection("owner")

local Labeld = Credit:CreateLabel("Chủ: @Mukino_machiru-Trần Mỹ Nhi", 93981953300699, Color3.fromRGB(204, 153, 255), true)

local Paragraph = Credit:CreateParagraph({Title = "Thông Báo", Content = "HUB Có vấn đề tham gia discord để được hỗ trợ"})

 local aButton = Information:CreateButton({
    Name = "Tham Gia Discord",
    Callback = function()
        setclipboard("https://discord.gg/3eyRTcsn")
        Rayfield:Notify({
            Title = "Copy!",
            Content = "Copy Thành Công",
            Duration = 6.5,
            Image = 124144713366592,
         })
    end,
 })

Section = Information:CreateSection("Auto Farm")
local Paragraph = Information:CreateParagraph({Title = "Thông Báo!!!", Content = "hãy cho tôi biết nếu bạn từng thấy một cày tự động nào xịn hơn cày tiền này về tiền vàng mỗi giờ, bạn có thể sử dụng webhook để theo dõi số liệu thống kê về cày tự động khi bạn không ngồi trước màn hình 😘.\n\n - Không Tăng: 20K/Giờ\n - Tăng x1.25: 25K/Giờ\n - Tăng x2: 40K/Giờ\n - Gamepass: 50k/Giờ"})
Section = Information:CreateSection("Tải Ảnh")
local Paragraph = Information:CreateParagraph({Title = "Yêu cầu", Content = "Dán URL hình ảnh vào hộp văn bản và để máy chủ chuyển đổi hình ảnh, máy chủ không thể truy cập một số hình ảnh nhất định (không phải là vấn đề về mã hóa) HOẶC bạn có thể tự chuyển đổi hình ảnh: (sẽ cung cấp thêm hình ảnh)Hình ảnh được tạo từ các tệp chứa dữ liệu đặc biệt (RGB), để có các tệp này hoặc để tạo tệp của riêng bạn từ hình ảnh mà bạn đã chọn, bạn phải tham gia discord, bạn cần một tập lệnh bên ngoài.\n\n - Tốc độ xây dựng: Bạn có thể chọn tốc độ mà hình ảnh được xây dựng. Nếu bạn có kết nối internet chậm, hãy đặt tốc độ ở mức thấp. Không đặt ở mức tối đa đối với hình ảnh lớn\n\n- Xem trước: Hiển thị bản xem trước của hình ảnh, giúp sử dụng các trình sửa đổi dễ dàng hơn hoặc xem hình ảnh sẽ trông như thế nào. Nó cũng cần thiết để xây dựng hình ảnh.\n\n- Thay đổi tốc độ: Dừng quá trình hiện tại bằng cách mở kho đồ của bạn và kiểm tra xem không còn khối nào được đặt nữa. Thay đổi tốc độ và nhấn 'Tải hình ảnh' một lần nữa. Nó sẽ tự động tiếp tục từ.\n\n- Chế độ tối ưu hóa: Cho phép ngay cả những máy tính yếu nhất hoặc những máy tính không có kết nối tốt cũng có thể tải hình ảnh."})
local Button = Information:CreateButton({
    Name = "sao chép danh sách các trang web đang hoạt động",
    Callback = function()
        setclipboard("https://www.pythonanywhere.com/whitelist/")
        Rayfield:Notify({
            Title = "Copy!",
            Content = "Dùng Link Trên Google Hoặc File Có Sẵn Trên Máy",
            Duration = 6.5,
            Image = 124144713366592,
         })
    end,
 })
Section = Information:CreateSection("Auto Build")
local Paragraph = Information:CreateParagraph({Title = "Thông Tin- [XÂY DỰNG TỰ ĐỘNG ĐANG ĐƯỢC TIẾN HÀNH]", Content = "Tính năng này không yêu cầu bất kỳ yêu cầu bên ngoài nào, nếu bạn lưu bản dựng với tên đã tồn tại, nó sẽ ghi đè lên.\n\n - Bạn có thể tải xuống và chia sẻ tệp trong Máy chủ Discord.\n\n - An toàn: ngăn chặn sự cố trong khi tải nếu bạn có kết nối internet kém, nút chuyển đổi này sẽ làm chậm tốc độ xây dựng.\n\n - Xem trước: hiển thị bản xem trước của bản dựng."})

local player = game.Players.LocalPlayer
local Nplayer = game.Players.LocalPlayer.Name

local characterConnection
local connection

local function enableAntiAFK()
    if not connection then
        Rayfield:Notify({
            Title = "Anti-Afk | ON",
            Content = "Sẽ Không Bị Văng Khi Treo Quá 20 Phút",
            Duration = 6.5,
            Image = 124144713366592,
         })
        connection = player.Idled:Connect(function()
            if getgenv().afk6464 then
                VirtualUser:CaptureController()
                VirtualUser:ClickButton2(Vector2.new())
            end
        end)
    end
end

local function disableAntiAFK()
    if connection then
        connection:Disconnect()
        connection = nil
        Rayfield:Notify({
            Title = "Anti-Afk | OFF",
            Content = "AFK Quá 20 Phút Có Thể Văng",
            Duration = 6.5,
            Image = 124144713366592,
         })
    end
end

local function loop()
    while true do
        if getgenv().afk6464 then
            enableAntiAFK()
        else
            disableAntiAFK()
        end
        wait(1)
    end
end

spawn(loop)

Section = Global:CreateSection("Utilities")
local AFKToggle = Global:CreateToggle({
    Name = "Anti-Afk",
    CurrentValue = false,
    Flag = "",
    Callback = function(Value)
        getgenv().afk6464 = Value
    end,
})

if getgenv().afk6464 == true then
    AFKToggle:Set(true)
end

local Button = Global:CreateButton({
    Name = "Tải Infinite Yield",
    Callback = function()
        loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
    end,
})

local Button = Global:CreateButton({
    Name = "Nút Dịch Chuyển",
    Callback = function()
        mouse = game.Players.LocalPlayer:GetMouse()
        tool = Instance.new("Tool")
        tool.RequiresHandle = false
        tool.Name = "Dịch Chuyển♥"
        tool.ToolTip = "Equip + click = tp"
        tool.Activated:connect(function()
        local pos = mouse.Hit+Vector3.new(0,2.5,0)
        pos = CFrame.new(pos.X,pos.Y,pos.Z)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
        end)
        tool.Parent = game.Players.LocalPlayer.Backpack
    end,
})

local Button = Global:CreateButton({ -- From IY
    Name = "Rejoin",
    Callback = function()
        Rayfield:Notify({
            Title = "Rejoin",
            Content = "hold on a sec",
            Duration = 6.5,
            Image = 124144713366592,
         })
         wait(0.2)
        if #Players:GetPlayers() <= 1 then
            Players.LocalPlayer:Kick("\nĐang Vào Lại...")
            wait()
            TeleportService:Teleport(PlaceId, Players.LocalPlayer)
        else
            TeleportService:TeleportToPlaceInstance(PlaceId, JobId, Players.LocalPlayer)
        end
        wait(5)
        Rayfield:Notify({
            Title = "Vào Lại Thất Bại🙁",
            Content = "Thử Sài infinite yield",
            Duration = 6.5,
            Image = 124144713366592,
         })
    end,
})

local Button = Global:CreateButton({ -- From IY by IY devs and NoobSploit
    Name = "Server Hop",
    Callback = function()
        if httprequest then
            Rayfield:Notify({
                Title = "Server Hop",
                Content = "hold on a sec",
                Duration = 6.5,
                Image = 124144713366592,
             })
             wait(0.2)
            local servers = {}
            local req = httprequest({Url = string.format("https://games.roblox.com/v1/games/%d/servers/Public?sortOrder=Desc&limit=100&excludeFullGames=true", PlaceId)})
            local body = HttpService:JSONDecode(req.Body)

            if body and body.data then
                for i, v in next, body.data do
                    if type(v) == "table" and tonumber(v.playing) and tonumber(v.maxPlayers) and v.playing < v.maxPlayers and v.id ~= JobId then
                        table.insert(servers, 1, v.id)
                    end
                end
            end

            if #servers > 0 then
                TeleportService:TeleportToPlaceInstance(PlaceId, servers[math.random(1, #servers)], Players.LocalPlayer)
            else
                Rayfield:Notify({
                    Title = "Error",
                    Content = "Couldn't find a server.",
                    Duration = 6.5,
                    Image = 124144713366592,
                 })
            end
            wait(5)
            Rayfield:Notify({
                Title = "Server Hop Thất Bại🙁",
                Content = "Thử Sài infinite yield",
                Duration = 6.5,
                Image = 124144713366592,
             })
        end
    end,
})

local Silent = false

Section = Global:CreateSection("Cày Tiền - Người mạnh nhất sever")
local AutoFarm1 = Global:CreateToggle({
    Name = "Auto Farm",
    CurrentValue = false,
    Flag = "",
    Callback = function(Value)
        getgenv().AF = Value
        local isFarming = false

        local function startAutoFarm()
            if Value == false then return end

            local character = player.Character or player.CharacterAdded:Wait()
            local humanoidRootPart = character:WaitForChild("HumanoidRootPart")

            local newPart = Instance.new("Part")
            newPart.Size = Vector3.new(5, 1, 5)
            newPart.Transparency = 1
            newPart.CanCollide = true
            newPart.Anchored = true
            newPart.Parent = workspace

            local decal = Instance.new("Decal")
            decal.Texture = "rbxassetid://139953968294114"
            decal.Face = Enum.NormalId.Top 
            decal.Parent = newPart

            local function TPAF(iteration)
            if not Silent then
                if Value == false then return end
                if iteration == 5 then
                    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart"), workspace.BoatStages.NormalStages.TheEnd.GoldenChest.Trigger, 0)
                    task.delay(0.8, function()
                        workspace.ClaimRiverResultsGold:FireServer()
                    end)

                    humanoidRootPart.CFrame = CFrame.new(-51, 65, 984 + (iteration - 1) * 770)
                else
                    if iteration == 1 then
                        humanoidRootPart.CFrame = CFrame.new(160.16104125976562, 29.595888137817383, 973.813720703125)
                    else
                    humanoidRootPart.CFrame = CFrame.new(-51, 65, 984 + (iteration - 1) * 770)
                    end
                end
                newPart.Position = humanoidRootPart.Position - Vector3.new(0, 2, 0)

                wait(2.3) -- if lower, it can't work every time
                if iteration == 1 then
                    wait(2.3)
                end
                if iteration == 4 then
                else
                    workspace.ClaimRiverResultsGold:FireServer()
                end
            else
                if Value == false then return end
                if iteration == 1 then
                    humanoidRootPart.CFrame = CFrame.new(160.16104125976562, 29.595888137817383, 973.813720703125)
                elseif iteration == 5 then
                    firetouchinterest(game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart"), workspace.BoatStages.NormalStages.TheEnd.GoldenChest.Trigger, 0)
                    task.delay(0.8, function()
                        workspace.ClaimRiverResultsGold:FireServer()
                    end)
                    
                    humanoidRootPart.CFrame = CFrame.new(70.02417755126953, 138.9026336669922, 1371.6341552734375 + (iteration - 2) * 770)
                else
                    humanoidRootPart.CFrame = CFrame.new(70.02417755126953, 138.9026336669922, 1371.6341552734375 + (iteration - 2) * 770)
                end
                newPart.Position = humanoidRootPart.Position - Vector3.new(0, 2, 0)

                wait(2.3) -- if lower, it can't work every time
                if iteration == 1 then
                    wait(2.3)

                end
                if iteration == 4 then
                else
                    workspace.ClaimRiverResultsGold:FireServer()
                end
            end
            end

            for i = 1, 10 do
                if not Value then
                    break
                end
                TPAF(i)
            end

            newPart:Destroy()
        end

                local function onCharacterRespawned()
                    if getgenv().AF == true then
                        if FcMaster == false then return end
                    local character = player.Character or player.CharacterAdded:Wait()
                    character:WaitForChild("HumanoidRootPart")
                       -- wait(2)
                    startAutoFarm()
                    end
                end

        if Value then
            Rayfield:Notify({
                Title = "Auto Farm - Enabled",
                Content = "Isolation mode and Anti-afk is recommended",
                Duration = 6.5,
                Image = 124144713366592,
             })
            game.Players.LocalPlayer.Character:BreakJoints()
            wait(1)
            game.Players.LocalPlayer.CharacterAdded:Connect(onCharacterRespawned)
        else
            Rayfield:Notify({
                Title = "Auto Farm - Disabled",
                Content = "Please, wait for the iteration to finish...",
                Duration = 6.5,
                Image = 124144713366592,
             })
            game.Players.LocalPlayer.CharacterAdded:Connect(function() end)
        end
    end,
})

local Toggle = Global:CreateToggle({
    Name = "Make it Silent",
    CurrentValue = false,
    Flag = "Toggle1",
    Callback = function(Value)
        Silent = Value
    end,
 })

local FStats = Global:CreateParagraph({Title = "Điểm Số", Content = "Thời gian đã cày: -".."\n".."GoldBlock Đã Nhận: -".."\n".."Gold Đã Nhận: -".."\n".."\n".."Gold 1 Giờ: -"})

local clockTime = 0
local running = false
local totalGoldGained = 0
local Ftime = 0 
local totalGoldBlock = 0
local GoldPerHour = 0
local lastGoldValue = game:GetService("Players").LocalPlayer.Data.Gold.Value
local IGBLOCK = game:GetService("Players").LocalPlayer.Data.GoldBlock.Value

local function formatTime(seconds)
    local hours = math.floor(seconds / 3600)
    local minutes = math.floor((seconds % 3600) / 60)
    local sec = seconds % 60
    return hours .. " hours " .. minutes .. " minutes " .. sec .. " seconds"
end

local function startClock()
    if running then return end
    running = true

    while running do
        if getgenv().AF then
            clockTime = clockTime + 1
        else
            running = false
        end
        task.wait(1) 
    end
end

game:GetService("RunService").Stepped:Connect(function()
    if getgenv().AF and not running then
        wait(5)
        startClock()
    end
end)

function initclock()
while true do
    local FinalGold = game:GetService("Players").LocalPlayer.Data.Gold.Value
    Ftime = formatTime(clockTime)
    local GoldGained = FinalGold - lastGoldValue
    totalGoldGained = totalGoldGained + GoldGained
    local FGBLOCK = game:GetService("Players").LocalPlayer.Data.GoldBlock.Value
    totalGoldBlock = FGBLOCK - IGBLOCK

    GoldPerHour = (totalGoldGained / clockTime) * 3600
    

    FStats:Set({
        Title = "Điểm Số",
        Content = "Thời gian đã trôi qua:   " .. Ftime .. "\n" ..
                  "GoldBlock Đã Nhận: " .. totalGoldBlock .. "\n" ..
                  "Gold Đã Nhận: " .. totalGoldGained .. "\n" ..
                  "Gold 1 Giờ: " .. math.floor(GoldPerHour),
    
