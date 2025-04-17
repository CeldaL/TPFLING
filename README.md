-- Auto Super Heavy Rapid Punch con más golpes
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local player = game.Players.LocalPlayer

-- Función que ejecuta los golpes automáticamente
local function autoSuperHeavyRapidPunch()
    while true do
        --   (puedes ajustar este número)
        for i = 1, 45 do
            ReplicatedStorage.Events.Punch:FireServer(0.000001, 0.00001, 1) -- Golpe rápido
            wait(0.000001) -- Intervalo entre golpes (puedes ajustarlo para más rapidez)
        end

        -- Espera 11 segundos antes de repetir
        wait(11)
    end
end


task.spawn(autoSuperHeavyRapidPunch)
