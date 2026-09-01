# Referência — Design System Rede Vip 24h

Tokens extraídos de duas fontes da verdade: o CSS de produção de **redevip24h.com.br** (paleta digital, fontes, raio) e o **logo vetorial `.ai` original** (cores de impressão). Boilerplate e componentes prontos para colar.

## Boilerplate base (copie e preencha)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rede Vip 24h</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Allura&family=Geist:wght@300..800&family=JetBrains+Mono:wght@400..800&family=Montserrat:wght@400..900&display=swap" rel="stylesheet">
<style>
:root{
  /* marca — digital */
  --brand-red:#C72C2F; --brand-red-dark:#9E2124; --brand-red-light:#E04B4E;
  --brand-yellow:#F5C518; --brand-yellow-dark:#D9A800; --brand-yellow-light:#FFDD5C;
  --brand-black:#0A0A0A; --brand-white:#FAFAFA; --brand-gray:#6B7280;
  /* marca — impresso / vetor (só para peça impressa e para o logo) */
  --print-red:#ED1C24; --print-yellow:#FFF200; --print-black:#231F20;
  /* superfícies claras (padrão) */
  --background:#FFFFFF; --foreground:#171717;
  --card:#FFFFFF; --card-foreground:#171717;
  --muted:#F5F5F5; --muted-foreground:#6B7280;
  --border:#E5E5E5; --input:#E5E5E5; --ring:var(--brand-red);
  /* superfícies escuras (hero, faixa, rodapé, peça de oferta) */
  --dark:#0A0A0A; --dark-2:#1E1E22; --dark-foreground:#FAFAFA;
  --dark-border:rgba(255,255,255,.12);
  /* sub-marca VIP Café */
  --cafe-brown:#4A2C1A; --cafe-cream:#F5ECD7; --cafe-gold:#C8A96E;
  --menu-paper:#FBEED2; --menu-banner:#6B2C12; --menu-desc:#B17B5C; --menu-yellow:#F2C84B;
  /* estado */
  --success:#22C55E; --warning:#F5C518; --danger:#C72C2F; --info:#2563EB;
  /* gráficos (nesta ordem) */
  --chart-1:#C72C2F; --chart-2:#F5C518; --chart-3:#4A2C1A; --chart-4:#2563EB; --chart-5:#6B7280;
  /* raio / sombra / fontes */
  --radius:.625rem; --radius-sm:.375rem; --radius-lg:1rem; --radius-full:9999px;
  --shadow-sm:0 1px 2px rgba(10,10,10,.06);
  --shadow:0 4px 16px rgba(10,10,10,.10);
  --shadow-lg:0 12px 40px rgba(10,10,10,.18);
  --glow-yellow:0 0 32px rgba(245,197,24,.45);
  --font-display:'Montserrat',sans-serif;
  --font-body:'Geist','Geist Variable',system-ui,sans-serif;
  --font-mono:'JetBrains Mono',monospace;
  --font-script:'Allura',cursive;
}
*{box-sizing:border-box}
body{margin:0;background:var(--background);color:var(--foreground);
  font-family:var(--font-body);font-weight:400;line-height:1.6;
  -webkit-font-smoothing:antialiased}
h1,h2,h3,h4,h5{font-family:var(--font-display);font-weight:800;line-height:1.15;
  letter-spacing:-.02em;margin:0 0 .5em}
h1{font-size:clamp(2rem,5vw,3.25rem);font-weight:900}
h2{font-size:clamp(1.5rem,3.5vw,2.25rem)}
h3{font-size:1.25rem;font-weight:700}
a{color:var(--brand-red);text-decoration:none}
a:hover{color:var(--brand-red-dark)}
.num,.price{font-family:var(--font-mono);font-variant-numeric:tabular-nums;font-weight:800}
.script{font-family:var(--font-script);font-weight:400}
.container{max-width:1180px;margin:0 auto;padding:0 24px}
.section{padding:clamp(48px,8vw,96px) 0}
.dark-section{background:var(--dark);color:var(--dark-foreground)}
.dark-section h1,.dark-section h2,.dark-section h3{color:var(--brand-white)}
</style>
</head>
<body>
  <!-- conteúdo -->
</body>
</html>
```

## Paleta completa

### Marca (digital — padrão)

| Token | Hex | Uso |
|---|---|---|
| `--brand-red` | `#C72C2F` | cor de campo, CTA principal, faixa, header |
| `--brand-red-dark` | `#9E2124` | hover do CTA, sombra do vermelho, texto sobre amarelo |
| `--brand-red-light` | `#E04B4E` | gradiente, estado ativo sutil |
| `--brand-yellow` | `#F5C518` | **destaque único**: preço, palavra-chave, selo, ícone |
| `--brand-yellow-dark` | `#D9A800` | hover de botão amarelo, borda |
| `--brand-black` | `#0A0A0A` | fundo dark, bloco de preço, rodapé |
| `--brand-white` | `#FAFAFA` | texto sobre vermelho/preto/foto |
| `--brand-gray` | `#6B7280` | texto secundário, legenda, disclaimer |

