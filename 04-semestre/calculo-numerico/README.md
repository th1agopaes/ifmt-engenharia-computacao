# ➗ Cálculo Numérico

![código: ENC-24](https://img.shields.io/badge/c%C3%B3digo-ENC--24-cba6f7?style=flat-square) ![semestre: 4º · 2026/1](https://img.shields.io/badge/semestre-4%C2%BA_%C2%B7_2026%2F1-89b4fa?style=flat-square) ![carga horária: 68 h](https://img.shields.io/badge/carga_hor%C3%A1ria-68_h-fab387?style=flat-square) ![status: concluída](https://img.shields.io/badge/status-conclu%C3%ADda-a6e3a1?style=flat-square)

[🏠 Início](../../README.md) · [📅 4º semestre](../README.md) · [📏 Convenções](../../CONVENCOES.md)

| | |
| --- | --- |
| **Código** | ENC-24 |
| **Semestre** | 4º · 2026/1 |
| **Carga horária** | 68 h (51 teórica · 17 prática) |
| **Núcleo** | Profissionalizante |
| **Pré-requisitos** | [Cálculo Diferencial e Integral I](../../02-semestre/calculo-i/README.md) |
| **Libera** | — |
| **Professor(a)** | _a preencher_ |

## 📌 Ementa

> Introdução. Zeros de funções. Interpolação. Sistemas de equações lineares. Integração numérica. Equações diferenciais ordinárias.

## 🗺️ Conteúdo programático

- Introdução
  - Fundamentação
  - Motivação sobre o uso dos Métodos Numéricos
- Sistema de Numeração
  - Sistemas de Numeração
  - Conversão de base numérica
  - Erros de representação numérica, sistemas de ponto flutuante (SPF)
  - Erro relativo e erro absoluto
  - Erros de arredondamento, erros de truncamento e propagação de erros
  - Erros de truncamento e série de Taylor
- Zero Funções
  - Método da Bissecção
  - Método da Falsa Posição. Armadilhas do método da Falsa
  - Posição e, erro relativo percentual do método
  - Métodos abertos. Iteração de Ponto Fixo Simples. Método de Newton-Raphson
  - Análise do erro do Método de Newton-Raphson
  - Método da Secante
  - Diferenças entre o Método da Secante e da Falsa Posição
  - Método da Secante Modificado
  - Cálculo de raízes múltiplas
  - Método de Newton-Raphson Modificado para raízes múltiplas
- Sistemas de Equaçòes Algébricas Lineares
  - Fundamentos Matemáticos e notação matricial
  - Eliminação de Gauss
  - Método Gráfico
  - Determinantes e a Regra de Cramer
  - Eliminação de Variáveis. Eliminação de Gauss Ingênua. Eliminação Progressiva e Substituição Regressiva
  - Armadilhas da Eliminação de Gauss
  - Efeito de Escala no Determinante. Mudança de escala
  - Cálculo do determinante usando a Eliminação de Gauss
  - Técnicas para melhorar as soluções
  - Métodos de Gauss-Jordan e Decomposição LU
  - Sistemas Tridiagonais. Algoritmo de Thomas
  - Gauss-Seidel e Método SOR
- Interpolação
  - Introdução
  - Polinômios Interpoladores por Diferenças Divididas de Newton
  - Forma geral dos polinômios interpoladores de Newton
  - Erros nos polinômios Interpoladores de Newton
  - Polinômios Interpoladores de Lagrange
  - Interpolação por Splines
- Integração Numérica
  - Introdução
  - Fórmulas de Integração de Newton-Cotes
  - A Regra do Trapézio. Erro na Regra do Trapézio
  - Aplicação Múltipla na Regra do Trapézio
  - As regras de Simpson. A Regra de 1/3 de Simpson. Aplicações Múltiplas da Regra de 1/3 de Simpson
  - A regra de 3/8 de Simpson
- Equações Diferenciais Ordinárias
  - Introdução
  - Método de Euler
  - Métodos de Runge-Kutta

## 📚 Bibliografia

### Básica

- BARROSO, L. C. et al. Cálculo Numérico (com Aplicações), 2a ed., São Paulo: Harbra, 1987.
- RUGGIERO, M.A.G.; LOPES, V.L. Cálculo numérico: aspectos teóricos e computacionais. 2a ed., São Paulo: Makron Books, 1997.
- STEVEN C. CHAPRA E RAYMOND P. CANALE. Métodos Numéricos para Engenharia, 5ª ed., Editora McGraw Hill, 2008.

### Complementar

- ARENALES, S. H. de V.; DAREZZO, A. Cálculo Numérico - com apoio de software, 2ª ed., CENGAGE Learning, 2015.
- BURDEN, L. B.; Douglas F. J. Análise Numérica. CENGAGE Learning. 2ª edição 2008.
- BURIAN, R.; LIMA, A. C. de; HETEM JUNIOR, A. Fundamentos de Informática: Cálculo Numérico. Rio de Janeiro RJ: LTC, 2016.
- PIRES, A. de Abreu. Cálculo Numérico - Práticas com algoritmos e planilhas, 1ª ed., Editora Atlas, 2015.
- SPERANDIO, D. et al., Cálculo Numérico, 2ª ed., Editora Pearson, 2014.

> 📖 Marque com 📖 os livros que estiverem na Biblioteca Virtual Pearson (acesso pelo IFMT).

## 📂 Nesta pasta

| Pasta | O que guarda |
| --- | --- |
| `anotacoes/` | Minhas anotações, uma por aula ou tópico (`AAAA-MM-DD_tema.md`) |
| `exercicios/` | Listas resolvidas e treinos (`lista-NN/`, `treino-NN_tema.md` + gabarito separado) |
| `projeto/` | Só para projeto pequeno desta disciplina; projeto grande ganha repositório próprio e um link aqui |

_As pastas aparecem quando ganham o primeiro arquivo (o Git não guarda pasta vazia)._

## 🔁 Revisão

- [ ] Resumo dos tópicos da ementa em `anotacoes/`
- [ ] Exercícios de revisão em `exercicios/`
- [ ] Trabalhos ou projeto da época (link ou `projeto/`)

## 🔗 Links

- 📁 Materiais do professor: `Documentos/IFMT/04-semestre/calculo-numerico/` no PC, sincronizada com o Google Drive (em **Computadores**)
- 🎓 AVA / Moodle: _colar o link_
