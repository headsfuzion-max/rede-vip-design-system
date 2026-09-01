---
name: rede-vip-design-system
description: Aplica o Design System oficial da Rede Vip 24h (tokens, cores, fontes, logos, componentes) em qualquer peça HTML/UI ou criativo. Use quando o usuário pedir para criar/estilizar landing page, one-pager, proposta, apresentação, e-mail, card, componente, post de feed, story, cartaz A4 de oferta, mockup, ou disser "no visual da Rede Vip", "identidade da Rede Vip", "cores da Rede Vip", "DS da Vip 24h", "Vip Café".
---

# Design System — Rede Vip 24h

Rede de postos de combustível 24 horas em Porto Alegre, Canoas e Alvorada (Shell e Ipiranga, GNV, troca de óleo, conveniência, app com descontos e a sub-marca **VIP Café**).

O visual é **vermelho + amarelo sobre preto**, com foto real do posto/produto, cartão de vidro sobre a foto e preço gigante. Nunca invente cor, fonte ou raio — use os tokens.

## Arquivos desta skill

| Arquivo | Quando abrir |
|---|---|
| [`reference.md`](reference.md) | **Sempre.** Tokens completos, boilerplate HTML e componentes web (botão, card, hero, tabela de preço, header/footer). |
| [`creative.md`](creative.md) | Peça gráfica: post de feed, story, carrossel, cartaz A4 de oferta, capa de Reels. Traz os formatos, as receitas visuais e os artboards para o Claude Design. |
| [`assets/`](assets/) | Logos vetoriais (SVG). Ver "Logo" abaixo. |

## Fluxo

1. Entenda **o que** é a peça (web/UI ou criativo gráfico) e **onde salvar**.
2. Abra `reference.md` (sempre) e `creative.md` (se for peça gráfica).
3. Comece do **boilerplate** — ele já traz os tokens como CSS variables e o import das fontes. Copie e preencha.
4. Use só as variáveis (`var(--brand-red)`), nunca hex cru repetido.
5. Entregue um arquivo **self-contained** (CSS inline no `<head>`, fontes via Google Fonts, logo inline do `assets/`).

## Tokens essenciais (completo em reference.md)

| Papel | Token | Hex |
|---|---|---|
| Vermelho da marca | `--brand-red` | `#C72C2F` |
| Amarelo da marca | `--brand-yellow` | `#F5C518` |
| Preto / fundo dark | `--brand-black` | `#0A0A0A` |
| Branco / fundo light | `--brand-white` | `#FAFAFA` |
| Cinza de apoio | `--brand-gray` | `#6B7280` |
| Raio | `--radius` | `0.625rem` |

Fontes: títulos **Montserrat** (700–900) · corpo/UI **Geist** · preço e número **JetBrains Mono** · script **Allura** (só na palavra "Café" do VIP Café).

## Duas paletas — digital vs. impresso

A marca tem duas gerações de vermelho/amarelo. **Escolha pelo destino, não por gosto:**

- **Digital (site, LP, e-mail, UI, post):** `#C72C2F` / `#F5C518`. É o que está no ar em redevip24h.com.br e o que este DS assume por padrão.
- **Impresso e logo vetorial (cartaz A4, adesivo, fachada):** `#ED1C24` / `#FFF200` / preto `#231F20` — as cores dentro do arquivo `.ai` original.

**Nunca reColora o logo.** O SVG em `assets/` carrega as cores originais (`#ED1C24`/`#FFF200`) de propósito; sobre fundo colorido use `logo-branco.svg`.

## Logo

| Arquivo | Uso |
|---|---|
| `assets/logo-principal.svg` | Padrão: "REDE Vip 24horas". Header, rodapé, assinatura de peça. |
| `assets/logo-assinatura-completa.svg` | Com "Postos de combustíveis". Documento formal, cartaz institucional, primeira impressão. |
| `assets/logo-horizontal.svg` | "Vip 24horas" sem "REDE". Espaço apertado, faixa horizontal. |
| `assets/logo-compacto.svg` | Versão travada mais estreita da principal. |
| `assets/simbolo.svg` | Só o símbolo (swoosh + "Vip"). Avatar, favicon, selo, marca d'água. |
| `assets/logo-branco.svg` | Monocromático branco. **Use sempre sobre foto, vermelho ou preto.** |

Regras: altura mínima 24px em tela / 12mm impresso · área de respiro = altura do "V" em todos os lados · nunca distorça, gire, aplique sombra dura ou troque as cores · sobre foto, use o branco e garanta que a área atrás esteja escurecida.

## Regras duras do DS

1. **Vermelho é o campo, amarelo é o destaque.** O vermelho pinta a área; o amarelo marca **uma** coisa por peça (o preço, a palavra-chave, o selo). Amarelo em tudo mata a hierarquia.
2. **Preço é sempre o maior elemento** de peça de oferta, em JetBrains Mono 800, e nunca compete com o título.
3. **Contraste (medido):** branco sobre `--brand-red` = 5,48:1 ✅ texto corrido. Amarelo sobre vermelho = 3,36:1 → **só título grande** (≥24px ou ≥19px bold), nunca corpo. Preto sobre amarelo = 12,2:1 ✅ sempre. Nunca amarelo sobre branco.
4. **Foto real do posto/produto** sempre que houver imagem — a marca é de lugar físico, não de ilustração. Foto escurecida (overlay preto 35–55%) quando levar texto por cima.
5. **Cartão de vidro** é o recipiente de texto sobre foto: `background:rgba(20,20,20,.55)`, `backdrop-filter:blur(12px)`, borda `1px solid rgba(255,255,255,.25)`, `--radius-lg`.
6. **VIP Café tem paleta própria** (marrom/creme/dourado) — é sub-marca, não substitui o vermelho da rede. Ver `reference.md`.
7. **Só variáveis.** Nunca hardcode um hex que já existe como token.
8. Layout responsivo com flex/grid; posição absoluta só em peça de tamanho fixo (criativo).