**Gradiente de marca:** `linear-gradient(135deg,#C72C2F,#9E2124)` — hero, header, faixa.
**Gradiente de preço:** `linear-gradient(180deg,#FFDD5C,#F5C518)` — número grande de oferta.
**Glow amarelo:** `box-shadow:var(--glow-yellow)` — bloco de preço sobre preto.

### Marca (impresso / logo)

`--print-red #ED1C24` · `--print-yellow #FFF200` · `--print-black #231F20`.
Só em cartaz A4, adesivo, fachada e **dentro do logo**. Em tela, use a paleta digital.

### VIP Café (sub-marca)

| Token | Hex | Uso |
|---|---|---|
| `--cafe-brown` | `#4A2C1A` | fundo e título da área café |
| `--cafe-cream` | `#F5ECD7` | superfície clara, card de café |
| `--cafe-gold` | `#C8A96E` | detalhe, filete, ícone |
| `--menu-paper` | `#FBEED2` | fundo do cardápio |
| `--menu-banner` / `--menu-title` | `#6B2C12` | faixa e título do cardápio |
| `--menu-desc` | `#B17B5C` | descrição do item |
| `--menu-yellow` | `#F2C84B` | preço no cardápio |

A palavra "Café" pode sair em `--font-script` (Allura). O resto do VIP Café é Montserrat.
O VIP Café **não substitui** o vermelho da rede: a assinatura da peça continua sendo o logo da Rede Vip.

### Contraste (calculado — respeite)

| Combinação | Ratio | Veredito |
|---|---|---|
| branco `#FAFAFA` sobre vermelho | **5,48:1** | ✅ texto corrido e título |
| preto `#0A0A0A` sobre amarelo | **12,2:1** | ✅ sempre |
| amarelo sobre vermelho | **3,36:1** | ⚠️ só ≥24px, ou ≥19px bold |
| vermelho sobre amarelo | **3,36:1** | ⚠️ só título grande (é o padrão da faixa de produto) |
| amarelo sobre branco | ~1,6:1 | ❌ nunca |
| branco sobre preto | 18,9:1 | ✅ sempre |

## Tipografia

- **Montserrat** → títulos, headline de oferta, nome de produto, marca. Pesos 700–900, `letter-spacing:-.02em`. Caixa alta em headline de cartaz.
- **Geist** → corpo, parágrafo, label, botão, navegação. Pesos 300–500.
- **JetBrains Mono** → **todo preço, número, litro, %, horário**. Peso 700–800 com `tabular-nums`. Use a classe `.num` / `.price`.
- **Allura** → exclusivamente a palavra "Café" na sub-marca VIP Café. Nunca em texto corrido.

Escala: `h1` clamp(2rem→3.25rem) · `h2` clamp(1.5rem→2.25rem) · `h3` 1.25rem · corpo 1rem/1.6 · legenda .875rem.

## Componentes

### Botões
```html
<button class="btn btn-primary">Ver ofertas</button>
<button class="btn btn-yellow">Baixar o app</button>
<button class="btn btn-outline">Nossas unidades</button>
```
```css
.btn{font-family:var(--font-body);font-weight:600;font-size:1rem;
  padding:.75rem 1.5rem;border-radius:var(--radius);border:2px solid transparent;
  cursor:pointer;transition:.18s ease;display:inline-flex;align-items:center;gap:.5rem}
.btn-primary{background:var(--brand-red);color:var(--brand-white)}
.btn-primary:hover{background:var(--brand-red-dark)}
.btn-yellow{background:var(--brand-yellow);color:var(--brand-black)}
.btn-yellow:hover{background:var(--brand-yellow-dark)}
.btn-outline{background:transparent;color:var(--brand-red);border-color:var(--brand-red)}
.btn-outline:hover{background:var(--brand-red);color:var(--brand-white)}
.dark-section .btn-outline{color:var(--brand-white);border-color:rgba(255,255,255,.4)}
```

### Card
```css
.card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius-lg);
  padding:24px;box-shadow:var(--shadow-sm);transition:.18s ease}
.card:hover{box-shadow:var(--shadow);transform:translateY(-2px)}
.card-accent{border-top:4px solid var(--brand-red)}
```

### Cartão de vidro sobre foto (assinatura da marca)
```css
.glass{background:rgba(20,20,20,.55);backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);
  border:1px solid rgba(255,255,255,.25);border-radius:var(--radius-lg);
  padding:28px 32px;color:var(--brand-white)}
```
Use sobre foto do posto/produto. Texto principal em branco, **uma** linha em `--brand-yellow`.

