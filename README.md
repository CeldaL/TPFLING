-- Auto Super Heavy Rapid Punch con más golpes
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local player = game.Players.LocalPlayer

-- Función que ejecuta los golpes automáticamente
local function autoSuperHeavyRapidPunch()
    while true do
        --  1000 golpes automáticos (puedes ajustar este número)
        for i = 1, 60 do
            ReplicatedStorage.Events.Punch:FireServer(0.00001, 0.0001, 1) -- Golpe rápido
            wait(0.01) -- Intervalo entre golpes (puedes ajustarlo para más rapidez)
        end

        -- Espera 11 segundos antes de repetir
        wait(10)
    end
end


task.spawn(autoSuperHeavyRapidPunch)
