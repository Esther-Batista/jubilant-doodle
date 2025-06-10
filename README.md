-- Script em um LocalScript (por exemplo, dentro de StarterPlayerScripts)

local Players = game:GetService("Players")
local player = Players.LocalPlayer

-- Função de compra simulada
local function comprar(itemPreco)
    -- Espera os dados do jogador carregarem
    local leaderstats = player:WaitForChild("leaderstats")
    local dinheiro = leaderstats:WaitForChild("Money")

    -- Simula a "compra" ganhando dinheiro em vez de perder
    dinheiro.Value = dinheiro.Value + itemPreco
    print("Você comprou o item e ganhou $" .. itemPreco .. "!")
end

-- Exemplo de uso:
comprar(100) -- Simula uma compra de item de 100, mas o jogador ganha 100 ao invés de perder


