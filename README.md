# ♞ Xadrez Online

Jogo de xadrez para jogar **online com um amigo** (por link de convite), **contra o computador** ou **a dois no mesmo aparelho**. Funciona no celular e no computador.

Tudo fica em um único arquivo, o `index.html`, com o código comentado em português para quem está começando a programar.

## Como jogar

1. Abra o site do jogo.
2. Escolha o relógio, o nível do PC e a sua cor.
3. Escolha o modo:
   - **Criar partida online e convidar**: o jogo gera um link. Mande para o seu amigo; quando ele abrir, a partida começa.
   - **Jogar contra o PC**: três níveis (Fácil, Médio e Difícil).
   - **Jogar a dois neste aparelho**: os dois jogadores revezam no mesmo celular ou computador.
4. Para mover, toque na peça e depois no destino, ou arraste a peça.

## O que o jogo tem

- Todas as regras do xadrez: xeque, xeque-mate, empate, roque, en passant e promoção (você escolhe a peça)
- Relógio: 3, 5 ou 10 minutos, ou 15 + 10 (15 minutos e mais 10 segundos por lance)
- Desistir, propor empate e pedir revanche (na revanche as cores trocam)
- Chat entre os dois jogadores no modo online
- Sons de lance, captura, xeque e fim de jogo
- Seis temas de tabuleiro e três conjuntos de peças
- Lista de lances, peças capturadas e vantagem em pontos

## Como o jogo é montado

Pense no jogo em 3 partes:

| Parte | Quem faz | Para que serve |
|---|---|---|
| Tabuleiro | Código próprio (HTML, CSS e desenhos SVG) | Mostra o tabuleiro e as peças e recebe os toques |
| Juiz | Biblioteca [chess.js](https://github.com/jhlywa/chess.js) | Confere se cada lance é válido e detecta xeque-mate e empate |
| Carteiro | Biblioteca [PeerJS](https://peerjs.com/) | Leva os lances e as mensagens de um jogador até o outro |

O computador joga usando o método **minimax com corte alfa-beta**: ele imagina alguns lances à frente e escolhe o que deixa a posição melhor para ele. O nível define quantos lances à frente ele imagina.

## Como publicar (GitHub Pages)

1. No repositório, abra **Settings → Pages**.
2. Em **Branch**, escolha `main` e a pasta `/ (root)`, depois clique em **Save**.
3. Em um ou dois minutos, o endereço do jogo aparece no topo dessa página.

O modo online só funciona com o site publicado na internet, porque os dois jogadores precisam acessar o mesmo endereço.

## Limitações conhecidas

- Em algumas redes (certos 4G e Wi-Fi de empresas ou escolas), a conexão direta entre os dois aparelhos pode não funcionar.
- No modo online, cada jogador conta o próprio relógio, e os dois se acertam a cada lance; pode haver diferença de até um segundo.

## Licença

Código aberto sob a licença [MIT](LICENSE). As bibliotecas usadas têm licenças próprias: chess.js (BSD-2-Clause) e PeerJS (MIT).
