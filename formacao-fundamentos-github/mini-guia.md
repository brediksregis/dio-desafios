# 📓 Miniguia de Estudos: Fundamentos de Git e GitHub com NotebookLM

Este repositório foi desenvolvido como entregável para o Desafio de Projeto da [DIO (Digital Innovation One)](https://dio.me), com o objetivo de demonstrar o uso da Inteligência Artificial (NotebookLM) como uma ferramenta de aprendizagem ativa para dominar os conceitos e práticas essenciais de Git e GitHub.

---

## 🎯 Contexto e Objetivos

O assunto escolhido para este caderno temático foi **Fundamentos de Git e GitHub**, tendo como base principal o material didático da Formação da DIO. 

### Objetivos de Estudo:
*   Compreender a diferença fundamental entre controle de versão local (Git) e plataforma de hospedagem/colaboração (GitHub).
*   Dominar o ciclo de vida dos arquivos no Git (Working Directory, Staging Area, Local Repository, Remote Repository).
*   Aprender as melhores práticas de ramificação (branching), commits semânticos e resolução de conflitos.
*   Explorar o fluxo de colaboração em equipe usando Pull Requests e code reviews.

---

## 📚 Curadoria de Fontes

Para alimentar o **NotebookLM** e construir o caderno temático, foram selecionadas as seguintes fontes abertas e oficiais:

1.  **Formação Fundamentos GitHub (Aline Antunes)**
    *   *Link:* [GitBook do Curso](https://aline-antunes.gitbook.io/formacao-fundamentos-github)
    *   *Descrição:* Guia conceitual e prático utilizado durante as aulas da formação.
2.  **Pro Git Book (Scott Chacon e Ben Straub)**
    *   *Link:* [Livro Oficial Pro Git](https://git-scm.com/book/pt-br/v2)
    *   *Descrição:* O manual definitivo e detalhado sobre o funcionamento interno do Git.
3.  **GitHub Git Cheat Sheet**
    *   *Link:* [Cheat Sheet Oficial (PDF)](https://education.github.com/git-cheat-sheet-education.pdf)
    *   *Descrição:* Guia de referência rápida para os comandos mais utilizados no dia a dia.
4.  **GitHub Flow Guide**
    *   *Link:* [Fluxo de Trabalho Oficial do GitHub](https://docs.github.com/pt/get-started/quickstart/github-flow)
    *   *Descrição:* Documentação do fluxo padrão de ramificação e entrega de código de forma colaborativa.

---

## 🧠 Engenharia de Prompts e "Cicatrizes"

Esta seção documenta a experiência prática de interação com o NotebookLM, detalhando como os prompts foram refinados para extrair as respostas mais completas e precisas.

> [!TIP]
> **Como preencher esta seção no seu projeto:** 
> Substitua os blocos abaixo com as suas reais interações no NotebookLM, descrevendo o que funcionou bem e onde a IA precisou de um "empurrãozinho" para responder corretamente.

### 🧪 Teste 1: Diferença entre Git e GitHub (Conceitual)
*   **Prompt Inicial:** *"O que é o Git e qual a diferença dele para o GitHub, com base nos materiais fornecidos?"*
*   **Resultado Obtido:** Uma resposta curta e genérica explicando que um é a ferramenta e o outro o site.
*   **Refinamento (Prompt Otimizado):** *"Com base no GitBook de Fundamentos do GitHub e no livro Pro Git, explique a diferença conceitual e prática entre o Git (como sistema de controle de versão distribuído) e o GitHub (como plataforma de colaboração). Use uma analogia do mundo real para ilustrar."*
*   **Resultado com Prompt Otimizado:** A IA gerou uma resposta muito mais robusta, usando a analogia de que o Git é como o editor de texto no seu computador e o GitHub é como o Google Docs na nuvem.

### 🧪 Teste 2: Resolução de Conflitos (Prático)
*   **Prompt Inicial:** *"Como resolvo conflito de merge?"*
*   **Resultado Obtido:** Passos genéricos de editor de texto, sem contextualizar os comandos de terminal.
*   **Refinamento (Prompt Otimizado):** *"Passo a passo: como um desenvolvedor júnior deve identificar, abrir no VS Code e resolver um conflito de merge após dar um `git pull`? Detalhe os comandos necessários (`git status`, `git add`, `git commit`) e como finalizar a sincronização com o repositório remoto."*
*   **Resultado com Prompt Otimizado:** A IA gerou um guia sequencial e seguro, explicando exatamente os delimitadores de conflito (`<<<<<<<`, `=======`, `>>>>>>>`).

### 🛠️ Dificuldades e Soluções (Troubleshooting / Cicatrizes)
*   **Problema de Alucinação/Contexto:** Em alguns momentos, a IA tentou recomendar ferramentas pagas ou fluxos complexos (como Git Flow avançado) que não estavam nas fontes.
*   **Como foi resolvido:** Ajustei o prompt para incluir restrições explícitas, por exemplo: *"Responda utilizando **apenas** o fluxo simplificado do GitHub Flow presente nas fontes selecionadas."*

---

## 📖 Miniguia de Estudo (Entrega Final)

### 📌 Resumos Estruturados

#### 1. Ciclo de Vida dos Arquivos (Git Lifecycle)
No Git, os arquivos passam por diferentes estados antes de serem consolidados no histórico:
*   **Untracked:** Arquivos novos que ainda não são rastreados pelo Git.
*   **Tracked (Unmodified):** Arquivos rastreados que não sofreram alterações desde o último commit.
*   **Modified:** Arquivos rastreados que foram alterados, mas cujas alterações ainda não foram salvas na área de preparação.
*   **Staged:** Arquivos cujas alterações foram selecionadas e preparadas para fazer parte do próximo commit.

```
 [ Working Directory ]  ---> (git add) --->  [ Staging Area ]  ---> (git commit) --->  [ Local Repository ]
```

#### 2. Boas Práticas de Commits Semânticos
Para manter o histórico do projeto legível e profissional:
*   Use verbos no imperativo (ex: `add`, `fix`, `refactor`).
*   **Commits Semânticos (padrão Angular):**
    *   `feat:` Nova funcionalidade.
    *   `fix:` Correção de bug.
    *   `docs:` Alterações na documentação (ex: README).
    *   `style:` Formatação de código que não altera o comportamento.
    *   `refactor:` Refatoração de código que não corrige bug nem adiciona funcionalidade.

---

### 📕 Glossário de Conceitos-Chave

| Termo | Definição Rápida |
| :--- | :--- |
| **Repository (Repositório)** | Pasta gerenciada pelo Git onde todo o histórico de alterações é salvo. |
| **Commit** | Um "print" ou registro do estado atual do seu código em um determinado momento. |
| **Branch (Ramificação)** | Uma linha de desenvolvimento paralela, que permite testar recursos sem afetar o código principal (`main`). |
| **Merge** | Ação de mesclar as alterações de uma branch em outra branch de destino. |
| **Pull Request (PR)** | Solicitação formal para que suas alterações (de uma branch) sejam revisadas e integradas ao repositório principal. |
| **Clone** | Cópia local de um repositório que está hospedado na nuvem (ex: GitHub). |
| **Fork** | Cópia de um repositório público de outro usuário para a sua própria conta do GitHub, permitindo modificações livres. |

---

### 🔄 Prompts Reutilizáveis para Revisão

Guarde estes prompts para usar in IA quando precisar revisar o conteúdo ou estudar para entrevistas técnicas:

*   **Revisão Teórica Rápida:**
    > *"Faça um questionário com 5 perguntas de múltipla escolha sobre o ciclo de vida de arquivos no Git e me forneça o gabarito comentado ao final."*
*   **Simulador de Cenários:**
    > *"Apresente um cenário hipotético de erro no Git (ex: commit na branch errada ou push indesejado) e me peça para explicar como resolveria. Avalie a minha resposta."*
*   **Treinador de Commits:**
    > *"Vou te passar uma lista de alterações que fiz no meu código. Com base nas boas práticas de commits semânticos, sugira 3 opções de mensagens de commit claras e adequadas."*

---
🔬 *Criado com a ajuda do NotebookLM e do DIO Agent como ferramenta de estudo ativo.*
