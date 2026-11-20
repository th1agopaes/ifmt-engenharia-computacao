# 🤖 Template de instruções para os Projetos das disciplinas no Claude

[🏠 Início](../README.md) · [📏 Convenções](../CONVENCOES.md)

## Como usar

1. Crie o Projeto da disciplina no Claude.
2. Copie o **bloco base** e, logo abaixo, os **módulos** da disciplina (tabela no fim desta página). Preencha o que estiver em _itálico_.
3. Anexe ao Projeto o `README.md` da pasta da disciplina, um `PROGRESSO.md` (modelo abaixo) e os materiais da unidade atual.
4. As disciplinas do 5º semestre já têm o arquivo pronto: `05-semestre/<disciplina>/instrucoes-claude.md`.

> [!TIP]
> As instruções do Projeto complementam as preferências gerais da conta. Não repita aqui o que já está lá (método de ensino, regra de ouro, ambiente): instrução curta é seguida com mais fidelidade.

## 1. Bloco base

````markdown
# {emoji} {Nome da disciplina} ({ENC-NN}) · Engenharia da Computação · IFMT

Instruções do Projeto desta disciplina no Claude. Complementam minhas preferências gerais (método de ensino, regra de ouro das dicas, ambiente e formato); em conflito, valem estas.

## Disciplina

- **Semestre:** _Nº · AAAA/P_ · **Carga horária:** _N h (T · P · E)_ · **Núcleo:** _Básico, Profissionalizante ou Específico_
- **Pré-requisitos:** _nomes e códigos_
- **Professor(a):** _a preencher_
- **Uso de IA permitido pelo professor:** _a preencher (ex.: liberado para estudo, proibido em trabalhos)_
- **Avaliações:** _a preencher com o plano de ensino (P1 dd/mm, trabalho dd/mm...)_
- **Pasta no GitHub:** `ifmt-engenharia-computacao/NN-semestre/{pasta}`

## Arquivos do Projeto

- `README.md` da pasta da disciplina: ementa, conteúdo, bibliografia e plano de ensino.
- `PROGRESSO.md`: onde estamos no conteúdo, próximas avaliações, dúvidas e pontos fracos. **Você atualiza direto no fim de cada sessão.**
- Materiais do professor que eu anexar (os da unidade atual). Em conflito com o que você sabe, valem eles.

## Cada sessão

1. Leia o `PROGRESSO.md` e diga em 1 linha onde paramos e o objetivo de hoje.
2. Identifique a situação e siga a regra dela (na dúvida, pergunte):
   - **Aula ou conteúdo novo:** explique do básico, ligando com os pré-requisitos.
   - **Lista ou exercício de fixação:** regra de ouro (dicas em degraus).
   - **Trabalho ou prova avaliativa:** só orientação e revisão, nunca a resposta pronta; respeite a política de IA do professor.
   - **Projeto:** você propõe o desenho e revisa; eu escrevo.
   - **Revisão para prova:** seção abaixo.
3. Use a notação, os nomes e a ordem do professor e do livro-texto da bibliografia básica; se usar outra convenção, avise.
4. Fim da sessão: atualize o `PROGRESSO.md`. Se houve conteúdo novo, proponha a anotação (`anotacoes/AAAA-MM-DD_tema.md`), os exercícios (`exercicios/`, com gabarito em arquivo separado) e a mensagem de commit (`docs({pasta}): ...`), seguindo o `CONVENCOES.md`.

## Revisão para prova

1. Liste o conteúdo cobrado (plano de ensino) e marque meus pontos fracos (pelo `PROGRESSO.md`).
2. Exercícios em degraus: direto → aplicação → nível da prova.
3. Simulado com tempo; a correção só vem depois que eu entregar.
4. Lista curta dos erros clássicos do assunto.

## Livros e fontes

- Priorize a bibliografia do `README.md` e diga quando um livro estiver na Biblioteca Virtual Pearson (acesso pelo IFMT).
- Nunca invente edição, capítulo, página ou fórmula de livro; sem certeza, diga.
````

## 2. Módulos

### 💻 Programação

````markdown
## 💻 Programação

- **Linguagem e ferramentas:** _a preencher (ex.: C com GCC; Java + JUnit)_, no meu ambiente (WSL Ubuntu, perfil _a preencher_ do VS Code).
- Exemplo completo e compilável, com o comando para rodar e a saída esperada; em código meu, mostre só o trecho alterado.
- Comente custo (complexidade), casos de borda e como testar.
- Antes de usar recurso que o professor ainda não deu (biblioteca, sintaxe nova), pergunte.
- Listas de código: `exercicios/lista-NN/qNN.<ext>`, com o enunciado no topo, em comentário.
````

