# Milano Concierge

Duas ferramentas pessoais para a transição de chef de sala para concierge de hotel em Milão.

**Guia Mestre** — `index.html`
Página de leitura com 33 módulos: geografia, história, museus, gastronomia, transporte,
perfis culturais por nacionalidade, casos difíceis, hotéis 5★ e diretório de contatos.
Tem sumário lateral, busca e modo claro/escuro. Não guarda estado.

**Fichas** — `fichas.html`
App de campo. 119 lugares organizados em 12 semanas de visitas. Em cada ficha:
nota, faixa de preço, perfil, ocasião, ruído, tamanho de grupo, serve com chuva,
LGBTQIA+ friendly, acessível, pontos fracos e três campos de texto.
Aba de consulta que devolve A/B/C a partir do perfil do hóspede.

## Publicar no GitHub Pages

1. Criar um repositório (sugestão: `milano-concierge`).
2. Subir `index.html`, `fichas.html` e este README.
3. Settings → Pages → Source: `Deploy from a branch` → branch `main`, pasta `/ (root)`.
4. Aguardar um minuto. O endereço fica:
   - Guia: `https://<usuario>.github.io/milano-concierge/`
   - Fichas: `https://<usuario>.github.io/milano-concierge/fichas.html`

## Importante sobre os dados das fichas

As anotações ficam no armazenamento local do navegador, presas ao endereço do site.
**Anotações feitas no link do Claude não aparecem no GitHub Pages, e vice-versa.**

Antes de migrar: abrir o app no link antigo → aba Exportar → Copiar tabela (CSV) →
colar na planilha. Depois, recomeçar no endereço novo.

Outro ponto: iPhone/Safari pode apagar o armazenamento local após semanas sem uso do site.
Copiar o CSV para a planilha de tempos em tempos não é opcional.

## Estrutura

```
index.html     guia de leitura, arquivo único, sem dependências
fichas.html    app de campo, arquivo único, dados embutidos
README.md
```

Ambos são HTML único, sem build e sem backend. A única dependência externa é a fonte
Archivo (Google Fonts) no app; sem ela, cai para a fonte do sistema.

## Dados

Horários, preços e contatos foram verificados em 19/09/2026 e estão marcados no guia:
🟢 verificado · 🟡 confirmar antes de usar · 🔴 checar sempre no dia.
Confirme no dia antes de mandar um hóspede a qualquer lugar.
