# Autoescuelas Hermanos Delgado — Torrent (Valencia)

Landing page institucional e de alta conversão da **Autoescuelas Hermanos Delgado** (*Autoescuela Ángel Delgado, S.L.*), com mais de cinco décadas formando condutores em Torrent (Valencia).

- **Sede Única:** Plaza San Jaime, 6, Bajo (Izda.) · 46900 Torrent, Valencia
- **Telefones:** `961 56 70 01` · `961 56 71 09`
- **WhatsApp:** `+34 639 28 96 95` · `+34 620 16 13 41`
- **Repositório:** [github.com/ahk2001/hnosdelgado](https://github.com/ahk2001/hnosdelgado)
- **GitHub Pages:** [ahk2001.github.io/hnosdelgado](https://ahk2001.github.io/hnosdelgado/)

---

## Principais Recursos

- **Design Editorial & Alto Contraste:** Interface moderna com tipografia refinada (`Inter Tight`, `Plus Jakarta Sans`, `JetBrains Mono`), paleta oficial da autoescola e vídeo introdutório responsivo (desktop e mobile).
- **Estrutura Otimizada & Limpa:** HTML5 semântico, CSS3 moderno e Vanilla JavaScript puro, sem dependências pesadas e com ativos nomeados no padrão web (`kebab-case`).
- **SEO & Metadados:** Meta tags Open Graph, `robots.txt` (bloqueando `/docs/`) e `sitemap.xml` configurados.
- **Segurança & Cabeçalhos HTTP (`vercel.json`):**
  - `X-Content-Type-Options: nosniff`
  - `X-Frame-Options: SAMEORIGIN`
  - `X-XSS-Protection: 1; mode=block`
  - `Referrer-Policy: strict-origin-when-cross-origin`
  - `Permissions-Policy: camera=(), microphone=(), geolocation=()`
  - `Strict-Transport-Security: max-age=31536000; includeSubDomains; preload`
  - Cache imutável de 1 ano para ativos estáticos em `/assets/`.
- **CI/CD Seguro (`.github/workflows/deploy.yml`):** Pipeline automatizado para GitHub Pages com princípio de menor privilégio (`contents: read`, `pages: write`, `id-token: write`) e controle de concorrência.

---

## Estrutura de Diretórios

```text
hermanos-delgado/
├── .github/
│   └── workflows/
│       └── deploy.yml                   # Pipeline CI/CD para GitHub Pages
├── assets/                              # Mídias, vídeos e fotos otimizadas
│   ├── alumna-aprobada-vw-troc.png
│   ├── alumno-moto-honda-a2.png
│   ├── amigos-aprobados-l.png
│   ├── angel-alumno-aprobado.png
│   ├── angel-alumnos-todas-edades.png
│   ├── favicon.png
│   ├── logo.png
│   ├── monse-alumnas-aprobadas.png
│   ├── monse-alumnos-aprobados.png
│   ├── monse-nuevas-conductoras.png
│   ├── videodesktophome.mp4
│   └── videomobilehome.mp4
├── docs/                                # Documentação interna e referências
│   ├── aviso-troca-endereco-referencia.png
│   ├── dados.txt
│   └── dossie_autoescola.md
├── .gitignore                           # Exclusões de segurança e arquivos temporários
├── index.html                           # Página principal institucional
├── README.md                            # Documentação técnica do projeto
├── robots.txt                           # Regras de rastreamento para buscadores
├── sitemap.xml                          # Mapa do site
└── vercel.json                          # Headers de segurança e cache para Vercel
```

---

## Deploy

### GitHub Pages
1. No repositório `ahk2001/hnosdelgado`, acesse **Settings > Pages**.
2. Em **Build and deployment > Source**, selecione **GitHub Actions**.
3. Todo push na branch `main` publica automaticamente em `https://ahk2001.github.io/hnosdelgado/`.

### Vercel
Com `vercel.json` incluído na raiz, basta importar o repositório no painel da Vercel ou executar `vercel --prod` para publicar com todos os headers de segurança e políticas de cache ativos.
