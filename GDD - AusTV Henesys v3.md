---
tags: [faculdade, games, gdd, austv, henesys, rpg, plataforma-2d, besta, mcmmo]
data_criacao: 2026-03-27
disciplina: Desenvolvimento de Games
autores: [Murillo Weiss, Herick Eduardo Vavassori]
versao: "3.0"
titulo: "AusTV: Henesys — O Despertar dos Wisps"
genero: Plataforma 2D de Ação e RPG por Zonas
status: versao_final
---

# GDD v3 — AusTV: Henesys — O Despertar dos Wisps

> **Resumo:** Versão final do jogo de plataforma 2D de ação e RPG onde Rael, novato sem clã, entra no servidor AusTV e precisa reunir as 4 facções rivais de Henesys para encerrar a ameaça do Titã Corrompido — usando mecânicas, itens, eventos e personagens baseados no servidor real.

→ Parte do projeto [[Desenvolvimento de Games - Index|Desenvolvimento de Games]]
→ Versão anterior: [[GDD - AusTV Henesys v2]]

---

## Novidades da v3 em relação à v2

- **Líderes de clã com nomes reais:** Blocão (Imperial/Caipira), Shinigami (Moon/Espacial), Marcus (Royals/Pizzaria), Ozielux (Kuromi/Halloween)
- **Power** substituiu Blocko como mentor — o fundador real do AusTV, ex-líder do maior clã, que abdicou do poder pela paz
- **Besta (crossbow)** como arma de longo alcance principal, com mecânica idêntica ao Minecraft (recarregar → mirar → disparar)
- **Controles inspirados no Minecraft:** WASD, mouse esquerdo/direito, Shift=Sneak, Ctrl=Sprint, hotbar 1-4
- **Narrativa emocional aprofundada:** o Titã é a manifestação do antigo clã de Power, dissolvido sem despedida — a batalha final é um ritual de encerramento, não apenas combate
- **Mecânica de Sneak** (Shift) — reduz hitbox, move devagar, não acorda inimigos dormentes em 4 blocos
- **Skins de arma com nomes reais do resource pack AusTV** (Besta das Sombras, Devaneio, Tetsubo, etc.)

---

## Parte 1 — Jornada do Herói

### Mapa de Henesys
Servidor governado por 4 clãs, cada um controlando uma região:

| Clã | Líder | Zona | Estilo |
|---|---|---|---|
| **Clã Imperial** | Blocão | Sul — Terras Caipiras | Rural, desconfiado, respeita ação |
| **Clã Moon** | Shinigami | Norte — Zona Espacial | Calculista, frio, valoriza inteligência |
| **Clã Royals** | Marcus | Leste — Bairro da Pizzaria | Carismático, popular, prova de habilidade social |
| **Clã Kuromi** | Ozielux | Oeste — Distrito de Halloween | Enigmática, teatral, admira quem não tem medo |

Centro: **Altar dos Titãs** — administrado por **Power**, fundador neutro do AusTV.

### Protagonista — Rael
Novato sem bandeira de clã. Por isso, transita livremente pelos 4 territórios em guerra. Não carrega as brigas antigas — essa é sua maior força.

### Mentor — Power
Fundador do AusTV. Ex-líder do clã mais poderoso de Henesys, dissolvido por ele mesmo quando percebeu que o poder de um único clã estava sufocando o servidor. Vive como NPC neutro no Altar dos Titãs, respeitado por todos. Frase-chave: *"Eu já tentei reunir esses quatro. Não funcionou vindo de mim. Talvez funcione vindo de alguém que eles não têm motivo para odiar."*

### Chamado e Travessia
Titã Corrompido emerge + corrupção transforma Wisps em criaturas agressivas. Power convoca Rael. Primeira dungeon: **Dungeon Ruína** — câmaras subterrâneas de pedra ancestral, relíquias de um clã que existiu antes dos quatro atuais. Ao sair vitorioso, Blocão reconhece Rael como digno.

### Testes por Zona e Condições dos Líderes

| Zona | Dungeon | Condição do Líder |
|---|---|---|
| **Caipira / Blocão** | Dungeon Ruína — pedra, fósseis, puzzles de mineração | Completar sem usar kit médico nenhuma vez |
| **Espacial / Shinigami** | Dungeon Tormenta — torre elétrica, Robôs Corrompidos | Resolver puzzles de ordem (não força bruta) |
| **Pizzaria / Marcus** | Dungeon Carmesim — cristal carmesim, ilusões/caminhos falsos | Vencer BuildBattle local primeiro |
| **Halloween / Ozielux** | Dungeon Assombrada — mansão 3 andares, Fantasmas, visibilidade reduzida | Completar sem correr nenhuma vez |

### Aliados e Habilidades

