<div align="center">

<h1>🎮 ObjtEdit — Object Editor for SA-MP.</h1>

<p>
  <strong>Editor de objetos acoplados ao corpo do personagem para servidores SA-MP.</strong><br/>
  Posicione, rotacione, escale e salve objetos em qualquer osso do modelo com precisão.
</p>

<p>
  <img src="https://img.shields.io/badge/SA--MP-0.3.7-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Pawn-ZCMD-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/license-Personal%20Use%20Only-red?style=flat-square" />
  <img src="https://img.shields.io/badge/by-@olverjs-purple?style=flat-square" />
</p>

</div>

---

## 📸 Preview

> **Menu principal do editor**

![Menu](https://github.com/olverjscode/objtEdit/raw/main/preview/menu.png)

> **HUD de edição em tempo real**

![HUD](https://github.com/olverjscode/objtEdit/raw/main/preview/hud.png)

> **Menu de escolha do nome do projeto**

![Save](https://github.com/olverjscode/objtEdit/raw/main/preview/save.png)

---

## ✨ Features

- 🦴 **18 ossos suportados** — Coluna, Cabeça, Mãos, Pés, Clavículas, Pescoço e mais
- 📦 **Até 10 objetos por slot** — gerenciamento completo por índice
- 🎨 **Skin customizável** — troque o modelo do personagem diretamente no editor
- 🕹️ **Controle por cursor** — mova objetos com precisão em tempo real (PC only)
- 💾 **Salvamento automático** — exporta `SetPlayerAttachedObject` pronto para uso no arquivo `scriptfiles/saveObjtEdit.txt`
- 🖥️ **HUD visual** — 41 textdraws por jogador com todas as coordenadas em tempo real
- 🏷️ **Sistema de projetos** — nomeie cada sessão de edição para organização
- 🔑 **Tecla F** — abre o menu principal rapidamente
- 🔒 **Tecla ESC** — fecha o menu principal

---

## 📁 Estrutura do projeto

```
objtEdit/
├── gamemodes/
│   └── objt.amx           ← Gamemode compilado (pronto para uso)
├── pawno/
│   └── include/           ← Includes necessários para compilação
├── scriptfiles/
│   └── saveObjtEdit.txt   ← Arquivo de saída com os dados salvos
├── server.cfg             ← Configuração do servidor
├── samp-server.exe        ← Executável do servidor SA-MP
└── README.md
```

---

## ⚙️ Instalação

### Pré-requisitos

- **SA-MP Server** `0.3.7` ou superior
- **SA-MP Client** instalado no seu PC

### Passo a passo

**1.** Faça o download do repositório (botão **Code → Download ZIP** no GitHub)

**2.** Extraia o conteúdo para qualquer pasta no seu computador

**3.** Execute o arquivo `samp-server.exe`

**4.** Abra o cliente SA-MP e conecte em:
```
127.0.0.1:7777
```

**5.** Após conectar, pressione **F** para abrir o menu do editor

---

## 🕹️ Como usar

### Fluxo básico

```
1. Conecte ao servidor
2. Pressione [F] → abre o menu principal
3. Defina o nome do projeto
4. Selecione o slot do objeto (0–9)
5. Escolha o modelo (ID do objeto GTA SA)
6. Selecione o osso onde o objeto será fixado
7. Use os controles de cursor para mover/rotacionar/escalar
8. Salve — o código é exportado automaticamente
```

### Ossos disponíveis

| # | Osso | # | Osso |
|---|------|---|------|
| 1 | Coluna | 10 | Pé Dir. |
| 2 | Cabeça | 11 | Canela Dir. |
| 3 | Braço Esq. | 12 | Canela Esq. |
| 4 | Braço Dir. | 13 | Antebraço Esq. |
| 5 | Mão Esq. | 14 | Antebraço Dir. |
| 6 | Mão Dir. | 15 | Clavícula Esq. |
| 7 | Coxa Esq. | 16 | Clavícula Dir. |
| 8 | Coxa Dir. | 17 | Pescoço |
| 9 | Pé Esq. | 18 | Queixo |

### Coordenadas editáveis

| Campo | Descrição |
|-------|-----------|
| `Offset X / Y / Z` | Posição relativa ao osso |
| `Rot X / Y / Z` | Rotação do objeto |
| `Scale X / Y / Z` | Escala do objeto |

---

## 💾 Formato do arquivo salvo

Após salvar, o arquivo `scriptfiles/saveObjtEdit.txt` é gerado com o código pronto para copiar direto no seu gamemode:

```pawn
// ============================================================
//   ObjtEdit  |  Objeto Editor  -  BY @olverjs
//   https://github.com/olveirajs
// ============================================================

// ------------------------------------------------------------
// Projeto  : MeuProjeto
// Objeto   : MochilaTática
// Slot     : 0
// Id model : 19572
// Skin     : 170
// Osso     : Coluna
// ------------------------------------------------------------
SetPlayerAttachedObject(playerid, 0, 19572, 1,  0.0530, -0.2199, -0.1700,  0.0000, 0.0000, 0.0000,  1.0000, 1.0000, 1.0000);
```

---

## 👨‍💻 Autores

| Dev | GitHub |
|-----|--------|
| **@olverjs** | [github.com/olveirajs](https://github.com/olverjscode) |
| **@saresjs** | [github.com/Saresjs](https://github.com/Saresjs) |

> **LostWay Studios**

---

## 📜 Licença

```
Copyright (c) 2026 @olverjs — LostWay Studios

Este projeto é disponibilizado SOMENTE PARA USO PESSOAL.

Você PODE:
  ✔ Baixar e executar em ambiente local
  ✔ Usar as coordenadas geradas nos seus próprios projetos
  ✔ Estudar o funcionamento do código

Você NÃO PODE:
  ✖ Redistribuir o código-fonte (.pwn) ou compilado (.amx)
  ✖ Modificar e publicar versões derivadas
  ✖ Usar comercialmente sem autorização explícita do autor
  ✖ Remover os créditos dos autores

O arquivo .pwn (código-fonte) não é distribuído com este repositório.
Qualquer uso além do descrito acima requer autorização prévia por escrito.

Para contato: github.com/olverjscode
```

---

<div align="center">
  <sub>Feito com 💜 por <strong>@olverjs</strong> · LostWay Studios</sub>
</div>
