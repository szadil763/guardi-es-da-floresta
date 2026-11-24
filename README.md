# 🌲 Guardiões da Floresta: Lenhador Ilegal

Jogo em HTML criado pelos alunos, no qual você vive o papel de um lenhador ilegal para entender as consequências do desmatamento. Corte árvores, venda a madeira e tente não ser pego pela polícia.

## Como jogar

Abra o link do jogo (GitHub Pages):

https://szadil763.github.io/guardi-es-da-floresta/

Ou baixe o projeto e abra o arquivo `index.html` no navegador. Não precisa instalar nada, mas precisa de internet: o jogo usa a biblioteca [three.js](https://threejs.org/) para desenhar a floresta em 3D.

Controles (teclado):

| Tecla | Ação |
|-------|------|
| W A S D (ou setas) | Mover o personagem / dirigir a caminhonete |
| Espaço | Cortar a árvore mais próxima |
| E | Falar com os personagens e vender madeira na serraria |
| F | Entrar e sair da caminhonete (depois de ganhá-la) |
| 1 a 5 | Escolher opções nas conversas (loja e ferreiro) |
| M | Ligar e desligar a música |
| G | Gráficos completos ou leves (para computadores mais fracos) |
| R | Jogar de novo (na tela final) |
| Enter | Começar o jogo |

O jogo precisa de teclado, então não funciona bem em celular. Se o computador for lento, o jogo muda sozinho para os gráficos leves.

## Objetivo

O Seu Zé, um madeireiro que não liga para a lei, dá as missões na vila. Siga o feixe de luz amarela (e o círculo no minimapa) para saber aonde ir:

1. Corte 5 árvores.
2. Venda 5 toras na serraria da vila.
3. Melhore o machado com o Ferreiro Tião.
4. Compre uma roupa nova na loja da Dona Rosa.
5. Corte 15 árvores e ganhe a caminhonete.
6. Venda 20 toras na Serraria do Norte (que paga o dobro).
7. Corte uma castanheira, árvore protegida por lei, do outro lado do rio.
8. Chegue ao nível 4 de ferramenta.
9. Junte 3000 de dinheiro sem ser preso.

Cada árvore cortada aumenta a **suspeita** (a castanheira aumenta muito mais). Os fiscais patrulham a floresta: se um deles vir você cortando, a suspeita sobe rápido. Ela diminui devagar quando você para de cortar (mais rápido à noite e na neblina). Com 70% ou mais a polícia se aproxima, e com 100% você é preso. No fim, o jogo mostra o que o desmatamento ilegal causa.

## O que tem no jogo

- **Mundo aberto**: vila, floresta, rio com ponte, lago, estradas de terra, Serraria do Norte e a floresta antiga de castanheiras.
- **Personagens**: Seu Zé (missões), Ferreiro Tião (melhora o machado), Dona Rosa (loja de roupas) e os fiscais ambientais.
- **Ferramentas**: machado velho, de ferro, de aço, de ouro e motosserra (corta muito rápido, mas faz barulho).
- **Roupas (skins)**: xadrez vermelho, explorador, xadrez azul, ninja da noite e dourado.
- **Caminhonete**: anda rápido, leva até 30 toras e mostra a madeira na caçamba.
- **Interface**: dinheiro, madeira, ferramenta, barra de suspeita, minimapa, relógio, clima e cartão da missão.
- **Visual e som**: dia e noite com estrelas, sol, lua, vaga-lumes, pássaros, chuva, neblina, sombras, música de fundo (fica tensa quando a polícia está chegando) e efeitos sonoros. Tudo é desenhado e tocado pelo próprio navegador, sem arquivos de imagem ou de áudio.
- **Você sabia?**: de tempos em tempos aparecem curiosidades sobre as florestas e a lei.

## Estrutura

```
guardi-es-da-floresta/
├── index.html    # o jogo inteiro (visual 3D com three.js + lógica)
├── README.md
└── CLAUDE.md
```

## Como mudar a dificuldade

No começo do código do `index.html`, procure o bloco "Ajustes do jogo":

```js
const SUSPEITA_POR_ARVORE=4;   // quanto a suspeita sobe a cada árvore cortada
const QUEDA_SUSPEITA=0.012;    // quanto a suspeita cai por quadro quando você para de cortar
const META_DINHEIRO=3000;      // dinheiro da última missão (para vencer)
const MUNDO=600;               // tamanho do mapa (em metros)
const NUM_ARVORES=1800;        // quantas árvores existem na floresta
const VELOCIDADE=0.2;          // velocidade do lenhador a pé
const VELOCIDADE_CARRO=0.9;    // velocidade máxima da caminhonete
const PRECO_TORA=40;           // preço de cada tora na serraria da vila
const PRECO_TORA_NORTE=80;     // preço de cada tora na Serraria do Norte
const CAPACIDADE_MOCHILA=10;   // quantas toras cabem na mochila
const CAPACIDADE_CARRO=30;     // quantas toras cabem depois de ganhar a caminhonete
const RAIO_FISCAL=28;          // distância que o fiscal consegue ver você cortando
```

Logo abaixo ficam as listas `NIVEIS_MACHADO` (nome, força e preço de cada ferramenta) e `SKINS` (nome, preço e cores de cada roupa). Mais para baixo, a lista `MISSOES` tem o texto, a meta e a recompensa de cada missão, e a lista `FATOS` tem as curiosidades. Dá para mudar ou acrescentar itens nelas.


## Publicar no GitHub Pages

1. No repositório, vá em **Settings → Pages**.
2. Em **Source**, escolha **Deploy from a branch**.
3. Selecione a branch `main` e a pasta `/ (root)` e clique em **Save**.
4. Em 1 ou 2 minutos o jogo estará no ar.

## Créditos

Projeto criado pelos alunos com o GitHub Copilot, com orientação do professor Adilson.