| Aliado | Habilidade Ativa | Cooldown | Aura Passiva |
|---|---|---|---|
| **Blocão** | Escudo de Terra — bloqueia 4 HP do próximo hit | 20s | Resistência a knockback |
| **Shinigami** | Análise de Alvo — destaca ponto fraco por 8s | 15s | Dano de Besta +1 |
| **Marcus** | Grito de Clã — Wisps próximos atacam mesmo alvo | 18s | +0.5 velocidade |
| **Ozielux** | Véu de Kuromi — invisível por 4s, inimigos param de perseguir | 25s | Regenera 1 HP / 20s fora de combate |

### Grande Provação — Revelação do Titã
Ao reunir os 4 Fragmentos, Power toca os fragmentos e o Titã Corrompido invade o Altar. Power é incapacitado. Revelação: o Titã é a **manifestação do antigo clã de Power**, corrompida pela dissolução forçada. Energia de um coletivo desfeito sem encerramento, sem despedida. Power murmura: *"Não se pode dissolver o que as pessoas constroem juntas. Só transformar."*

### Recompensa e Retorno
Os 4 líderes chegam ao Altar (convocados por Power). Cada um "honra" o antigo clã: Blocão com força, Shinigami com respeito, Marcus com alegria, Ozielux com memória. O Titã se dissolve em luz — não em derrota, mas em **encerramento**. Rael recebe o **Wisp Único** e o título **"Embaixador de Henesys"**. Henesys cria o **Protocolo Rael**: qualquer jogador neutro pode convocar os líderes ao Altar em caso de ameaça.

---

## Parte 2 — Game Design Document

### High Concept
| Campo | Valor |
|---|---|
| **Título** | AusTV: Henesys — O Despertar dos Wisps |
| **Gênero** | Plataforma 2D de Ação e RPG por Zonas |
| **Diferencial** | Controles inspirados no Minecraft; Besta como arma principal |

### Core Loop
1. Spawna no Hub (Altar dos Titãs) com mcMMO zerado
2. Explora a zona — coleta recursos, derrota Wisps corrompidos, sobe mcMMO
3. Entra na dungeon temática — usa Besta e Espada, resolve puzzles, derrota Wisp Lendário
4. Coleta o Fragmento de Essência
5. Retorna ao Hub — entrega fragmento a Power, sobe Battle Pass, compra na Shop
6. Avança para próxima zona com mcMMO recém-desbloqueado
7. Enfrenta o Titã de Obsidiana com os 4 aliados (ritual de encerramento)

### Controles (Inspirados no Minecraft)

| Tecla | Ação |
|---|---|
| A / D | Mover esquerda / direita |
| W / Espaço | Pulo |
| W (2x no ar) | Pulo Duplo (mcMMO Acrobacia nível 20) |
| S | Agachar / descer plataformas |
| Ctrl | Sprint por 2s (CD 5s ao parar) |
| **Mouse Esquerdo** | Ataque corpo-a-corpo (Espada / Picareta) |
| **Mouse Direito** | Usar/Interagir — Besta em inimigos / Interagir com NPC / Picareta em blocos |
| E | Inventário / Battle Pass |
| 1 / 2 / 3 / 4 | Hotbar: Espada / Besta / Consumível / Ferramenta |
| Q | Habilidade do Wisp equipado (CD 30s) |
| F | Trocar mão principal (Espada ↔ Besta) |
| **Shift** | Sneak — reduz hitbox, move devagar, não acorda inimigos em 4 blocos |
| **R** | Recarregar Besta (1.5s — interrompido por dano) |
| Enter | Falar com NPC / abrir loja |

### Mecânica da Besta (Crossbow) — Destaque v3

A Besta segue exatamente o comportamento do Minecraft:

1. **Recarregar** (R) — animação de 1.5s. Interrompida por dano recebido.
2. **Mirar** (manter Mouse Direito) — linha de trajetória pontilhada, alcance 15 blocos.
3. **Disparar** (soltar Mouse Direito) — 3 HP de dano, perfura inimigos alinhados (pierce).

**Skins da Besta** (baseadas no resource pack real do AusTV):
Devaneio, Besta das Sombras, Lança Confetes, Dardo do Amor, Yumi Sagrado, Besta da Colheita, Besta dos Ovos, Pterodactyl, Besta Tempestuosa.

**Skins de Espada/Clava:**
Destruidor, Clava do Além, Bloco Carnavalesco, Clava Glacial, Tetsubo, Ankylosaurus, Clava Fóssil.

### Protagonista — Rael

| Atributo | Valor |
|---|---|
| Vida inicial | 6 corações (12 HP) |
| Vida máxima | 12 corações (24 HP) |
| Velocidade caminhando | 2.5 blocos/s |
| Velocidade sprint | 4.5 blocos/s |
| Ataque Espada | 2 HP (sem cooldown) |
| Ataque Besta | 3 HP (recarga 1.5s) |

**Sistema mcMMO:**

