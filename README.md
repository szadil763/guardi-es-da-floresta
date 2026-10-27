# 🌲 Guardiões da Floresta: Lenhador Ilegal

Jogo em HTML criado pelos alunos, no qual você vive o papel de um lenhador ilegal para entender as consequências do desmatamento. Corte árvores, venda a madeira e tente não ser pego pela polícia.

## Como jogar

Abra o link do jogo (GitHub Pages):

https://szadil763.github.io/guardi-es-da-floresta/

Ou baixe o projeto e abra o arquivo `index.html` no navegador. Não precisa instalar nada.

Controles (teclado):

| Tecla | Ação |
|-------|------|
| W A S D | Mover o personagem |
| Espaço | Cortar a árvore mais próxima |
| E | Vender a madeira (50 de dinheiro por tora) |
| R | Jogar de novo (na tela final) |

O jogo precisa de teclado, então não funciona bem em celular.

## Objetivo

1. Missão 1: corte 5 árvores.
2. Missão 2: junte 1000 de dinheiro sem a **suspeita** chegar a 100%.

Cada árvore cortada aumenta a suspeita. Ela diminui devagar quando você para de cortar (mais rápido na neblina). Com 70% ou mais a polícia se aproxima, e com 100% você é preso. No fim, o jogo mostra o que o desmatamento ilegal causa.

## Estrutura

```
guardi-es-da-floresta/
├── index.html    # o jogo inteiro (visual + lógica)
├── README.md
└── CLAUDE.md
```

## Como mudar a dificuldade

No começo do código do `index.html`, procure o bloco "Ajustes do jogo":

```js
const SUSPEITA_POR_ARVORE=5;   // quanto a suspeita sobe a cada árvore cortada
const META_DINHEIRO=1000;      // dinheiro para vencer
const MUNDO=8000;              // tamanho do mapa
```

## Publicar no GitHub Pages

1. No repositório, vá em **Settings → Pages**.
2. Em **Source**, escolha **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/ (root)` e clique em **Save**.
4. Em 1 ou 2 minutos o jogo estará no ar.

## Créditos

Projeto criado pelos alunos com o GitHub Copilot, com orientação do professor Adilson.
