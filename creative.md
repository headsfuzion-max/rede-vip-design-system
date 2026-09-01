# Peças gráficas — Rede Vip 24h

Receitas dos criativos da marca: feed, story, carrossel, cartaz A4 e cardápio. Use junto com os tokens de [`reference.md`](reference.md).

## Formatos (artboards)

| Peça | Tamanho (px) | Observação |
|---|---|---|
| Post de feed | **1080 × 1350** (4:5) | formato padrão da marca |
| Post quadrado | 1080 × 1080 | só quando o cliente pedir |
| Story / Reels / capa | **1080 × 1920** (9:16) | zona segura: 250px topo, 320px base |
| Carrossel | 1080 × 1350 por card | capa + 3 a 6 cards |
| Cartaz A4 (tela) | **1414 × 2000** | proporção A4; para gráfica, 2480 × 3508 @300dpi |
| A3 duplo (encarte) | 2000 × 1414 (paisagem) | grade de ofertas |
| Cardápio VIP Café | 1414 × 2000 | paleta café, fundo `--menu-paper` |

No **Claude Design**, cada peça é um artboard `.dc.html` com `width`/`height` fixos nesses valores, lado a lado no canvas. Use posição absoluta à vontade — é peça de tamanho fixo, não layout responsivo.

## Elementos assinatura da marca

Todo criativo da Rede Vip usa alguns desses, nunca todos ao mesmo tempo:

- **Foto real** do posto, da loja ou do produto — nunca ilustração genérica. É marca de lugar físico.
- **Cartão de vidro** sobre a foto para receber o texto (`.glass` do reference). Em story, pode ganhar um "rabinho" de balão de fala apontando para o elemento citado.
- **Sparkle amarelo** — estrela de 6 a 8 pontas em `--brand-yellow`, 2 a 4 por peça, tamanhos diferentes, nas bordas. Nunca sobre o rosto ou o preço.
- **Moldura de canto** — filete `1px rgba(255,255,255,.35)` afastado 40px da borda, com cantos arredondados; às vezes só nos cantos.
- **Faixa amarela de produto** — pílula amarela com o nome do produto em vermelho, Montserrat 800.
- **Bloco de preço preto** com contorno e número amarelos, ou preço em branco gigante direto sobre o vermelho.
- **Assinatura**: `logo-branco.svg` centralizado no rodapé (feed/story) ou `logo-principal.svg` dentro de uma caixa branca arredondada no topo direito (cartaz).

### SVG do sparkle
```html
<svg viewBox="0 0 100 100" width="96" height="96" aria-hidden="true">
  <path fill="#F5C518" d="M50 0 L58 34 L92 20 L66 46 L100 50 L66 54 L92 80 L58 66 L50 100 L42 66 L8 80 L34 54 L0 50 L34 46 L8 20 L42 34 Z"/>
</svg>
```

## Receita 1 — Post de feed sobre foto (comunicação)

Fundo: foto do posto/produto cobrindo o artboard, com `linear-gradient(rgba(10,10,10,.45),rgba(10,10,10,.25))` por cima.

1. Moldura de canto branca a 40px da borda.
2. Cartão de vidro no terço superior, largura ~78%, padding 48px.
3. Dentro: headline Montserrat 800, ~64px, branco — com **uma** linha ou expressão em `--brand-yellow`. Máximo 4 linhas.
4. Filete de 3px sob o headline: metade amarela, metade vermelha, largura ~120px.
5. Subtítulo/pergunta em Geist 500, 32px, branco 85%, com seta `→` quando puxar interação.
6. Sparkles amarelos: 1 grande fora do cartão à esquerda, 1 pequeno na base oposta.
7. `logo-branco.svg` centralizado, altura ~72px, a 80px da base.

## Receita 2 — Post de oferta (fundo vermelho)

Fundo: `--brand-red` (ou `--print-red` se for para impressão) com textura sutil — ruído/pontilhado a 6% de opacidade.

