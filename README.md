# Design System — Rede Vip 24h

Skill do Claude Code com o design system oficial da **Rede Vip 24h** (rede de postos 24h em Porto Alegre, Canoas e Alvorada). Instalando isso, qualquer Claude da agência gera landing page, proposta, apresentação, post, story ou cartaz de oferta já na identidade certa — sem precisar mandar cor, fonte ou logo junto.

## Instalar

```bash
git clone https://github.com/headsfuzion-max/rede-vip-design-system.git ~/.claude/skills/rede-vip-design-system
```

No Windows (PowerShell):

```powershell
git clone https://github.com/headsfuzion-max/rede-vip-design-system.git "$env:USERPROFILE\.claude\skills\rede-vip-design-system"
```

Reinicie o Claude Code. A skill aparece como `rede-vip-design-system` e dispara sozinha quando alguém pede algo "no visual da Rede Vip".

## Atualizar

```bash
cd ~/.claude/skills/rede-vip-design-system && git pull
```

## O que tem aqui

| Arquivo | Conteúdo |
|---|---|
| `SKILL.md` | Regras duras do DS, tokens essenciais, uso do logo. É o que o Claude lê primeiro. |
| `reference.md` | Paleta completa, tipografia, boilerplate HTML e componentes (botão, card, vidro, bloco de preço, hero, tabela de combustível). |
| `creative.md` | Formatos e receitas de peça gráfica: feed, story, carrossel, cartaz A4, cardápio. Inclui os artboards para o Claude Design. |
| `assets/*.svg` | Seis variações do logo em vetor, extraídas do `.ai` original. |

## Resumo da marca

- **Vermelho** `#C72C2F` · **Amarelo** `#F5C518` · **Preto** `#0A0A0A` (digital)
- **Vermelho** `#ED1C24` · **Amarelo** `#FFF200` (impresso e dentro do logo)
- Montserrat (títulos) · Geist (corpo) · JetBrains Mono (preço) · Allura (só "Café")
- Foto real do posto, cartão de vidro sobre a foto, preço gigante, amarelo só no destaque.

## Fontes da verdade

- Paleta digital, fontes e raio: CSS de produção de [redevip24h.com.br](https://www.redevip24h.com.br/)
- Cores de impressão e vetores do logo: arquivo `.ai` original da marca
- Elementos de criativo: peças aprovadas de feed, story e cartazes A4

Se o site mudar, ele vence — atualize `reference.md` aqui e dê push.

---

Mantido pela [Fuzion](https://github.com/headsfuzion-max). Mesmo molde da skill `fuzion-design-system`.