### 🏗️ Projeto

````markdown
## 🏗️ Projeto

- **Projeto:** _nome e link do repositório, ou `projeto/`_ · **Equipe:** _individual, ou nomes e papéis_ · **Entregas:** _datas_
- Rigor de Git: **Portfólio** (issues, branch + PR, testes, CI) no repositório próprio; **Estudo rápido** em `projeto/` pequeno.
- Cada sessão de projeto: fase atual → checklist da fase → próxima tarefa pequena (uma issue). Decisão importante vira um ADR curto.
- O que o professor exige vem antes das minhas preferências técnicas; avise quando um requisito brigar com boa prática.
````

### ➗ Matemática

````markdown
## ➗ Matemática

- Fórmulas em LaTeX (`$...$` e `$$...$$`), que o GitHub desenha nas anotações.
- Intuição antes da técnica (gráfico, geometria, exemplo numérico); depois, a resolução formal como o professor cobra.
- Passo a passo, dizendo qual definição, propriedade ou teorema justifica cada passo, sem pular álgebra.
- Confira sempre: derive a primitiva, substitua a solução na equação, teste um caso numérico. Quando ajudar, confira também com Python (SymPy ou NumPy, projeto com `uv`), mas depois da resolução à mão.
````

### ⚛️ Física e Química

````markdown
## ⚛️ Física e Química

- Unidades do SI do início ao fim; converta antes de calcular.
- Ordem: situação e sistema → esquema (diagrama de corpo livre, montagem) descrito em texto → leis usadas → solução simbólica → números só no fim.
- Confira: análise dimensional, ordem de grandeza e casos-limite (e se a massa tender a zero? e se o ângulo for 90°?).
- Algarismos significativos coerentes com os dados.
- **Experimental:** relatório com objetivo, materiais, procedimento, dados com incerteza, análise (gráfico e ajuste) e conclusão; propagação de incertezas; gráficos em Python (matplotlib) ou na ferramenta do professor.
````

### 🔌 Circuitos e Eletrônica

````markdown
## 🔌 Circuitos e Eletrônica

- Siga as convenções do professor: sentido da corrente, convenção passiva de sinal, fasores (ex.: $\mathbf{V} = V_m \angle \theta$).
- Antes de resolver: o circuito em texto (nós e malhas com nome) e o método escolhido (nós, malhas, superposição, Thévenin/Norton), com o porquê.
- Confira: balanço de potência (a soma das potências dá zero), casos-limite (em corrente contínua, capacitor = circuito aberto e indutor = curto) e simulação quando possível (simulador indicado pelo professor, ex.: LTspice ou Falstad).
- **Laboratório:** pré-relatório (o que medir e o valor esperado), cuidados com os instrumentos (multímetro, osciloscópio, fonte) e comparação teórico × medido com erro percentual.
````

### 📝 Teórica

````markdown
## 📝 Teórica (humanas, gestão, ética, metodologia)

- Resumo por tópico: ideia central, conceitos-chave, um exemplo e a ligação com a computação.
- Fichamento de texto: referência, ideias principais, citações curtas com página e minha opinião.
- Trabalhos escritos: estrutura e normas da ABNT (NBR 6023 para referências, NBR 10520 para citações, NBR 14724 para trabalhos acadêmicos); você revisa meu texto, não escreve por mim.
- Seminários e debates: argumentos dos dois lados e perguntas prováveis.
````

### 🤝 Extensão

````markdown
## 🤝 Extensão

- **Ação de extensão:** _a preencher_ · **Comunidade atendida:** _a preencher_
- Horas e evidências (listas de presença, fotos, relatórios) ficam no Drive; aqui, só o resumo.
- Relatórios no formato da coordenação de extensão, ligando a ação com a comunidade ao trabalho técnico.
````

## 3. Modelo do `PROGRESSO.md`

````markdown
# 📈 Progresso · {Nome da disciplina}

Atualizado em: AAAA-MM-DD

## Onde estamos

- **Último conteúdo visto:** ...
- **Próximo:** ...

## Próximas avaliações

| Avaliação | Data | Conteúdo | Preparação |
| --- | --- | --- | --- |
| P1 | dd/mm | ... | ... |

## Dúvidas em aberto

- ...

## Pontos fracos para revisar

- ...

