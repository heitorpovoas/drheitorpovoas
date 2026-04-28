# drheitorpovoas.com.br

Site institucional do Dr. Heitor Póvoas — cirurgião bariátrico e intensivista em Salvador.

Construído em **Jekyll**, hospedado gratuitamente no **GitHub Pages**, com domínio customizado `drheitorpovoas.com.br`.

---

## Estrutura do projeto

```
.
├── _config.yml              # configuração principal (dados do médico, URL, plugins)
├── _layouts/                # templates HTML (default, home, post, page)
├── _includes/               # partials (header, footer)
├── _posts/                  # artigos do blog em markdown
├── pages/                   # páginas estáticas (sobre, áreas, blog index)
├── assets/
│   ├── css/main.css         # folha de estilo principal
│   └── img/                 # imagens (foto do médico, logo, favicon)
├── index.html               # home
├── CNAME                    # domínio customizado para GitHub Pages
└── Gemfile                  # dependências Jekyll (preview local)
```

---

## Deploy passo a passo

### 1. Criar repositório no GitHub

- Acesse github.com → New repository
- Nome do repo: `drheitorpovoas` (ou `heitorpovoas.github.io` para uso direto sem domínio customizado)
- Visibilidade: **público** (necessário para GitHub Pages no plano gratuito)
- Não inicializar com README (vamos subir o nosso)
- Criar repositório

### 2. Subir os arquivos via GitHub Desktop

- Abra GitHub Desktop
- File → Clone repository → selecione `drheitorpovoas`
- Salve em pasta local (ex: `~/Documentos/drheitorpovoas`)
- **Cole todos os arquivos deste pacote** dentro da pasta clonada
- Volte ao GitHub Desktop — vai detectar todos os arquivos como modificações
- Commit message: "Initial site setup"
- Commit to main → Push origin

### 3. Ativar GitHub Pages

- No site do repositório (github.com/seuusuario/drheitorpovoas)
- Settings → Pages
- Source: **Deploy from a branch**
- Branch: **main** / **/ (root)**
- Save

Em 2 a 5 minutos o site estará no ar em `https://seuusuario.github.io/drheitorpovoas/`.

### 4. Configurar DNS no Registro.br

- Entre em registro.br com login da sua conta
- Acesse o domínio drheitorpovoas.com.br
- Editar zona DNS

**Adicione 4 registros A apontando para os IPs do GitHub Pages:**

```
@   A   185.199.108.153
@   A   185.199.109.153
@   A   185.199.110.153
@   A   185.199.111.153
```

**E 1 registro CNAME para o subdomínio www:**

```
www   CNAME   seuusuario.github.io.
```

(Ponto final é importante.)

Salvar. **Propagação: de 1 a 24 horas.**

### 5. Configurar domínio customizado no GitHub

- No repo → Settings → Pages
- Custom domain: `drheitorpovoas.com.br`
- Save
- Aguardar verificação de DNS (alguns minutos a algumas horas)
- Marcar checkbox **Enforce HTTPS** assim que estiver disponível (geralmente leva uma hora após DNS validar)

Pronto. Site no ar em `https://drheitorpovoas.com.br`.

---

## Como adicionar novo artigo no blog

### Pelo computador (recomendado)

1. Crie arquivo na pasta `_posts/`
2. Nome do arquivo: `AAAA-MM-DD-titulo-do-artigo.md` (data no início é obrigatória)
3. Front matter no início do arquivo:

```yaml
---
layout: post
title: "Título do artigo"
description: "Meta description para SEO (até 160 caracteres)"
date: 2026-05-15
category: cirurgia-bariatrica
tags: [cirurgia bariátrica, sleeve, recidiva]
permalink: /url-amigavel-do-artigo/
---
```

4. Escreva o artigo abaixo do front matter, em markdown
5. Commit + push via GitHub Desktop
6. Em 2 a 3 minutos, artigo no ar

### Pelo celular ou direto no GitHub.com

- Acessar github.com/seuusuario/drheitorpovoas
- Navegar até `_posts/`
- Add file → Create new file
- Nomear seguindo padrão `AAAA-MM-DD-titulo.md`
- Colar conteúdo
- Commit changes

---

## Como editar conteúdo existente

- Páginas estáticas (sobre, áreas): editar arquivos em `pages/`
- Identidade visual e cores: editar `assets/css/main.css` (variáveis CSS no topo)
- Dados do médico (CRM, RQE, endereço, WhatsApp): editar `_config.yml`
- Após qualquer edição: commit + push

---

## Imagens necessárias

Salvar em `assets/img/`:

- `dr-heitor-hero.jpg` — foto profissional para hero da home (formato vertical ou recortada para portrait)
- `favicon.png` — ícone do site (256×256px, fundo navy, monograma "HP" em dourado)
- (Opcional) `logo-baros.png` — logo da Clínica Baros, se quiser usar em algum lugar

---

## Preview local (opcional, para testar antes de publicar)

Requer Ruby instalado.

```bash
cd ~/Documentos/drheitorpovoas
bundle install
bundle exec jekyll serve
```

Abrir http://localhost:4000 no navegador.

---

## Próximas tarefas (depois do lançamento inicial)

- [ ] Cadastrar site no **Google Search Console** (essencial para SEO)
- [ ] Cadastrar site no **Google My Business** com endereço completo
- [ ] Adicionar **Google Analytics 4** (criar tag e colar no `_layouts/default.html`)
- [ ] Criar perfil no **Doctoralia** linkando para este site
- [ ] Solicitar reviews de pacientes em Google e Doctoralia
- [ ] Adicionar imagens de boa resolução nas páginas de áreas
- [ ] Publicar artigo 4 (GLP-1 + bariátrica) ~3 semanas após lançamento

---

## Suporte

Site mantido pelo próprio Dr. Heitor Póvoas. Estrutura técnica documentada acima.
