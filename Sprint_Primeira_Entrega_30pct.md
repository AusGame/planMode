# 🎮 Sprints — Primeira Entrega (30%)
## AusTV: Henesys — O Despertar dos Wisps

> **Disciplina:** Desenvolvimento de Games
> **Autores:** Murillo Weiss · Herick Eduardo Vavassori
> **Referência GDD:** GDD_AusTV_Henesys_v3.txt
> **Meta da entrega:** implementar 30% do jogo planejado, cobrindo todos os critérios de avaliação obrigatórios

---

## 🗂️ Mapeamento dos Critérios de Avaliação

### Pontos Fixos (6 pontos)

| Critério | Sprint | Status |
|---|---|---|
| Apresentação do jogo (5–10 min) | Sprint 4 | 🔲 Pendente |
| GitHub (repositório organizado) | Sprint 1 | 🔲 Pendente |
| Menu Principal | Sprint 1 | 🔲 Pendente |
| Tela de Loading / Splash Screen | Sprint 1 | 🔲 Pendente |
| Tela de Fim de Jogo | Sprint 1 | 🔲 Pendente |
| Ajuste de volume (dentro do jogo) | Sprint 1 | 🔲 Pendente |

### Mecânicas Implementadas nos 30%

| Mecânica | Sprint | Justificativa no GDD |
|---|---|---|
| **HUD** | Sprint 2 | Corações de vida, Bits, hotbar de 4 slots, cronômetro |
| **Combate** | Sprint 3 | Ataque de espada (2 HP), dano recebido, knockback |
| **Música (Trilha Sonora)** | Sprint 3 | BGM Hub Central + Zona Caipira em chiptune |
| **Efeitos Visuais/Sonoros** | Sprint 3 | SFX de pulo, ataque, dano, coleta de itens |
| **Score de Jogador (Bits)** | Sprint 3 | Bits dropados por inimigos, contador no HUD |
| **Coleta de Itens** | Sprint 3 | Essências e Bits coletados ao contato |
| **Botão de Pause** | Sprint 1 | Menu de pause com "Continuar" e "Menu Principal" |
| **Botão de Recomeçar** | Sprint 1 | Presente na tela de Game Over ("Reconectar") |
| **Paralax** | Sprint 2 | Backgrounds em múltiplas camadas por zona |
| **Missões Primárias** | Sprint 3 | Diálogo inicial com Power + missão de entrar na Zona 1 |

---

## 🗺️ Escopo dos 30% — O Que Estará Jogável

Ao final desta entrega, o jogador poderá:

1. Ver a **Splash Screen** com a logo do AusTV animada
2. Navegar pelo **Menu Principal** completo (Novo Jogo, Configurações com volume, Créditos)
3. Controlar **Rael** no **Hub Central** com movimento, pulo e sprint
4. Conversar com o NPC **Power** e receber a missão primária
5. Entrar na **Zona 1 — Terras Caipiras** (mapa externo, 2 das 4 seções planejadas)
6. Combater **Wisps Comuns** corrompidos e coletar **Bits** e **Essências Comuns**
7. Ver o **HUD completo** funcionando (vida, Bits, hotbar, Wisp slot)
8. Receber **Game Over** ao zerar a vida e escolher recomeçar
9. Pausar o jogo a qualquer momento
10. Ouvir a **trilha sonora** do Hub e da Zona Caipira + efeitos sonoros

---

## 📅 Sprint 1 — Base do Projeto e Telas Obrigatórias

**Duração:** Semana 1
**Objetivo:** entregar toda a infraestrutura e as telas exigidas pelos critérios de avaliação antes de qualquer gameplay.

### Tarefas

#### 1.1 Setup e GitHub
- [ ] Criar repositório no GitHub com nome `AusTV-Henesys`
- [ ] Configurar `.gitignore` para a engine escolhida
- [ ] Definir estrutura de pastas: `Assets/`, `Scenes/`, `Scripts/`, `Audio/`, `Art/`
- [ ] Criar `README.md` com: título, autores, descrição do jogo, instruções de build e screenshot
- [ ] Configurar branch `main` (build estável) e `dev` (desenvolvimento)
- [ ] Primeiro commit com cena vazia funcional

