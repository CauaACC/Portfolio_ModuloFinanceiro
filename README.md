# Portfólio de Estágio — Sistema Financeiro OPCTEC

Site estático (HTML + CSS puros) para a **Avaliação Bimestral — Portfólio do Projeto de Estágio** (UniFil, 3º bimestre, entrega 14/09/2026).

## Como visualizar localmente

Basta abrir `index.html` no navegador (duplo clique). Não precisa de servidor local — todo o site é estático.

Se preferir servir via HTTP (recomendado para o vídeo iframe funcionar corretamente):

```bash
cd F:/trabalhos_facul/Estagio_2026/portfolio_estagio
python -m http.server 8000
# abra http://localhost:8000
```

## Estrutura de pastas

```
portfolio_estagio/
├── index.html                  # página única com as 7 seções obrigatórias
├── style.css
├── README.md                   # este arquivo
└── assets/
    ├── diagramas/              # 14 PNGs (classe, DER, sequência, estado, uso, implantação, workflow, cronograma)
    ├── ucspecs/                # 4 UCSpec em PDF
    ├── relatorio/              # Relatório de Estágio em PDF
    └── telas/                  # (VAZIO) coloque aqui os prints do sistema
```

## O que ainda falta preencher antes de publicar

### 1. Identificação do aluno (`index.html`, seção 7)

Procure pelos marcadores `[PREENCHER ...]` no HTML e substitua:

- Matrícula
- Curso
- Nome do(a) professor(a) orientador(a)

### 2. Prints das telas (pasta `assets/telas/`)

Nomeie exatamente assim para que o site exiba automaticamente:

| Arquivo | Tela |
|---|---|
| `01_plano_de_contas.png` | Plano de Contas |
| `02_centro_de_custo.png` | Centro de Custo |
| `03_rateios.png` | Rateios |
| `04_lancamentos.png` | Lançamentos Contábeis |
| `05_fontes_recurso.png` | Fontes de Recurso |
| `06_contabilizacao.png` | Contabilização Automática |

Os slots já estão prontos: enquanto o arquivo não existe aparece um placeholder pontilhado; assim que existir, a imagem entra automaticamente (sem precisar mexer no HTML).

### 3. Vídeo demonstrativo (máx. 5 min)

Você já tem `Crud_Funcional_Final.mp4` em `F:/trabalhos_facul/Estagio_2026/video_crud_b1/Crud_Funcional_Final/`. Passos:

1. Suba no **YouTube como "não listado"** (a exigência é "acessível ao professor sem pedir permissão").
2. Abra `index.html` e localize o bloco `<div class="video-placeholder" id="video-slot">` (seção 5.2).
3. Substitua o conteúdo pelo iframe do YouTube (exemplo já comentado no HTML):

```html
<iframe width="100%" height="480"
    src="https://www.youtube.com/embed/SEU_ID_AQUI"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen>
</iframe>
```

### 4. Relatório de Estágio atualizado

O PDF em `assets/relatorio/Relatorio_De_Estagio.pdf` foi copiado de `documentos_planejacao/Relatorio_De_Estagio_ModuloFinanceiro.pdf`. Se você atualizar o relatório antes da entrega, substitua o arquivo (mantendo o mesmo nome) — o link no site continua funcionando.

## Como publicar (opções — todas gratuitas)

Escolha uma:

### Opção A — Netlify Drop (mais rápido, sem conta)
1. Acesse https://app.netlify.com/drop
2. Arraste a pasta `portfolio_estagio` inteira.
3. Copie o link gerado (algo como `https://xxx.netlify.app`).
4. Cole no Classroom.

### Opção B — GitHub Pages (se preferir git)
1. Crie um repo público (ex.: `portfolio-estagio-contabil`).
2. Suba o conteúdo da pasta `portfolio_estagio/` na raiz.
3. Settings → Pages → Source: `main` / `/root` → Save.
4. Link: `https://SEU_USUARIO.github.io/portfolio-estagio-contabil/`.

### Opção C — Vercel
1. `vercel deploy` na pasta (após instalar CLI e logar).

## Checklist antes de entregar (14/09/2026)

- [ ] Preencher matrícula, curso e orientador no `index.html`.
- [ ] Colocar os 6 prints em `assets/telas/`.
- [ ] Fazer upload do vídeo no YouTube (não listado) e substituir o placeholder.
- [ ] Atualizar o PDF do relatório se houve mudanças recentes.
- [ ] Publicar (Netlify/GitHub Pages/Vercel).
- [ ] Testar TODOS os links do site aberto no navegador.
- [ ] Verificar que os PDFs abrem sem pedir permissão (Netlify/GH Pages já garantem isso — cuidado se hospedar no Drive/OneDrive).
- [ ] Postar o link do site na atividade do Classroom.

## Critérios da avaliação (10 pontos)

| Critério | Pontuação |
|---|---|
| Organização e estrutura do portfólio | 2,0 |
| Documentação técnica (diagramas e organização) | 2,0 |
| Clareza das informações e descrição do projeto | 2,0 |
| Evidências do funcionamento (telas e vídeo) | 2,0 |
| Qualidade geral da apresentação e publicação no prazo | 2,0 |
