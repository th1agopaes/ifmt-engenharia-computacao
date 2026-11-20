# 📏 Convenções

[🏠 Início](README.md)

Regras para nomes, pastas e o que vai para cada lugar. Valem para o GitHub, o Google Drive e a pasta `~/dev/faculdade` no PC.

## 🏷️ Nomes de pastas e arquivos

| # | Regra | Exemplo | Por quê |
| --- | --- | --- | --- |
| 1 | Minúsculas, sem acento, sem `ç`, sem espaço | `circuitos-eletricos-i` | No Linux, `Aula.pdf` e `aula.pdf` são arquivos diferentes; no Windows, são o mesmo (e o Git se confunde). Espaço e acento exigem aspas no zsh e viram `%20` em links |
| 2 | Hífen entre palavras; sublinhado entre blocos de informação | `lista-03_automatos-finitos.pdf` | Lê-se `[tipo-número]_[assunto]`: dá para separar os blocos de olho e por script |
| 3 | Números com 2 dígitos | `aula-07`, `01-semestre` | Sem o zero, `10` aparece antes de `2` na ordem alfabética |
| 4 | Datas no padrão ISO 8601 (`AAAA-MM-DD`) | `2026-11-19_analise-sintatica.md` | A ordem alfabética vira ordem cronológica |
| 5 | Do geral para o específico | `prova-1_2026-2.pdf` | Arquivos do mesmo tipo ficam juntos na listagem |
| 6 | Nada de `final`, `v2`, `agora-vai`, `(1)` | `relatorio-04_thevenin.docx` | Versões ficam no histórico do Git e do Drive |
| 7 | Disciplina: nome sem artigos e preposições, número em romano minúsculo (como no nome oficial); abreviação só quando já for de uso comum | `calculo-ii`, `lab-circuitos-eletricos-i`, `calculo-vetorial-ga` | Curto, legível e **igual no GitHub, no PC e no Drive** |
| 8 | `README.md` em maiúsculas; os outros `.md` em minúsculas | `README.md`, `anotacoes/2026-11-19_lr0.md` | O GitHub mostra o `README.md` da pasta sozinho |

### 📚 Vocabulário de tipos

| Prefixo | O que é | Exemplo |
| --- | --- | --- |
| `aula-NN` | Slides ou material de uma aula numerada pelo professor | `aula-07_analise-sintatica.pdf` |
| `lista-NN` | Lista de exercícios do professor | `lista-03_automatos-finitos.pdf` |
| `treino-NN` | Exercícios extras (meus ou criados com o Claude) | `treino-02_gramaticas.md` |
| `..._gabarito` | Resolução separada do enunciado | `treino-02_gramaticas_gabarito.md` |
| `prova-N` | Prova (enunciado ou resolução) | `prova-1_2026-2.pdf` |
| `trabalho-N` | Trabalho avaliativo | `trabalho-2_analisador-lexico.pdf` |
| `pre-relatorio-NN` · `relatorio-NN` | Laboratório | `relatorio-04_thevenin.docx` |
| `plano-ensino` · `cronograma` | Documentos do professor no SUAP | `plano-ensino_2026-2.pdf` |
| `resumo` | Resumo meu para prova | `resumo_p1.md` |
| `AAAA-MM-DD_tema` | Anotação de aula | `2026-11-19_analise-sintatica.md` |

### 🔄 Renomeando o que vem do AVA/Moodle

| Nome original | Nome novo |
| --- | --- |
| `Aula 7 - Análise Sintática (1).pdf` | `aula-07_analise-sintatica.pdf` |
| `Lista_3_Automatos FINAL.pdf` | `lista-03_automatos-finitos.pdf` |
| `Plano de Ensino - Compiladores 2026.2.pdf` | `plano-ensino_2026-2.pdf` |
| `Relatório Lab 4 Thévenin.docx` | `relatorio-04_thevenin.docx` |
| `P1 Circuitos.pdf` | `prova-1_2026-2.pdf` |

## 🗂️ O que vai para cada lugar

| Conteúdo | GitHub (público) | Google Drive (privado) | Projeto no Claude |
| --- | :---: | :---: | :---: |
| Plano da disciplina (`README.md`) | ✅ | | ✅ anexo |
| Minhas anotações e resumos | ✅ | | quando ajudar |
| Exercícios e treinos resolvidos por mim | ✅ | | |
| Slides, listas e apostilas do professor | ❌ direitos autorais | ✅ | ✅ só os da unidade atual |
| Livros em PDF | ❌ | só os de acesso aberto | |
| Enunciado de prova ou trabalho | ❌ | ✅ | |
| Minha resolução de prova ou trabalho | ⏳ só depois da nota, e se o professor não reaproveitar | ✅ | |
| Trabalho em grupo | ⏳ só com o ok do grupo | ✅ | |
| Fotos do quadro, scans, áudios | ❌ arquivo pesado | ✅ | |
| Comprovantes (certificados, estágio) | ❌ | ✅ | |
| Notas, histórico e documentos pessoais | ❌ | ✅ | |

