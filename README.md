# Milano Concierge

Quatro ferramentas pessoais para a transição de chef de sala para concierge de hotel em Milão.

**Guia Mestre** — `index.html`
Página de leitura com 36 módulos: geografia, história, museus, gastronomia, transporte,
perfis culturais por nacionalidade, playbook de casos difíceis (agora com os Três Passos
da Ritz-Carlton e os 5 A's de Danny Meyer), hotéis 5★, experiências premium com operadores
e contatos, diretório de contatos, página de preparação para entrevista (incluindo técnicas
de entrevista verbal e negociação) e um índice de consulta com os 183 endereços em 52 categorias.
Tem sumário lateral, busca e modo claro/escuro. Não guarda estado.

**Fichas** — `fichas.html`
App de campo. 183 lugares organizados em 16 blocos de visitas — 12 semanas por bairro, mais rede de
serviços, hotéis boutique, experiências premium e vida noturna. Em cada ficha:
nota, faixa de preço, perfil, ocasião, ruído, tamanho de grupo, serve com chuva,
LGBTQIA+ friendly, acessível, pontos fracos e três campos de texto.
Aba de consulta que devolve A/B/C a partir do perfil do hóspede.

**Hospitalidade de luxo** — `hospitalidade.html`
Resumo aplicado à Terrazza do que ensinam Ritz-Carlton, Forbes Travel Guide, Danny Meyer,
Will Guidara, a escola italiana de sala, Les Clefs d'Or e a pesquisa de Cornell/50 Best:
os 7 princípios comuns, a jornada do hóspede momento a momento, o que fazer quando algo dá
errado, rituais de equipe, ideias de baixo custo para propor à direção e como registrar
cada caso (método STAR) para virar experiência comprovável em entrevista.

**Guia de vinhos** — `vinhos.html`
Ferramenta de equipe da Terrazza (não exclusiva da transição de carreira): carta de vinhos
e harmonização com o cardápio, em 10 idiomas, com perfil de sabor, temperatura de serviço,
glossário de termos e sugestão da casa. Tem uma terceira aba, **Aromas**, com os 34 pratos
do cardápio da Terrazza (composição, perfil gustativo, aroma e fragrância, textura, como
apresentar ao cliente, alérgenos e uma nota interna), em PT/IT/EN/ES com fallback para
inglês nos outros idiomas — fonte: o Manual de Conhecimento Gastronômico da casa. Hospedada
aqui para ficar no mesmo endereço das outras três páginas, com link de volta para elas.

## Publicar no GitHub Pages

1. Criar um repositório (sugestão: `milano-concierge`).
2. Subir `index.html`, `fichas.html`, `hospitalidade.html`, `vinhos.html`, este README,
   `manifest.webmanifest`, `icon-180.png`, `icon-192.png`, `icon-512.png`, `favicon-32.png`
   e `favicon-16.png` — **tudo na raiz do repositório**, sem subpasta.
3. Settings → Pages → Source: `Deploy from a branch` → branch `main`, pasta `/ (root)`.
4. Aguardar um minuto. Os endereços ficam:
   - Guia: `https://<usuario>.github.io/milano-concierge/`
   - Fichas: `https://<usuario>.github.io/milano-concierge/fichas.html`
   - Hospitalidade: `https://<usuario>.github.io/milano-concierge/hospitalidade.html`
   - Vinhos: `https://<usuario>.github.io/milano-concierge/vinhos.html`

## Ícone na tela de início (Adicionar à Tela de Início)

Só o **Guia Mestre** (`index.html`) aponta para os arquivos de ícone (`icon-180.png`,
`favicon-32.png`, `manifest.webmanifest`), gerados a partir do logo Terrazza Duomo 21 ·
Concierge. `fichas.html`, `hospitalidade.html` e `vinhos.html` continuam sem essas tags —
abrem normal, sem ícone próprio de tela de início. Depois de publicar no GitHub Pages:

- **iPhone (Safari):** abrir `index.html` → ícone de compartilhar → "Adicionar à Tela de
  Início". Vem com o nome "Guia Mestre" e a barra de status no estilo "translúcido escuro".
- **Android (Chrome):** menu ⋮ → "Adicionar à tela inicial" / "Instalar app". Usa o
  `manifest.webmanifest` (ícone 192/512, modo `standalone`, sem barra de endereço).
- Isso só funciona depois de publicado em `https://...github.io/...` — não funciona
  abrindo o arquivo local ou o link de prévia do Claude.
- Os arquivos `icon-*.png`, `favicon-*.png` e `manifest.webmanifest` continuam indo
  junto no repositório (índice de referência do `index.html`), mesmo não sendo usados
  pelas outras três páginas.

## Importante sobre os dados das fichas

As anotações ficam no armazenamento local do navegador, presas ao endereço do site.
**Anotações feitas no link do Claude não aparecem no GitHub Pages, e vice-versa.**

Antes de migrar: abrir o app no link antigo → aba Exportar → Copiar tabela (CSV) →
colar na planilha. Depois, recomeçar no endereço novo.

Outro ponto: iPhone/Safari pode apagar o armazenamento local após semanas sem uso do site.
Copiar o CSV para a planilha de tempos em tempos não é opcional.

## Estrutura

```
index.html             guia de leitura, arquivo único, sem dependências
fichas.html            app de campo, arquivo único, dados embutidos
hospitalidade.html     resumo de hospitalidade de luxo, arquivo único
vinhos.html            guia de vinhos da equipe, arquivo único, 10 idiomas
manifest.webmanifest   nome, cor e ícones para "Adicionar à Tela de Início"
icon-180.png           ícone (Apple touch icon)
icon-192.png           ícone (Android/manifest)
icon-512.png           ícone (Android/manifest, alta resolução)
favicon-32.png         favicon da aba do navegador
favicon-16.png         favicon da aba do navegador (tamanho pequeno)
README.md
```

Todos são HTML único, sem build e sem backend. Dependências externas: a fonte Archivo
(Google Fonts) em alguns dos apps; sem ela, cai para a fonte do sistema.

## Dados

Horários, preços e contatos do Guia Mestre foram verificados em 19/09/2026 e estão marcados
no guia: 🟢 verificado · 🟡 confirmar antes de usar · 🔴 checar sempre no dia.
Confirme no dia antes de mandar um hóspede a qualquer lugar.

O módulo de playbook e a página de entrevista do Guia Mestre, e o `hospitalidade.html`,
foram ampliados em 16/11/2026 com os Três Passos da Ritz-Carlton, os 5 A's de Danny Meyer
e técnicas de entrevista/negociação de uma coach de carreira do mercado americano. No mesmo
dia, o `vinhos.html` recebeu a aba Aromas, com a leitura sensorial dos 34 pratos do Manual
de Conhecimento Gastronômico da Terrazza.