### Bloco de preço (o elemento mais importante de peça de oferta)
```html
<div class="price-block">
  <span class="price-label">Por apenas</span>
  <span class="price"><small>R$</small>9,90</span>
  <span class="price-unit">cada</span>
</div>
```
```css
.price-block{background:var(--brand-black);border:2px solid var(--brand-yellow);
  border-radius:var(--radius-lg);box-shadow:var(--glow-yellow);
  padding:16px 28px;display:inline-flex;align-items:baseline;gap:.5rem;color:var(--brand-white)}
.price-label{font-family:var(--font-body);font-weight:600;font-size:.95rem;
  text-transform:uppercase;letter-spacing:.06em}
.price{font-family:var(--font-mono);font-weight:800;font-size:clamp(2.5rem,7vw,4.5rem);
  line-height:1;color:var(--brand-yellow);font-variant-numeric:tabular-nums}
.price small{font-size:.45em;margin-right:.1em}
.price-unit{font-family:var(--font-body);font-weight:600;font-size:.9rem;color:var(--brand-white)}
```

### Faixa de produto (amarela, texto vermelho)
```css
.product-bar{background:var(--brand-yellow);color:var(--brand-red);
  font-family:var(--font-display);font-weight:800;font-size:1.5rem;
  padding:.5rem 1.5rem;border-radius:var(--radius-full);display:inline-block}
```

### Hero
```html
<section class="hero">
  <div class="container">
    <h1>Abastecer, comer e resolver — <span class="hl">24 horas</span>.</h1>
    <p class="lead">Postos em Porto Alegre, Canoas e Alvorada. Combustível Shell e Ipiranga, GNV, troca de óleo e VIP Café.</p>
    <a class="btn btn-yellow" href="#">Ver ofertas do mês</a>
  </div>
</section>
```
```css
.hero{background:linear-gradient(135deg,#C72C2F,#9E2124);color:var(--brand-white);
  padding:clamp(64px,10vw,128px) 0}
.hero .hl{color:var(--brand-yellow)}
.hero .lead{font-size:1.125rem;max-width:56ch;opacity:.92;margin-bottom:2rem}
```
Variante com foto: `background:linear-gradient(rgba(10,10,10,.55),rgba(10,10,10,.55)),url(foto.jpg) center/cover`.

### Selo circular ("Sabores que te movem!")
```css
.seal{background:var(--brand-black);color:var(--brand-white);
  border:2px solid var(--brand-yellow);border-radius:var(--radius-full);
  width:160px;height:160px;display:grid;place-content:center;text-align:center;
  font-family:var(--font-display);font-weight:800;text-transform:uppercase;
  line-height:1.15;font-size:.95rem;padding:12px}
```

### Faixa de benefícios (rodapé de peça)
Três colunas: ícone amarelo + duas linhas — `ENERGIA / QUE TE MOVE`, `QUALIDADE / QUE VOCÊ CONFIA`, `CONVENIÊNCIA / PARA VOCÊ`. Primeira linha em branco 700, segunda em branco 400 ou `--brand-gray`.

### Tabela de preço de combustível
```css
.fuel-table{width:100%;border-collapse:collapse;font-family:var(--font-body)}
.fuel-table th{background:var(--brand-red);color:var(--brand-white);
  font-family:var(--font-display);font-weight:700;text-align:left;padding:12px 16px}
.fuel-table td{padding:12px 16px;border-bottom:1px solid var(--border)}
.fuel-table td.val{font-family:var(--font-mono);font-weight:700;text-align:right;
  font-variant-numeric:tabular-nums}
.fuel-table tr:hover td{background:var(--muted)}
```

### Header e rodapé
- **Header:** fundo branco, `logo-principal.svg` à esquerda (altura 40px), navegação Geist 500, CTA `btn-primary` à direita. Em scroll, `box-shadow:var(--shadow-sm)`.
- **Rodapé:** fundo `--brand-black`, `logo-branco.svg` (altura 48px), colunas em `--brand-gray`, filete superior `2px solid var(--brand-red)`.

## Voz e conteúdo

Direta, prática, de bairro — sem formalidade corporativa. Fala de rotina real: o café antes do trabalho, o tanque na volta pra casa, a madrugada. Frases curtas, segunda pessoa, uma ideia por peça. Ex.: *"Se a segunda-feira tá difícil de engatar, a gente tem o aditivo certo."* · *"Café da manhã no VIP Café."* · *"Mais energia para o seu dia!"*

Toda peça de oferta leva **produto + preço + validade**. O disclaimer vai em `--brand-gray` .8rem no rodapé: *"Promoções válidas de 01/06 a 30/06 ou enquanto durarem os estoques."*