#### 1.2 Splash Screen / Tela de Loading
- [ ] Cena de splash screen com logo do AusTV em pixel art
- [ ] Animação de Wisp Lendário voando ao redor do título (spritesheet 6 frames)
- [ ] Barra de loading simulada (ou real, conforme tamanho dos assets)
- [ ] Transição automática para o Menu Principal após 3–5 segundos
- [ ] SFX: efeito de "boot" de servidor ao iniciar

#### 1.3 Menu Principal
- [ ] Fundo: mapa de Henesys em pixel art com as 5 zonas visíveis (arte estática inicial)
- [ ] Logo animada com Wisp
- [ ] Botões funcionais:
  - "Novo Servidor" → inicia nova partida
  - "Continuar" → carrega save (state básico, pode ser stub)
  - "Configurações" → abre painel de configurações (ver 1.5)
  - "Créditos" → tela com nomes da equipe
  - "Conectar ao AusTV" → abre link do servidor (placeholder por ora)
- [ ] Música de menu: tema tranquilo do Hub Central

#### 1.4 Tela de Game Over
- [ ] Animação: pixels da tela se dissolvendo (efeito de kick de servidor)
- [ ] Texto "VOCÊ FOI DESCONECTADO" em vermelho pixelado
- [ ] Exibir motivo da morte (ex: "Morte em combate")
- [ ] Botões:
  - "Reconectar" → volta ao último checkpoint (inicialmente: início da Zona 1)
  - "Menu Principal" → volta ao menu
- [ ] SFX: 4 notas descendentes + silêncio (conforme GDD)

#### 1.5 Ajuste de Volume (in-game)
- [ ] Painel de configurações acessível pelo Menu Principal **e** pelo Menu de Pause
- [ ] Controles separados:
  - Slider de Volume Geral (Master)
  - Slider de Música (BGM)
  - Slider de Efeitos Sonoros (SFX)
- [ ] Persistência da configuração entre sessões (PlayerPrefs ou equivalente)
- [ ] Aplicação em tempo real ao mover os sliders

#### 1.6 Menu de Pause
- [ ] Tecla ESC pausa o jogo e abre o menu
- [ ] Fundo escurecido sobre o jogo
- [ ] Botões:
  - "Continuar" → retoma o jogo
  - "Configurações" → abre painel de volume (1.5)
  - "Voltar ao Menu" → retorna ao Menu Principal
- [ ] O tempo do jogo **congela** durante o pause (inimigos param)

#### 1.7 Botão de Recomeçar
- [ ] Disponível na tela de Game Over ("Reconectar")
- [ ] Reseta: vida do Rael, posição no checkpoint, inimigos da área
- [ ] Mantém: Bits coletados (decisão de design: não punir demais no 30%)

**Entregáveis do Sprint 1:**
- Repositório GitHub com commits organizados
- Todas as 4 telas obrigatórias funcionando
- Volume configurável funcionando
- Build rodando sem erros

---

## 📅 Sprint 2 — Personagem, Mundo e HUD

**Duração:** Semana 2
**Objetivo:** Rael jogável no Hub Central com HUD completo e paralax funcionando.

### Tarefas

#### 2.1 Sprite e Animações do Rael
- [ ] Sprite sheet de Rael em pixel art 16x16 (ou 32x32 para legibilidade)
- [ ] Animações:
  - Idle (4 frames)
  - Correndo (6 frames)
  - Pulando — subindo (2 frames)
  - Pulando — descendo (2 frames)
  - Atacando espada (4 frames)
  - Tomando dano (flash branco, 2 frames)
  - Morto (2 frames + fade)
- [ ] Flip horizontal automático conforme direção do movimento

#### 2.2 Controles do Rael
- [ ] **A / D** → mover esquerda / direita (velocidade: 2,5 blocos/s)
- [ ] **W / Espaço** → pulo (física com gravidade)
- [ ] **Ctrl** → Sprint (velocidade: 4,5 blocos/s, sem cooldown nesta entrega)
- [ ] **S** → agachar / passar por plataformas one-way
- [ ] **Botão Esquerdo** → ataque espada (2 HP, sem cooldown nesta entrega)
- [ ] **Botão Direito sobre NPC** → iniciar diálogo
- [ ] SFX: "blip" agudo no pulo, "slash" no ataque, "whoosh" suave no sprint

#### 2.3 Física e Colisão
- [ ] Gravidade padrão com coyote time (0.1s após sair de plataforma)
- [ ] Colisão com chão, paredes e teto
- [ ] Plataformas one-way (S para descer)
- [ ] Limites da tela / câmera que segue o personagem com lerp suave

