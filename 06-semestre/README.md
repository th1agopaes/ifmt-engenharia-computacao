# 📅 6º semestre · 2027/1 ⏳

![status: futura](https://img.shields.io/badge/status-futura-9399b2?style=flat-square) ![carga horária: 442 h](https://img.shields.io/badge/carga_hor%C3%A1ria-442_h-fab387?style=flat-square) ![disciplinas: 7](https://img.shields.io/badge/disciplinas-7-cba6f7?style=flat-square)

[🏠 Início](../README.md) · [← 5º semestre](../05-semestre/README.md) · [7º semestre →](../07-semestre/README.md)

| Status | Código | Disciplina | Carga horária | Núcleo |
| :---: | --- | --- | --- | --- |
| ⏳ | ENC-36 | 🔌 [Eletrônica Analógica I](eletronica-analogica-i/README.md) | 68 h | Profissionalizante |
| ⏳ | ENC-37 | 🔌 [Circuitos Elétricos II](circuitos-eletricos-ii/README.md) | 68 h | Profissionalizante |
| ⏳ | ENC-38 | 🔌 [Laboratório de Circuitos Elétricos II](lab-circuitos-eletricos-ii/README.md) | 34 h | Profissionalizante |
| ⏳ | ENC-39 | ➗ [Sinais e Sistemas Lineares](sinais-sistemas-lineares/README.md) | 68 h | Específico |
| ⏳ | ENC-40 | 🏗️ [Análise e Projeto de Sistemas Computacionais](analise-projeto-sistemas-computacionais/README.md) | 68 h | Específico |
| ⏳ | ENC-41 | 🤖 [Inteligência Artificial](inteligencia-artificial/README.md) | 68 h | Específico |
| ⏳ | ENC-42 | 🌐 [Redes de Computadores](rede-computadores/README.md) | 68 h | Específico |

**Total:** 442 h · teórica 326 h · prática 102 h · extensão 14 h

> [!NOTE]
> Período calculado pelo fluxo regular do curso (2027/1); ajuste se cursou ou for cursar em outro período.

## 🔗 Pré-requisitos

```mermaid
flowchart LR
  subgraph antes["Semestres anteriores"]
    ENC21["Probabilidade e Estatística Computacional"]
    ENC22["Equações Diferenciais"]
    ENC23["Física Geral e Experimental III"]
    ENC28["Transmissão e Comunicação de Dados"]
    ENC31["Circuitos Elétricos I"]
    ENC34["Engenharia de Software"]
  end
  subgraph agora["6º semestre"]
    ENC36["Eletrônica Analógica I"]
    ENC37["Circuitos Elétricos II"]
    ENC38["Laboratório de Circuitos Elétricos II"]
    ENC39["Sinais e Sistemas Lineares"]
    ENC40["Análise e Projeto de Sistemas Computacionais"]
    ENC41["Inteligência Artificial"]
    ENC42["Redes de Computadores"]
  end
  ENC23 --> ENC36
  ENC31 --> ENC37
  ENC31 --> ENC38
  ENC22 --> ENC39
  ENC31 --> ENC39
  ENC34 --> ENC40
  ENC21 --> ENC41
  ENC28 --> ENC42
```
