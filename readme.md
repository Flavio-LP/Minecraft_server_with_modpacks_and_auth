# ⛏️ Modpack dos Guri

> Modpack multiplayer focado em tecnologia industrial, exploração de dimensões e batalhas épicas contra bosses.

---

## 📋 Informações

| | |
|---|---|
| **Versão do Minecraft** | 1.20.1 |
| **Mod Loader** | Forge |
| **Launcher recomendado** | Prism Launcher |

---

## 🚀 Como Jogar

### 1. Instale o Prism Launcher
Baixe em: [prismlauncher.org](https://prismlauncher.org)

### 2. Importe o Modpack
- Abra o Prism Launcher
- Clique em **Add Instance → Import**
- Selecione o arquivo `.mrpack` disponibilizado no Discord

<!--### 3. Configure o Pre-launch e Post-exit
Vá em **Edit Instance → Settings → Custom Commands** e configure:

**Pre-launch command** (roda antes de abrir o jogo):
```bash
curl -s -X POST https://SEU_IP:3000/api/sessions \
  -H "Content-Type: application/json" \
  -d "{\"username\": \"SEU_NICK\", \"password\": \"SUA_SENHA\"}"
```

**Post-exit command** (roda depois de fechar o jogo):
```bash
curl -s -X DELETE https://SEU_IP:3000/api/sessions \
  -H "Content-Type: application/json" \
  -d "{\"username\": \"SEU_NICK\", \"password\": \"SUA_SENHA\"}"
```

> ⚠️ Substitua `SEU_NICK` e `SUA_SENHA` pelas credenciais que você criou no registro.

### 4. Registre sua Conta (apenas na primeira vez)
```bash
curl -X POST https://SEU_IP:3000/api/players \
  -H "Content-Type: application/json" \
  -d '{"username": "SEU_NICK", "password": "SUA_SENHA"}'
```

### 5. Entre no Servidor
- Clique em **Play** no Prism Launcher
- O sistema de autenticação libera seu acesso automaticamente
- Conecte em: `SEU_IP:25565`

> ⚠️ O nick configurado no Prism Launcher deve ser **idêntico** ao nick cadastrado no registro.

---

-->

## 🧩 Mods Incluídos

### ⚙️ Tecnologia e Automação
| Mod | Descrição |
|---|---|
| **Mekanism** | Sistema tech completo com máquinas, energia e química |
| **Mekanism Generators** | Geradores solar, eólico e fusão nuclear |
| **Mekanism Tools** | Ferramentas e armaduras do Mekanism |
| **Immersive Engineering** | Tecnologia realista com multiblocks e cabos |
| **Industrial Foregoing** | Automação de fazendas e recursos |
| **Create** | Automação com engrenagens e mecânica rotacional |
| **Create: Steam 'n' Rails** | Trens e locomotivas a vapor |

### 🔋 Energia
| Mod | Descrição |
|---|---|
| **Flux Networks** | Redes de energia sem fio compatível com todos os mods |
| **Powah** | Geração de energia simples e progressiva |
| **Extreme Reactors** | Reatores nucleares de grande escala |

### 📦 Armazenamento
| Mod | Descrição |
|---|---|
| **Applied Energistics 2** | Armazenamento digital avançado com autocrafting |
| **AE2 Wireless Terminals** | Acesso ao AE2 de qualquer lugar via terminal sem fio |
| **Iron Chests** | Baús maiores em ferro, ouro, diamante e mais |

### 🚰 Transporte
| Mod | Descrição |
|---|---|
| **Pipez** | Pipes simples para itens, fluidos e energia |
| **XNet** | Rede de transporte avançada e configurável |
| **Thermal Dynamics** | Ducts do Thermal para transporte de recursos |

### 🧪 Processamento
| Mod | Descrição |
|---|---|
| **Thermal Expansion** | Máquinas térmicas para processar recursos |
| **Thermal Foundation** | Minérios e materiais base do Thermal |

### ⛏️ Mineração e Recursos
| Mod | Descrição |
|---|---|
| **Tinkers' Construct** | Ferramentas customizáveis com materiais especiais |
| **Mystical Agriculture** | Cultivar minérios e recursos como plantas |

### 🔄 Chunk Loader
| Mod | Descrição |
|---|---|
| **Chunk Loaders** | Mantém chunks carregados mesmo com o jogador offline |
| **FTB Chunks Compatibility** | Compatibilidade de proteção de chunks |

### 🌍 Dimensões
| Mod | Descrição |
|---|---|
| **The Undergarden** | Mundo subterrâneo obscuro com flora e fauna únicas |

### 👹 Bosses e Combate
| Mod | Descrição |
|---|---|
| **L_Ender's Cataclysm** | Bosses épicos endgame em arenas especiais com múltiplas fases |
| **Stalwart Dungeons** | Dungeons no Nether e End com bosses invocáveis em altares |
| **Dungeon Crawl** | Masmorras roguelike geradas pelo mundo com loot progressivo |
| **Daily Boss x Brutal Bosses** | Bosses diários com recompensas especiais |

### 🗺️ Qualidade de Vida
| Mod | Descrição |
|---|---|
| **JEI (Just Enough Items)** | Visualiza receitas de todos os mods |
| **JourneyMap** | Minimapa completo com waypoints |
| **Jade** | Informações de blocos e máquinas ao passar o mouse |
| **Waystones** | Pontos de teleporte pelo mundo |
| **Inventory Sorter** | Organiza inventário com 1 clique |

### 🔧 Dependências e APIs
> Instaladas automaticamente, não requerem configuração.

| Mod | Usado por |
|---|---|
| **Architectury API** | Base para vários mods multiplataforma |
| **Balm** | Dependência do Waystones |
| **Cloth Config** | Configuração de mods |
| **CoFH Core** | Base do Thermal |
| **Cucumber** | Dependência do Mystical Agriculture |
| **Curios API** | Sistema de slots extras (anéis, amuletos) |
| **Lionfish API** | Dependência de mods de combate |
| **Mantle** | Dependência do Tinkers' Construct |
| **MCJtyLib** | Dependência do XNet e RFTools |
| **RFTools Base** | Base do RFTools |
| **Supermartijn642's Config Lib** | Configuração do Chunk Loaders |
| **Supermartijn642's Core Lib** | Core do Chunk Loaders |
| **Titanium** | Dependência do Industrial Foregoing |
| **ZeroCore** | Dependência do Extreme Reactors |

<!--
## 🛠️ Para Administradores

### Estrutura do Projeto
```
/minecraft/
├── .env
├── docker-compose.yml
├── mods/
├── data/
└── portal/          ← API Ruby de autenticação
```

### Subindo o servidor
```bash
cd /minecraft
docker-compose up -d
docker-compose exec portal rails db:create db:migrate
```

### Adicionando novos mods
```bash
# Na máquina local, dentro da pasta do modpack
packwiz modrinth add nome-do-mod
packwiz refresh
git add .
git commit -m "Adiciona nome-do-mod"
git push

# Na VPS
docker-compose restart minecraft
```

### Gerenciando jogadores
```bash
# Verificar jogadores registrados
docker-compose exec db psql -U postgres minecraft_portal \
  -c "SELECT minecraft_username, whitelisted FROM users;"

# Ver logs do servidor
docker-compose logs -f minecraft

# Ver logs da API
docker-compose logs -f portal
```

---

## ❓ Problemas Comuns

**Não consigo entrar no servidor**
- Verifique se fez o registro da conta
- Confirme que o nick no Prism Launcher é **idêntico** ao cadastrado
- Verifique se o Pre-launch command está configurado corretamente

**O jogo trava ao iniciar**
- Verifique se tem pelo menos **6GB de RAM** alocados no Prism Launcher
- Vá em **Edit Instance → Settings → Java** e aumente o valor de memória

**Mod não está funcionando**
- Confirme que importou o modpack corretamente
- Tente reinstalar a instância no Prism Launcher

---
-->