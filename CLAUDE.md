# CLAUDE.md

Jogo em HTML 3D (three.js) "Lenhador Ilegal", do projeto Guardiões da Floresta. Projeto de alunos, orientado pelo professor Adilson. O objetivo pedagógico é mostrar as consequências do desmatamento ilegal.

## Regras do projeto

- Tudo fica em um único `index.html` (HTML, CSS e JavaScript). Sem build e sem imagens externas: tudo é montado com formas 3D.
- A única dependência é o three.js r128, carregado do cdnjs por uma tag `<script>` (sem módulos). Por isso o jogo precisa de internet.
- Idioma da interface e dos comentários: português do Brasil.
- O jogo é publicado no GitHub Pages a partir da branch `main`, pasta raiz.
- Controles: W A S D (ou setas) mover/dirigir, Espaço cortar, E falar/vender, F entrar e sair do carro, 1 a 5 opções das conversas, M música, G gráficos, Enter começar, R reiniciar na tela final.
- Música e efeitos são gerados com Web Audio no próprio código (sem arquivos de áudio).
- Os números que mudam a dificuldade ficam juntos, no bloco "Ajustes do jogo" (`SUSPEITA_POR_ARVORE`, `QUEDA_SUSPEITA`, `META_DINHEIRO`, `MUNDO`, `NUM_ARVORES`, `VELOCIDADE`, `VELOCIDADE_CARRO`, `PRECO_TORA`, `PRECO_TORA_NORTE`, `CAPACIDADE_MOCHILA`, `CAPACIDADE_CARRO`, `RAIO_FISCAL`), seguidos das listas `NIVEIS_MACHADO` e `SKINS`. As missões ficam na lista `MISSOES` e as curiosidades em `FATOS`.
- Pense em computadores de escola: mantenha o modo de gráficos leves (tecla G) funcionando e use `InstancedMesh` para objetos repetidos.

## Cuidados ao alterar

- Mantenha o código simples e legível: os alunos precisam conseguir ler e editar.
- A tela final deve continuar mostrando a mensagem sobre os danos do desmatamento ilegal.
- Teste abrindo o `index.html` no navegador antes de enviar.