O `.gitignore` deste repositório bloqueia PDF, Office, imagens de câmera, vídeos e compactados, para nada disso entrar por engano. Arquivo **meu** que precise mesmo ficar aqui (ex.: relatório que eu escrevi) entra com `git add -f arquivo`, e o motivo vai na mensagem do commit.

## 📁 Pasta de cada disciplina

```text
05-semestre/compiladores/
├── README.md              plano: ementa, conteúdo, bibliografia, avaliações e links
├── anotacoes/             2026-09-15_analise-lexica.md
├── exercicios/
│   ├── lista-01/          q01.java, q02.java... (enunciado no topo, em comentário)
│   ├── treino-01_automatos.md
│   └── treino-01_automatos_gabarito.md
├── projeto/               só projeto pequeno desta disciplina
└── instrucoes-claude.md   instruções do Projeto da disciplina no Claude
```

A pasta só aparece quando ganha o primeiro arquivo, porque o Git não guarda pasta vazia.

### Projeto: aqui ou em repositório próprio?

Mesma regra do `jornada-dev`:

- **`projeto/` aqui dentro:** pequeno, só desta disciplina, sem CI nem deploy.
- **Repositório próprio:** serve a mais de uma disciplina, tem CI, deploy ou releases, é em grupo ou vai continuar depois como portfólio. O `README.md` da disciplina ganha o link. Exemplos: `columbinamath` (Engenharia de Software, Extensão I e Programação Web) e `compilador-colombe`.
- **No PC**, o clone pode ficar dentro da pasta da disciplina (como já está hoje), desde que o caminho esteja no `.gitignore` deste repositório. Sem isso, o Git trata o clone como "repositório dentro de repositório" e avisa no `git add`.

## ➗ Matemática e física no Markdown

O GitHub desenha fórmulas em LaTeX:

```markdown
A derivada de $f(x) = x^2$ é $f'(x) = 2x$.

$$
\int_0^1 x^2 \, dx = \frac{1}{3}
$$
```

Diagramas de fluxo, estados e árvores podem ser feitos em Mermaid (bloco `mermaid`). Circuitos: desenho em texto ou imagem exportada do simulador (PNG ou SVG pequeno, feito por mim).

## 📝 Commits

[Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/), assinados, com o **escopo = pasta da disciplina**:

| Tipo | Quando | Exemplo |
| --- | --- | --- |
| `docs` | Anotações, resumos, README | `docs(compiladores): anotações da aula de análise sintática` |
| `feat` | Exercício ou código novo | `feat(calculo-numerico): lista 2 com o método de Newton` |
| `fix` | Correção | `fix(fisica-i): unidade errada no exercício 4 da lista 3` |
| `chore` | Estrutura do repositório (escopo `repo`) | `chore(repo): pastas do 6º semestre` |

**Fluxo:** anotações e exercícios vão em commits atômicos direto na `main`, porque é um caderno e PR por aula seria atrito. Mudanças de estrutura (templates, README da raiz, CI) vão por branch + PR + squash, como nos outros repositórios.

## ☁️ Google Drive

A pasta `Documentos/IFMT` do Windows é sincronizada pelo Google Drive para computador (no site e no app do Drive, ela fica em **Computadores**). Ela tem a **mesma árvore e os mesmos nomes** deste repositório, para os arquivos que não vão para o GitHub:

```text
Documentos/IFMT/
├── documentos/                 PPC, regulamento didático, histórico, matrícula
├── atividades-complementares/  um comprovante por atividade (AAAA-MM-DD_tipo_evento.pdf)
├── estagio/
└── 05-semestre/
    └── compiladores/
        ├── plano-ensino_2026-2.pdf   plano de ensino do SUAP, na raiz da disciplina
        ├── aulas/              slides e apostilas (aula-NN_tema.pdf)
        ├── listas/             listas e resoluções (lista-NN_tema.pdf)
        ├── provas/             provas (prova-N_AAAA-P.pdf)
        └── trabalhos/          enunciados e o que eu entreguei (trabalho-N_tema.pdf)
```

> [!WARNING]
> O repositório Git fica **só no WSL** (`~/dev/faculdade`), nunca dentro de uma pasta sincronizada. O Drive copia os arquivos internos da `.git` um por um, fora de ordem, e isso pode gerar conflitos e corromper o repositório. Cada lugar guarda um tipo de coisa: o Git guarda o texto (com o GitHub de backup) e o Drive guarda os binários.

Quem visitar o GitHub não consegue abrir nada do Drive: as pastas continuam só suas.