#### 2.4 Hub Central — Layout e Arte
- [ ] Cena "Hub Central — Altar dos Titãs"
- [ ] Arte do Hub: azul médio, cinza pedra, branco — neutro e acolhedor
- [ ] Elementos presentes:
  - NPC Power (sprite estático com balão de diálogo ao pressionar direito)
  - Placa da ShopGUI (funcional em sprint futuro — sprite com "Em breve")
  - Altar dos Titãs ao fundo (arte decorativa)
  - 4 slots de Fragmento (vazios e escuros nesta entrega)
- [ ] Transição de e para a Zona 1 (porta/portal com hitbox)

#### 2.5 HUD Completo
Conforme GDD — todos os elementos visíveis, dados reais:

- **Canto superior esquerdo:** corações de vida estilo Minecraft (6 corações = 12 HP)
- **Canto superior direito:** contador de Bits + ícones dos 4 Fragmentos (todos vazios)
- **Canto inferior centro:** hotbar com 4 slots (apenas Espada ativa nesta entrega; slots 2/3/4 com ícone de "bloqueado")
- **Canto inferior direito:** slot do Wisp equipado (vazio, desbloqueável futuramente)

#### 2.6 Paralax Backgrounds
- [ ] Sistema de paralax com pelo menos 3 camadas por área:
  - Camada traseira (céu / fundo distante) → velocidade 20% do scroll da câmera
  - Camada média (árvores / edifícios distantes) → velocidade 50%
  - Camada frontal (elementos próximos) → velocidade 80%
- [ ] Arte de paralax para Hub Central (neutro, nuvens pixel art)
- [ ] Arte de paralax para Zona Caipira (campos verdes, horizonte rural)

**Entregáveis do Sprint 2:**
- Rael se movendo, pulando e atacando no Hub
- HUD completo visível e funcional
- Paralax funcionando em pelo menos uma área
- Transição Hub → Zona 1 funcionando

---

## 📅 Sprint 3 — Zona Caipira, Inimigos e Mecânicas de Jogo

**Duração:** Semana 3
**Objetivo:** conteúdo jogável com inimigos, itens, score, diálogo e trilha sonora.

### Tarefas

#### 3.1 Zona 1 — Terras Caipiras (Mapa Externo, 2 Seções)

Seção A — Campo Aberto:
- [ ] Layout horizontal com 2 plataformas elevadas e solo irregular
- [ ] Arte temática: verde saturado, marrom, barris, mesas de madeira
- [ ] Blocos de vegetação destrutíveis (não interativos nesta entrega — apenas visuais)
- [ ] Armadilhas de raiz no chão (área de slow: -0,5 blocos/s por 1,5s ao pisar)
- [ ] Posicionamento de 4–6 Wisps Comuns patrulhando

Seção B — Entrada da Fazenda:
- [ ] Layout com desnível e plataformas one-way (troncos de árvore)
- [ ] Wisps Comuns e Mobs de Fazenda (Boi Mutado — sprite simples, lento)
- [ ] Checkpoint visual: fogueira/tocha que acende ao ser atingida

#### 3.2 Inimigo: Wisp Comum (Corrompido)
- [ ] Sprite animado: bola de luz cinza com corrupção (4–6 frames)
- [ ] IA: patrulha em círculo de 6 blocos; ao ver Rael em 4 blocos, persegue
- [ ] Dano: 1 HP por contato (knockback leve no Rael)
- [ ] Vida: 4 HP (morrer em 2 ataques de espada)
- [ ] Drop ao morrer: Bit (moeda) com 80% de chance + Essência Comum com 30%
- [ ] SFX: som ao tomar dano + som ao morrer (puff de pixel art)

#### 3.3 Sistema de Combate
- [ ] Hitbox de ataque da espada (arco à frente de Rael, 1 bloco de alcance)
- [ ] Dano aplicado: 2 HP por acerto
- [ ] Flash branco no inimigo ao receber dano
- [ ] Invencibilidade de 0,5s no Rael após tomar dano (iframes)
- [ ] Flash vermelho na tela ao tomar dano
- [ ] SFX: "slash" ao atacar + "grunt" ao receber dano

