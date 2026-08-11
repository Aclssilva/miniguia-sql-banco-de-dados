# 📚 Caderno Temático: SQL e Dados

![Status](https://img.shields.io/badge/status-concluído-success)
![Tema](https://img.shields.io/badge/tema-SQL%20e%20Dados-blue)
![Ferramenta](https://img.shields.io/badge/IA-NotebookLM-orange)

> Projeto desenvolvido para o Desafio de Projeto da DIO, explorando a Inteligência Artificial como ferramenta de aprendizagem ativa.

---

## 🎯 Sobre o Projeto

Este projeto apresenta um **Caderno Temático sobre SQL e Dados**, desenvolvido com o objetivo de estudar e consolidar conhecimentos fundamentais sobre bancos de dados relacionais, SQL e modelagem de dados.

O **NotebookLM** foi utilizado como ferramenta de apoio ao processo de aprendizagem, permitindo trabalhar com fontes previamente selecionadas, realizar perguntas, explorar conceitos, testar diferentes estratégias de prompts e revisar criticamente as respostas obtidas.

Mais do que reunir informações, o projeto busca demonstrar um processo de aprendizagem baseado em:

**curadoria → exploração → questionamento → validação → organização → revisão.**

---

# 🧠 Objetivos

Os principais objetivos do projeto foram:

* compreender os fundamentos de bancos de dados;
* entender o modelo relacional;
* conhecer o funcionamento dos SGBDs;
* aprender os principais conceitos de SQL;
* compreender chaves primárias e estrangeiras;
* estudar modelagem e Diagramas Entidade-Relacionamento;
* praticar consultas e operações SQL;
* explorar o uso de Inteligência Artificial no processo de aprendizagem;
* desenvolver estratégias de engenharia de prompts;
* avaliar criticamente respostas geradas por IA;
* consolidar o conhecimento em um material reutilizável.

---

# 🗂️ Estrutura do Projeto

```text
caderno-tematico-sql-dados/
│
├── README.md
│
├── fontes/
│   └── fontes.md
│
├── prompts/
│   └── engenharia-de-prompts.md
│
└── miniguia/
    ├── resumo.md
    ├── glossario.md
    └── prompts-reutilizaveis.md
```

---

# 📖 1. Curadoria de Fontes

Foram selecionadas fontes abertas de diferentes tipos para construir a base de conhecimento do NotebookLM.

A curadoria buscou combinar:

* documentação oficial;
* materiais educacionais;
* tutoriais interativos;
* videoaulas;
* materiais voltados à prática.

### 📚 Fontes utilizadas

Entre os materiais consultados estão conteúdos de:

* PostgreSQL;
* MySQL;
* Microsoft Learn;
* Khan Academy;
* SQLBolt;
* freeCodeCamp;
* Curso em Vídeo;
* Simplilearn.

👉 **[Ver a curadoria completa de fontes](fontes/fontes.md)**

---

# 🤖 2. NotebookLM como Ferramenta de Aprendizagem

O NotebookLM foi utilizado como uma ferramenta de aprendizagem ativa.

Em vez de simplesmente solicitar respostas sobre SQL, o processo buscou utilizar a ferramenta para:

* explorar conceitos;
* fazer perguntas de aprofundamento;
* solicitar exemplos;
* comparar conceitos;
* identificar limitações das fontes;
* revisar respostas anteriores;
* testar diferentes formas de elaboração de prompts.

Uma das estratégias mais importantes foi estabelecer limites para a IA, solicitando que determinadas respostas fossem produzidas **exclusivamente com base nas fontes fornecidas**.

Isso permitiu observar não apenas o que as fontes apresentavam, mas também identificar informações que não estavam disponíveis no material.

---

# 🧪 3. Engenharia de Prompts

Durante o projeto, os prompts foram evoluindo de perguntas mais abertas para instruções mais estruturadas.

O processo passou por etapas como:

```text
Pergunta ampla
      ↓
Prompt estruturado
      ↓
Exploração de novos conceitos
      ↓
Questionamento
      ↓
Auditoria crítica
      ↓
Validação
```

Os experimentos foram documentados considerando:

* objetivo do prompt;
* estratégia utilizada;
* resposta obtida;
* análise crítica;
* aprendizados;
* problemas encontrados;
* soluções utilizadas.

👉 **[Ver os experimentos de engenharia de prompts](prompts/engenharia-de-prompts.md)**

---

# 🩹 4. Cicatrizes e Troubleshooting

Durante o desenvolvimento, alguns problemas e limitações foram identificados.

### 🔎 Prompt muito amplo

Perguntas genéricas produziram respostas úteis para introdução, mas pouco aprofundadas.

**Solução:** especificar público, objetivo, estrutura e profundidade esperada.

### 🔎 Respostas detalhadas não são necessariamente precisas

Uma resposta extensa pode conter simplificações ou interpretações que precisam ser verificadas.

**Solução:** utilizar prompts de auditoria e validação.

### 🔎 Limitações das fontes

Alguns conceitos procurados não estavam explicitamente presentes nos materiais selecionados.

**Solução:** solicitar que a IA informasse quando não houvesse evidência suficiente, evitando completar as lacunas com conhecimento externo.

Essas situações foram importantes para compreender que o uso de IA exige **pensamento crítico e validação**, e não apenas geração de respostas.

---

# 📘 5. Miniguia de Estudo

O conhecimento obtido durante o projeto foi consolidado em um material de revisão.

### 📚 Resumo

Conteúdo sobre:

* bancos de dados;
* modelo relacional;
* SGBDs;
* modelagem;
* Diagramas ER;
* chaves;
* SQL;
* `SELECT`;
* `WHERE`;
* `ORDER BY`;
* agregações;
* `GROUP BY`;
* `HAVING`;
* `JOIN`;
* subconsultas;
* `INSERT`;
* `UPDATE`;
* `DELETE`;
* CRUD;
* restrições;
* erros comuns.

👉 **[Acessar o resumo de SQL e Dados](miniguia/resumo.md)**

### 📑 Glossário

Lista dos principais termos estudados e suas respectivas definições.

👉 **[Acessar o glossário](miniguia/glossario.md)**

### ♻️ Prompts Reutilizáveis

Biblioteca de prompts desenvolvida durante o projeto para apoiar futuros estudos de SQL, programação e outros assuntos técnicos.

👉 **[Acessar os prompts reutilizáveis](miniguia/prompts-reutilizaveis.md)**

---

# 📊 6. Infográfico

Como recurso visual complementar, foi produzido um infográfico reunindo os principais conceitos abordados no caderno temático.

> O infográfico será disponibilizado nesta seção após sua geração no NotebookLM.

---

# 💡 7. Principais Aprendizados

O desenvolvimento do projeto permitiu perceber que utilizar Inteligência Artificial para estudar não significa simplesmente perguntar e aceitar a primeira resposta.

O processo mais eficiente envolveu:

### 1. Curadoria

Selecionar fontes confiáveis antes de começar a exploração.

### 2. Contextualização

Explicar para a IA qual era o objetivo e o nível de conhecimento esperado.

### 3. Questionamento

Fazer perguntas progressivamente mais específicas.

### 4. Validação

Verificar se as respostas realmente eram sustentadas pelas fontes.

### 5. Pensamento crítico

Questionar simplificações, possíveis erros e informações ausentes.

### 6. Organização

Transformar as descobertas em um material estruturado para futuras revisões.

---

# 🎓 Reflexão Final

Este projeto mostrou que a Inteligência Artificial pode ser utilizada como uma ferramenta de aprendizagem ativa quando o estudante participa de forma crítica do processo.

Durante o estudo de SQL e Dados, o NotebookLM foi utilizado não apenas para obter explicações, mas também para explorar conceitos, gerar perguntas, comparar informações e revisar respostas.

Um dos principais aprendizados foi perceber que **a qualidade da resposta depende também da qualidade da pergunta**.

Além disso, a utilização de fontes selecionadas tornou possível trabalhar com uma abordagem mais controlada, permitindo identificar quando uma informação estava sustentada pelo material e quando seria necessário investigar ou validar melhor.

Dessa forma, o projeto contribuiu não apenas para o aprendizado de SQL e bancos de dados, mas também para o desenvolvimento de habilidades relacionadas a:

* pensamento crítico;
* curadoria de informações;
* engenharia de prompts;
* validação de conteúdo;
* organização do conhecimento;
* uso responsável de Inteligência Artificial.

---

# 🚀 Conclusão

O Caderno Temático consolidou os principais fundamentos estudados sobre **SQL e Dados** em um material de consulta que pode continuar sendo utilizado durante a graduação e em estudos futuros.

Além do conhecimento técnico, o projeto demonstra uma metodologia de aprendizagem que pode ser aplicada a diferentes áreas da tecnologia:

> **Pesquisar → Questionar → Testar → Validar → Organizar → Aplicar**

---

## 👩‍💻 Projeto

**Tema:** SQL e Dados
**Ferramenta de IA:** NotebookLM
**Plataforma:** DIO
**Repositório:** GitHub

---

⭐ Se este projeto foi útil para você, considere deixar uma estrela no repositório!
