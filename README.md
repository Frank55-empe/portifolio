# Portfólio — Professor Frank Borges

Site one-page, responsivo, com dark/light mode, animações de scroll e identidade visual própria (tema "quadro-negro + terminal": fundo grafite, acentos amarelo-giz e verde-menta).

## O que já está pronto (Fase 1)
- `index.html` — site completo, funcional, sem necessidade de build (HTML + Tailwind via CDN + JS puro)
- `404.html` — página de erro personalizada
- `robots.txt` e `sitemap.xml` — base de SEO técnico
- Seções: Hero, Sobre, Especialidades, Habilidades, Projetos, Serviços, Depoimentos (carrossel), Contato (formulário → abre seu email), Rodapé
- Dark/Light mode com preferência salva no navegador
- Botões flutuantes: WhatsApp e Voltar ao topo
- Totalmente editável: os dados de projetos, serviços, habilidades e depoimentos estão em um único bloco `<script>` no topo do arquivo — edite ali, sem precisar mexer no HTML

## Como publicar GRÁTIS

### GitHub Pages
1. Crie um repositório novo (ex: `portfolio`)
2. Suba os arquivos (`index.html`, `404.html`, `robots.txt`, `sitemap.xml`) — **use `git add/commit/push` pelo terminal, não o upload por arrastar-e-soltar do GitHub**, para evitar corrupção de arquivo (mesmo problema que já pegamos no Bolão)
3. Em Settings → Pages, selecione a branch `main` e pasta `/ (root)`
4. Seu site fica em `https://seuusuario.github.io/portfolio/`

### Domínio próprio
- Compre o domínio (ex: Registro.br para `.com.br`)
- Aponte os DNS para o GitHub Pages (registros A + CNAME, conforme documentação oficial do GitHub Pages)
- Adicione um arquivo `CNAME` com seu domínio na raiz do repositório

### Cloudflare Pages / Vercel (alternativa)
- Conecte o repositório do GitHub direto no painel da Cloudflare Pages ou da Vercel
- Build command: nenhum (site estático) — output directory: `/`
- Deploy automático a cada push

## Checklist antes de publicar
- [ ] Trocar a foto placeholder pela sua foto real
- [ ] Preencher WhatsApp, email e telefone reais no rodapé e no botão flutuante
- [ ] Ajustar `mailto:seuemail@exemplo.com` no formulário de contato
- [ ] Trocar links de GitHub/LinkedIn/YouTube (estão como `#`)
- [ ] Ajustar textos de projetos/serviços com dados finais
- [ ] Rodar o Google Lighthouse (aba DevTools do Chrome) e conferir notas de Performance/SEO/Acessibilidade

## Fase 2 — o que fica para uma etapa separada
Essas frentes exigem backend de verdade (banco de dados, autenticação, checkout) e merecem projetos próprios, do mesmo porte do Bolão ou do ViralStudio:

1. **Blog com categorias** — Supabase como CMS (tabela `posts`), reaproveitando a mesma arquitetura de tabelas do ViralStudio
2. **Loja de Cursos e eBooks** — checkout (PIX/cartão), entrega de acesso, integração de pagamento
3. **Painel administrativo sem código** — login + CRUD visual para projetos, textos, cursos e ebooks (Supabase + área autenticada em React)
4. **Versão PWA** — instalável, com ícone e splash screen, offline básico
5. **Currículo em PDF gerado automaticamente** e Portfólio em PDF

Faz sentido priorizar o **blog + painel admin simples** primeiro, já que resolve "publicar sem programar" e reaproveita a base de dados que você já projetou para o ViralStudio.