1. Card do produto centralizado no topo: quadrado ~72% da largura, `border-radius: 48px`, fundo em gradiente laranja→amarelo (`linear-gradient(160deg,#F5A623,#F5C518)`) ou vidro claro, borda `2px rgba(255,255,255,.6)`.
2. Foto do produto recortada (PNG sem fundo) centralizada dentro do card, com brilhos brancos de 4 pontas nas quinas.
3. Badge circular amarelo no canto inferior direito do card (ícone vermelho: coração, raio, tag).
4. Faixa amarela de produto logo abaixo, alinhada à esquerda, com um selo quadrado vermelho de etiqueta antes do texto.
5. **Preço**: `R$` em ~90px e o inteiro em ~220px, JetBrains Mono 800 branco, centavos menores sobrescritos. É o maior elemento da peça.
6. Sparkles amarelos nos quatro cantos, tamanhos alternados.
7. `logo-branco.svg` centralizado no rodapé.

## Receita 3 — Cartaz A4 de oferta

Estrutura de cima para baixo:

1. **Topo**: faixa vermelha com corte diagonal na base (`clip-path`), ocupando ~28% da altura. Headline em caixa alta, duas linhas: a primeira em branco, a segunda em amarelo com contorno/sombra preta. Montserrat 900, itálico opcional.
2. **Logo** em caixa branca arredondada no canto superior direito, usando `logo-assinatura-completa.svg`.
3. **Selo circular preto** com contorno amarelo à direita, abaixo do topo, com a chamada curta.
4. **Miolo**: foto dos produtos em fundo escuro desfocado (bokeh quente).
5. **Base**: bloco preto à esquerda com nome/volume/variação do produto (branco, com a última linha em amarelo) e, ao lado, o **bloco de preço preto com contorno amarelo** — `POR APENAS` + `R$ 9,90` gigante em amarelo + `CADA`.
6. **Faixa de benefícios** em três colunas com ícones amarelos.
7. **Disclaimer** de validade centralizado, `--brand-gray`, com as datas em amarelo.

Para gráfica, use a paleta `--print-*` e exporte a 300dpi.

## Receita 4 — Story

Mesma lógica do feed em 1080 × 1920, com:
- Cartão de vidro em formato de **balão de fala** (com rabinho triangular) posicionado no terço superior, apontando para o elemento da foto que o texto cita.
- Área de respiro maior no topo (avatar/nome do perfil) e na base (barra de resposta).
- Enquete/caixinha: cartão de vidro estreito, pergunta em branco, opções em pílulas amarelas com texto vermelho.
- CTA "arrasta pra cima" / seta `↑` em amarelo acima da zona segura inferior.

## Receita 5 — Carrossel

- **Capa**: Receita 1, com o headline prometendo a lista ("3 coisas que você resolve às 3 da manhã").
- **Cards internos**: fundo `--brand-black` ou foto escurecida, número do card em JetBrains Mono 800 amarelo gigante no canto, título Montserrat 700 branco, corpo Geist 400.
- **Último card**: CTA em fundo vermelho, botão amarelo, endereço/unidades, logo branco.
- Indicador de continuidade: seta `→` amarela no canto direito de todos menos o último.

## Checklist antes de entregar

- [ ] Uma só coisa em amarelo (o destaque). O resto é branco, vermelho ou preto.
- [ ] Preço em JetBrains Mono, é o maior elemento da peça de oferta.
- [ ] Foto real, escurecida onde tem texto por cima.
- [ ] Logo branco sobre fundo colorido/foto; logo colorido só sobre branco.
- [ ] Área de respiro do logo respeitada (altura do "V").
- [ ] Texto pequeno nunca em amarelo sobre vermelho ou branco.
- [ ] Peça de oferta tem produto, preço e validade.
- [ ] Zona segura respeitada em story.