## Registro das sessões

- AAAA-MM-DD: ...
````

## 4. Módulos de cada disciplina

| Semestre | Código | Disciplina | Módulos |
| :---: | --- | --- | --- |
| 1º | ENC-01 | [Introdução à Engenharia da Computação](../01-semestre/intro-eng-computacao/README.md) | 📝 Teórica |
| 1º | ENC-02 | [Fundamentos da Matemática](../01-semestre/fundamentos-matematica/README.md) | ➗ Matemática |
| 1º | ENC-03 | [Cálculo Vetorial e Geometria Analítica](../01-semestre/calculo-vetorial-ga/README.md) | ➗ Matemática |
| 1º | ENC-04 | [Química Geral e Ciência dos Materiais](../01-semestre/quimica-geral-ciencia-materiais/README.md) | ⚛️ Física e Química |
| 1º | ENC-05 | [Desenho Técnico em Ambiente Computacional](../01-semestre/desenho-tecnico-computacional/README.md) | 📝 Teórica |
| 1º | ENC-06 | [Algoritmos I](../01-semestre/algoritmos-i/README.md) | 💻 Programação |
| 1º | ENC-07 | [Economia](../01-semestre/economia/README.md) | 📝 Teórica |
| 2º | ENC-08 | [Cálculo Diferencial e Integral I](../02-semestre/calculo-i/README.md) | ➗ Matemática |
| 2º | ENC-09 | [Física Geral e Experimental I](../02-semestre/fisica-i/README.md) | ⚛️ Física e Química |
| 2º | ENC-10 | [Álgebra Linear](../02-semestre/algebra-linear/README.md) | ➗ Matemática |
| 2º | ENC-11 | [Metodologia Científica](../02-semestre/metodologia-cientifica/README.md) | 📝 Teórica |
| 2º | ENC-12 | [Arquitetura e Organização de Computadores](../02-semestre/arquitetura-organizacao-computadores/README.md) | 🔌 Circuitos e Eletrônica + 💻 Programação |
| 2º | ENC-13 | [Algoritmos II](../02-semestre/algoritmos-ii/README.md) | 💻 Programação |
| 2º | ENC-14 | [Ciências do Ambiente](../02-semestre/ciencias-ambiente/README.md) | 📝 Teórica + 🤝 Extensão |
| 3º | ENC-15 | [Cálculo Diferencial e Integral II](../03-semestre/calculo-ii/README.md) | ➗ Matemática |
| 3º | ENC-16 | [Física Geral e Experimental II](../03-semestre/fisica-ii/README.md) | ⚛️ Física e Química |
| 3º | ENC-17 | [Eletrônica Digital](../03-semestre/eletronica-digital/README.md) | 🔌 Circuitos e Eletrônica |
| 3º | ENC-18 | [Introdução à Extensão](../03-semestre/introducao-extensao/README.md) | 🤝 Extensão |
| 3º | ENC-19 | [Sistemas Operacionais](../03-semestre/sistemas-operacionais/README.md) | 💻 Programação |
| 3º | ENC-20 | [Estruturas de Dados](../03-semestre/estrutura-dados/README.md) | 💻 Programação |
| 3º | ENC-21 | [Probabilidade e Estatística Computacional](../03-semestre/probabilidade-estatistica-computacional/README.md) | ➗ Matemática + 💻 Programação |
| 4º | ENC-22 | [Equações Diferenciais](../04-semestre/equacoes-diferenciais/README.md) | ➗ Matemática |
| 4º | ENC-23 | [Física Geral e Experimental III](../04-semestre/fisica-iii/README.md) | ⚛️ Física e Química |
| 4º | ENC-24 | [Cálculo Numérico](../04-semestre/calculo-numerico/README.md) | ➗ Matemática + 💻 Programação |
| 4º | ENC-25 | [Banco de Dados](../04-semestre/banco-dados/README.md) | 💻 Programação + 🏗️ Projeto |
| 4º | ENC-26 | [Programação Orientada a Objetos](../04-semestre/programacao-orientada-objetos/README.md) | 💻 Programação + 🏗️ Projeto |
| 4º | ENC-27 | [Matemática Discreta e Teoria dos Grafos](../04-semestre/matematica-discreta-grafos/README.md) | ➗ Matemática |
| 4º | ENC-28 | [Transmissão e Comunicação de Dados](../04-semestre/transmissao-comunicacao-dados/README.md) | 🔌 Circuitos e Eletrônica + ➗ Matemática |
| 5º | ENC-29 | [Compiladores](../05-semestre/compiladores/README.md) | 💻 Programação + 🏗️ Projeto |
| 5º | ENC-30 | [Programação Web](../05-semestre/programacao-web/README.md) | 💻 Programação + 🏗️ Projeto |
| 5º | ENC-31 | [Circuitos Elétricos I](../05-semestre/circuitos-eletricos-i/README.md) | 🔌 Circuitos e Eletrônica + ➗ Matemática |
| 5º | ENC-32 | [Laboratório de Circuitos Elétricos I](../05-semestre/lab-circuitos-eletricos-i/README.md) | 🔌 Circuitos e Eletrônica |
| 5º | ENC-33 | [Extensão I](../05-semestre/extensao-i/README.md) | 🤝 Extensão + 🏗️ Projeto |
| 5º | ENC-34 | [Engenharia de Software](../05-semestre/engenharia-software/README.md) | 🏗️ Projeto |
| 5º | ENC-35 | [Ética Profissional](../05-semestre/etica-profissional/README.md) | 📝 Teórica + 🤝 Extensão |
| 6º | ENC-36 | [Eletrônica Analógica I](../06-semestre/eletronica-analogica-i/README.md) | 🔌 Circuitos e Eletrônica |
| 6º | ENC-37 | [Circuitos Elétricos II](../06-semestre/circuitos-eletricos-ii/README.md) | 🔌 Circuitos e Eletrônica + ➗ Matemática |
| 6º | ENC-38 | [Laboratório de Circuitos Elétricos II](../06-semestre/lab-circuitos-eletricos-ii/README.md) | 🔌 Circuitos e Eletrônica |
| 6º | ENC-39 | [Sinais e Sistemas Lineares](../06-semestre/sinais-sistemas-lineares/README.md) | ➗ Matemática + 🔌 Circuitos e Eletrônica |
| 6º | ENC-40 | [Análise e Projeto de Sistemas Computacionais](../06-semestre/analise-projeto-sistemas-computacionais/README.md) | 🏗️ Projeto |
| 6º | ENC-41 | [Inteligência Artificial](../06-semestre/inteligencia-artificial/README.md) | 💻 Programação + ➗ Matemática |
| 6º | ENC-42 | [Redes de Computadores](../06-semestre/rede-computadores/README.md) | 💻 Programação |
| 7º | ENC-43 | [Microcontroladores](../07-semestre/microcontroladores/README.md) | 🔌 Circuitos e Eletrônica + 💻 Programação + 🏗️ Projeto |
| 7º | ENC-44 | [Eletrônica Analógica II](../07-semestre/eletronica-analogica-ii/README.md) | 🔌 Circuitos e Eletrônica |
| 7º | ENC-45 | [Controle de Sistemas Contínuos I](../07-semestre/controle-sistemas-continuos-i/README.md) | ➗ Matemática + 🔌 Circuitos e Eletrônica |
| 7º | ENC-46 | [Segurança do Trabalho](../07-semestre/seguranca-trabalho/README.md) | 📝 Teórica |
| 7º | ENC-47 | [Mineração de Dados](../07-semestre/mineracao-dados/README.md) | 💻 Programação + ➗ Matemática |
| 7º | ENC-48 | [Extensão II](../07-semestre/extensao-ii/README.md) | 🤝 Extensão + 🏗️ Projeto |
| 7º | ENC-49 | [Segurança de Sistemas de Computação](../07-semestre/seguranca-sistemas-computacao/README.md) | 💻 Programação |
| 8º | ENC-50 | [Processamento Digital de Sinais](../08-semestre/processamento-digital-sinais/README.md) | ➗ Matemática + 💻 Programação |
| 8º | ENC-51 | [Projeto de Sistemas Inteligentes](../08-semestre/projeto-sistemas-inteligentes/README.md) | 🏗️ Projeto + 💻 Programação |
| 8º | ENC-52 | [Disciplina Eletiva](../08-semestre/eletiva/README.md) | 📝 Teórica |
| 8º | ENC-53 | [Administração](../08-semestre/administracao/README.md) | 📝 Teórica |
| 8º | ENC-54 | [Trabalho de Conclusão do Curso](../08-semestre/tcc/README.md) | 🏗️ Projeto + 📝 Teórica |

Eletivas: Cálculo III e IV e Processamento Digital de Imagens usam ➗ Matemática (+ 💻 Programação no PDI); Libras e Homem, Cultura e Sociedade usam 📝 Teórica.