#### 3.4 Coleta de Itens
- [ ] **Bits:** objeto no chão com ícone de moeda dourada; coletado ao contato
- [ ] **Essência Comum:** orb de luz cinza; coletada ao contato
- [ ] Animação de pop-up "+1 Bit" / "+1 Essência" ao coletar
- [ ] Contador de Bits no HUD atualiza em tempo real
- [ ] SFX: "ding" agudo para Bit, "shimmer" para Essência (conforme GDD)

#### 3.5 Score de Jogador — Contador de Bits
- [ ] Bits acumulados exibidos no HUD (canto inferior direito)
- [ ] Bits persistem durante a sessão
- [ ] Tela de Game Over exibe total de Bits coletados antes de morrer

#### 3.6 NPC Power — Diálogo e Missão Primária
- [ ] Sistema de diálogo simples: caixa de texto com portrait de Power
- [ ] Sequência de falas de apresentação (3–5 linhas conforme narrativa do GDD):
  - "Bem-vindo ao AusTV. Eu sou Power."
  - "Henesys está em perigo. O Titã Corrompido emergiu."
  - "Você é um novato — isso é uma vantagem. Os clãs não têm motivo para te odiar."
  - "Vá até as Terras Caipiras ao sul. Prove seu valor para Blocão."
- [ ] Missão primária registrada: "Entrar na Zona das Terras Caipiras"
- [ ] Marcador visual na HUD: ícone de missão ativa (simples)

#### 3.7 Trilha Sonora
- [ ] **Hub Central:** tema tranquilo em chiptune (loop de 60–90s)
- [ ] **Zona Caipira:** viola caipira + percussão em chiptune (loop de 60s)
- [ ] Transição com fade de 1s ao mudar de área
- [ ] Integrado ao sistema de volume (slider de BGM do Sprint 1)

#### 3.8 Efeitos Sonoros (SFX)
- [ ] Pulo: "blip" agudo
- [ ] Sprint: "whoosh" suave
- [ ] Ataque espada: "slash" metálico
- [ ] Dano recebido: "grunt" + flash
- [ ] Coleta de Bit: "ding"
- [ ] Coleta de Essência: "shimmer"
- [ ] Wisp inimigo morrendo: "puff" pixelado
- [ ] Game Over: 4 notas descendentes
- [ ] Todos integrados ao slider de SFX do Sprint 1

**Entregáveis do Sprint 3:**
- Zona Caipira (2 seções) jogável com inimigos vivos
- Combate funcionando com feedback visual e sonoro
- Coleta de Bits e Essências operando
- Diálogo com Power funcional
- Trilha sonora em loop nas duas áreas

---

## 📅 Sprint 4 — Polimento, Testes e Apresentação

**Duração:** Semana 4
**Objetivo:** qualidade de entrega, ausência de bugs críticos e preparação da apresentação.

### Tarefas

#### 4.1 Tela de Vitória Parcial (Zona 1)
- [ ] Ao entrar na área de Blocão (portal ao fim da Seção B), exibir tela de "Área Completada"
- [ ] Exibir: Bits coletados, inimigos derrotados, mortes
- [ ] Botão "Voltar ao Hub" → retorna ao Hub Central
- [ ] Nota: boss e Fragmento serão implementados na próxima entrega (50%)

#### 4.2 Checkpoint System
- [ ] Salvar posição ao ativar a fogueira (Seção B)
- [ ] Ao usar "Reconectar" no Game Over, Rael aparece na fogueira ativada
- [ ] Vida restaurada para máximo ao reconectar

#### 4.3 Efeitos Visuais de Polimento
- [ ] Partículas de poeira ao pousar de um pulo
- [ ] Brilho pulsante nas Essências no chão (para chamar atenção)
- [ ] Efeito de "fade in" ao entrar em nova área
- [ ] Tremor de câmera (0,2s) ao tomar dano pesado (>2 HP de uma vez)

#### 4.4 Testes e Bug Fixes
- [ ] Testar fluxo completo: Splash → Menu → Hub → Zona 1 → Game Over → Reconectar
- [ ] Testar pause/resume em todas as cenas
- [ ] Verificar sliders de volume em todas as cenas
- [ ] Verificar que Bits e Essências são coletados corretamente
- [ ] Verificar hitboxes de ataque e de dano do inimigo
- [ ] Testar checkpoint e Game Over
- [ ] Revisar: nenhum objeto de inimigo morto permanece com collider ativo