| Habilidade | Nível 10 | Nível 20/25 | Nível 35/40/50 |
|---|---|---|---|
| Combate | Crítico passivo 10% | Combo Triple (2+2+5) | Berserker 8s (CD 40s) |
| Mineração | Drop 2x itens | Super Breaker 3x3 (CD 30s) | — |
| Acrobacia | — | Pulo Duplo | Dash 3 blocos 0.5s invenc. (CD 8s) / Rolamento sem queda |
| Herbalismo | +0.5 HP / coleta | Green Terra 5 blocos / 5s (CD 35s) | — |

**Wisps (passivo + ativo Q):**

| Raridade | Passivo | Ativo Q |
|---|---|---|
| Comum | +1 HP / 30s | Revela Wisps no mapa por 10s |
| Incomum | +0.5 blocos/s | Sprint grátis por 5s |
| Raro | 15% bloquear 1 hit/s | Escudo total por 2s |
| Épico | Dano +1 permanente | Próximo ataque 3x dano |
| Lendário | Único por Wisp | Exclusivo por Wisp |
| **Único** | Combina todos os anteriores | Cura 6 HP + dash automático (CD 60s) |

### Inimigos

| Inimigo | HP | Dano | Mecânica Especial |
|---|---|---|---|
| Wisp Comum | 4 HP | 1 HP | Patrulha circular 6 blocos |
| Wisp Incomum | 8 HP | 1 + veneno 0.5/3s | Teleporte (CD 8s) |
| Wisp Raro | 14 HP | 1.5/projétil | Flutuante, rajada de 3 |
| Wisp Épico | 25 HP | 3 HP | Campo de força — só corpo-a-corpo |
| Wisp Lendário (Mini-Boss) | 50 HP | 2/4 HP | 3 fases: voo → suporte → campo+rajada |

### Batalha Final — Titã de Obsidiana (3 Fases)

| Fase | HP | Nome | Mecânica | Solução |
|---|---|---|---|---|
| 1 | 40 HP | **Eco do Imperial** | Blocos caem do teto, raízes prendem 1.5s | Blocão (Escudo de Terra) + Besta na coroa |
| 2 | 35 HP | **Eco da Moon** | 3 cópias holográficas — apenas 1 real (tem sombra) | Shinigami (Análise de Alvo) revela a real |
| 3 | 25 HP | **Eco de Kuromi e Royals** | Arena com 4 plataformas. Alterna invisibilidade + NPCs falsos de aliados | Véu de Kuromi + Grito de Clã. Ao chegar 0 HP: cutscene do ritual |

### Zonas

| Zona | Tema | Paleta | Música | Mechânica Introduzida |
|---|---|---|---|---|
| Hub — Altar dos Titãs | Hub neutro | Azul/Branco/Cinza | Tranquilo, evolui com fragmentos | — |
| Caipira (Sul) | Rural, fazendas | Verde, Marrom, Ocre | Acordeão chiptune | Herbalismo / Green Terra |
| Espacial (Norte) | Sci-fi, hologramas | Azul-neon, Preto | Sintetizador alto BPM | Pulo Duplo |
| Pizzaria (Leste) | Urbano animado | Vermelho, Amarelo | Pop urbano chiptune | BuildBattle, ilusões |
| Halloween (Oeste) | Sombrio, Modo Zumbi | Roxo, Laranja, Preto | Ambiente tenso | Stealth/Sneak |
| Arena Final | Altar corrompido | Paletas mistas + glitch | Épico progressivo 3 camadas | Mecânicas cumulativas |

### Condições de Vitória e Derrota
**Vitória:** Derrotar o Titã com os 4 aliados participando do ritual. Zonas podem ser feitas em qualquer ordem, mas Pizzaria exige mcMMO nível 15 e Halloween exige nível 25.

**Game Over:** Vida zera → "DESCONECTADO" (retornar ao checkpoint). Cronômetro 72h esgota → "HENESYS CAIU" (reiniciar da última zona). O cronômetro pausa em dungeons, no Hub e durante diálogos.

### Itens Principais

| Item | Função | Obtenção |
|---|---|---|
| Essências (Comum/Incomum/Rara/Épica) | Craft na Forja + Leilões | Drop de Wisps |
| Fragmentos de Essência (4) | Progressão principal | Mini-boss de zona |
| Kit Médico | Recupera 4 HP (stack 5) | Drop ou ShopGUI |
| Poção de Mana | Recarrega TODOS os cooldowns | Leilões Sombrios / boss |
| Bits | Moeda (Shop + Leilões) | Drop de inimigos / cristais |
| Itens Gourmet (Tomate, Milho, Alho) | Poções especiais na Forja | Zona Caipira |

**Receitas Gourmet:**
- Tomate + Alho → Poção Anti-Zumbi (resistência Halloween 30s)
- Milho + Alho → Ração de Wisp (aumenta nível do Wisp equipado por 20s)