#### 4.5 GitHub — Organização Final
- [ ] README completo com:
  - Screenshot do jogo rodando
  - GIF de gameplay (15–30s)
  - Instruções de como rodar o build
  - Controles listados
  - Créditos de assets e autores
- [ ] Tag de versão: `v0.3-primeira-entrega`
- [ ] Build exportado disponível (pasta `Builds/` ou Release no GitHub)

#### 4.6 Preparação da Apresentação (5–10 min)
Roteiro sugerido:

1. **Introdução (1 min):** apresentar o jogo, os autores e a inspiração no servidor AusTV
2. **Demonstração ao vivo (4–5 min):**
   - Mostrar Splash Screen e Menu
   - Mostrar ajuste de volume
   - Jogar Hub Central + diálogo com Power
   - Jogar Zona Caipira: matar inimigos, coletar Bits
   - Demonstrar Game Over e Reconectar
   - Demonstrar Pause
3. **Mecânicas implementadas (2 min):** listar as 10 mecânicas entregues neste sprint
4. **Próximos passos (1 min):** o que vem nos 70% restantes

- [ ] Criar slides de apoio (mínimo: capa, visão geral do GDD, mecânicas entregues, roadmap)
- [ ] Ensaiar a demo com build estável (não usar versão em desenvolvimento)

**Entregáveis do Sprint 4:**
- Build estável e exportado
- GitHub com README, build e tag de versão
- Apresentação preparada e ensaiada
- Zero bugs críticos (crash, softlock, volume quebrado)

---

## 📊 Resumo Geral dos 30%

### O Que Está Sendo Entregue

| Área | Status Entrega |
|---|---|
| Hub Central | ✅ Completo (arte + NPC Power + diálogo) |
| Zona Caipira — Seções A e B | ✅ Completo (das 4 seções planejadas) |
| Dungeon Ruína | ❌ Próxima entrega |
| Zonas 2, 3 e 4 | ❌ Próximas entregas |
| Arena Final + Boss | ❌ Entrega final |
| Battle Pass | ❌ Próxima entrega |
| Leilão Sombrio | ❌ Próxima entrega |
| mcMMO completo | ❌ Próxima entrega |
| Besta (crossbow) | ❌ Próxima entrega |

### Mecânicas por Critério

| # | Mecânica | Sprint | Entregue |
|---|---|---|---|
| 1 | HUD | 2 | ✅ |
| 2 | Combate | 3 | ✅ |
| 3 | Música (Trilha Sonora) | 3 | ✅ |
| 4 | Efeitos Visuais/Sonoros | 3 | ✅ |
| 5 | Score de Jogador (Bits) | 3 | ✅ |
| 6 | Coleta de Itens | 3 | ✅ |
| 7 | Botão de Pause | 1 | ✅ |
| 8 | Botão de Recomeçar | 1 | ✅ |
| 9 | Paralax | 2 | ✅ |
| 10 | Missões Primárias | 3 | ✅ |

### Critérios Fixos

| Critério | Entregue |
|---|---|
| Apresentação (5–10 min) | ✅ Sprint 4 |
| GitHub | ✅ Sprint 1 |
| Menu Principal | ✅ Sprint 1 |
| Splash Screen / Loading | ✅ Sprint 1 |
| Tela de Fim de Jogo | ✅ Sprint 1 |
| Ajuste de volume | ✅ Sprint 1 |

---

## 🗓️ Linha do Tempo

```
Semana 1     Semana 2     Semana 3     Semana 4
┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐
│ Sprint 1 │ │ Sprint 2 │ │ Sprint 3 │ │ Sprint 4 │
│          │ │          │ │          │ │          │
│ GitHub   │ │ Rael     │ │ Caipira  │ │ Polimento│
│ Telas    │ │ Hub      │ │ Inimigos │ │ Testes   │
│ Volume   │ │ HUD      │ │ Combate  │ │ GitHub   │
│ Pause    │ │ Paralax  │ │ Diálogo  │ │ Apresen- │
│ GameOver │ │          │ │ Áudio    │ │ tação    │
└──────────┘ └──────────┘ └──────────┘ └──────────┘
```

---

*Documento gerado com base no GDD_AusTV_Henesys_v3.txt*
*Versão: 1.0 — Primeira Entrega (30%)*
