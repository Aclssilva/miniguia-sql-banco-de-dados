# ♻️ Prompts Reutilizáveis — SQL e Dados

> Biblioteca de prompts desenvolvida a partir dos experimentos realizados durante o projeto. Os prompts podem ser reutilizados no NotebookLM ou adaptados para outras ferramentas de Inteligência Artificial.

---

# 1. 📚 Explicação para Iniciantes

### Objetivo

Compreender um conceito técnico sem assumir conhecimento prévio.

### Prompt

> Explique o conceito de **[CONCEITO]** para uma pessoa que está começando a estudar Sistemas de Informação.
>
> Organize a resposta em:
>
> 1. O que é;
> 2. Para que serve;
> 3. Como funciona;
> 4. Exemplo prático;
> 5. Exemplo em SQL, quando aplicável;
> 6. Erros comuns de iniciantes.
>
> Utilize linguagem clara, mas preserve a precisão técnica. Baseie a explicação nas fontes disponíveis e indique quando uma informação não estiver presente nelas.

---

# 2. 🔎 Aprofundamento de um Conceito

### Objetivo

Aprofundar um assunto depois de obter uma explicação introdutória.

### Prompt

> Quero aprofundar meus conhecimentos sobre **[CONCEITO]**.
>
> Com base nas fontes disponíveis:
>
> * explique o conceito com maior profundidade;
> * apresente exemplos práticos;
> * mostre como ele é utilizado em sistemas reais;
> * apresente exemplos de SQL quando aplicável;
> * explique conceitos relacionados;
> * destaque erros comuns;
> * indique quais pontos são mais importantes para uma avaliação acadêmica ou entrevista técnica.
>
> Diferencie claramente informações diretamente sustentadas pelas fontes de possíveis inferências.

---

# 3. 🧩 Explicação com Analogia

### Objetivo

Facilitar a compreensão de conceitos abstratos.

### Prompt

> Explique **[CONCEITO]** utilizando uma analogia do cotidiano.
>
> Primeiro apresente a analogia de forma simples. Depois faça o mapeamento entre cada elemento da analogia e o conceito técnico real.
>
> Finalize explicando onde a analogia deixa de ser válida para evitar interpretações incorretas.

---

# 4. 💻 Aprendendo SQL na Prática

### Objetivo

Aprender um comando SQL através de exemplos progressivos.

### Prompt

> Ensine o comando **[COMANDO SQL]** começando do nível iniciante.
>
> Apresente:
>
> 1. Para que serve;
> 2. Sintaxe básica;
> 3. Exemplo simples;
> 4. Exemplo intermediário;
> 5. Exemplo mais avançado;
> 6. Erros comuns;
> 7. Um exercício para eu resolver sozinho.
>
> Não forneça a resposta do exercício imediatamente. Aguarde minha tentativa e depois corrija minha solução.

---

# 5. 🧪 Exercícios de SQL

### Objetivo

Transformar conhecimento teórico em prática.

### Prompt

> Crie **[NÚMERO] exercícios de SQL** sobre **[TEMA]**.
>
> Considere que meu nível é **[INICIANTE/INTERMEDIÁRIO/AVANÇADO]**.
>
> Para cada exercício, forneça:
>
> * contexto;
> * estrutura das tabelas necessárias;
> * dados de exemplo;
> * pergunta que devo responder;
> * nível de dificuldade.
>
> Não forneça as respostas inicialmente.
>
> Depois que eu enviar minhas soluções, corrija cada uma, explique os erros e apresente uma solução alternativa quando existir.

---

# 6. 🐛 Debug de SQL

### Objetivo

Encontrar e compreender erros em consultas SQL.

### Prompt

> Analise a seguinte consulta SQL:
>
> ```sql
> [COLE SEU CÓDIGO AQUI]
> ```
>
> Identifique:
>
> 1. erros de sintaxe;
> 2. possíveis erros de lógica;
> 3. problemas relacionados aos dados;
> 4. possíveis problemas de desempenho, quando relevantes;
> 5. como corrigir cada problema.
>
> Explique o motivo de cada correção de forma didática.
>
> Considere que estou utilizando **[MYSQL/POSTGRESQL/SQL SERVER/OUTRO]**.

---

# 7. 🔗 Aprendendo JOIN

### Objetivo

Compreender relacionamentos entre tabelas.

### Prompt

> Explique **[TIPO DE JOIN]** utilizando duas tabelas simples.
>
> Mostre:
>
> 1. estrutura das tabelas;
> 2. dados de exemplo;
> 3. relacionamento entre elas;
> 4. consulta SQL;
> 5. resultado esperado;
> 6. explicação linha por linha da consulta.
>
> Depois compare esse JOIN com **[OUTRO JOIN]** e explique em quais situações cada um seria utilizado.

---

# 8. 📐 Modelagem de Dados

### Objetivo

Aprender a transformar requisitos em um modelo de banco de dados.

### Prompt

> Considere o seguinte cenário:
>
> **[DESCREVA O SISTEMA]**
>
> Ajude-me a identificar:
>
> * entidades;
> * atributos;
> * possíveis chaves primárias;
> * chaves estrangeiras;
> * relacionamentos;
> * cardinalidades;
> * possíveis entidades fracas;
> * possíveis problemas de modelagem.
>
> Depois apresente uma proposta de modelo relacional e explique como cada elemento do modelo ER seria convertido em tabelas.

---

# 9. 🧠 Revisão para Prova

### Objetivo

Preparar uma revisão baseada nos conteúdos estudados.

### Prompt

> Com base exclusivamente nas fontes disponíveis, crie uma revisão de **[TEMA]** para uma prova de Sistemas de Informação.
>
> Organize em:
>
> * conceitos fundamentais;
> * definições que preciso saber;
> * diferenças entre conceitos semelhantes;
> * exemplos;
> * comandos SQL importantes;
> * erros comuns;
> * perguntas que um professor poderia fazer.
>
> No final, crie um quiz com **[NÚMERO] perguntas**, sem apresentar as respostas imediatamente.

---

# 10. 📝 Simulado

### Objetivo

Testar o conhecimento sem consultar o material.

### Prompt

> Crie um simulado sobre **[TEMA]** para um estudante de Sistemas de Informação.
>
> Inclua:
>
> * questões conceituais;
> * questões de interpretação de código SQL;
> * questões práticas;
> * questões de modelagem;
> * questões de verdadeiro ou falso.
>
> Misture diferentes níveis de dificuldade.
>
> Não apresente o gabarito até que eu envie minhas respostas.
>
> Depois corrija meu desempenho, indique quais conceitos preciso revisar e explique meus erros.

---

# 11. 🔍 Comparação de Conceitos

### Objetivo

Entender diferenças entre conceitos que costumam ser confundidos.

### Prompt

> Compare **[CONCEITO A]** e **[CONCEITO B]**.
>
> Apresente uma tabela contendo:
>
> | Critério        | Conceito A | Conceito B |
> | --------------- | ---------- | ---------- |
> | Definição       |            |            |
> | Finalidade      |            |            |
> | Quando utilizar |            |            |
> | Exemplo         |            |            |
> | Erro comum      |            |            |
>
> Finalize com uma explicação simples sobre a principal diferença entre os dois.

---

# 12. 🧑‍🏫 Professor Particular

### Objetivo

Utilizar a IA como tutora durante o processo de aprendizagem.

### Prompt

> A partir deste momento, atue como meu professor particular de **[TEMA]**.
>
> Meu nível atual é **[NÍVEL]**.
>
> Quero aprender por meio de explicações, exemplos e exercícios.
>
> Não entregue imediatamente a resposta dos exercícios. Primeiro faça perguntas ou dê pistas que me ajudem a chegar à solução.
>
> Quando eu responder:
>
> 1. avalie minha resposta;
> 2. diga o que está correto;
> 3. identifique os erros;
> 4. explique como melhorar;
> 5. apresente a solução completa somente depois da minha tentativa.
>
> Priorize compreensão em vez de memorização.

---

# 13. 🩺 Auditoria de uma Resposta da IA

### Objetivo

Verificar se uma resposta produzida anteriormente é confiável.

### Prompt

> Revise criticamente a resposta abaixo:
>
> **[COLE A RESPOSTA]**
>
> Classifique cada afirmação relevante em uma das categorias:
>
> * correta e sustentada pelas fontes;
> * correta, mas simplificada;
> * tecnicamente imprecisa;
> * não sustentada pelas fontes.
>
> Para cada problema encontrado:
>
> * explique o motivo;
> * indique qual fonte permite verificar a informação;
> * apresente uma versão corrigida.
>
> Não complemente a resposta com conhecimento externo quando as fontes não forem suficientes.

---

# 14. 📚 Comparação entre Fontes

### Objetivo

Identificar diferenças entre materiais utilizados no estudo.

### Prompt

> Compare como as fontes disponíveis explicam **[CONCEITO]**.
>
> Identifique:
>
> * pontos em comum;
> * diferenças de abordagem;
> * diferenças de terminologia;
> * informações presentes em uma fonte e ausentes em outra;
> * possíveis contradições.
>
> Não tente eliminar uma diferença automaticamente. Informe quando as fontes simplesmente apresentam perspectivas diferentes.

---

# 15. 🚨 Verificação de Alucinações

### Objetivo

Identificar informações que podem ter sido inventadas ou extrapoladas pela IA.

### Prompt

> Analise a resposta abaixo exclusivamente com base nas fontes disponíveis:
>
> **[COLE A RESPOSTA]**
>
> Para cada afirmação importante, indique:
>
> **🟢 Sustentada:** existe evidência clara nas fontes.
>
> **🟡 Parcial:** a fonte aborda o assunto, mas a resposta extrapola ou simplifica.
>
> **🔴 Não sustentada:** não encontrei evidência suficiente nas fontes.
>
> Não tente preencher lacunas com conhecimento externo.

---

# 16. 🔄 Transformar Conteúdo em Resumo

### Objetivo

Transformar uma explicação extensa em material de revisão.

### Prompt

> Transforme o conteúdo abaixo em um resumo para revisão:
>
> **[COLE O CONTEÚDO]**
>
> Preserve os conceitos tecnicamente importantes.
>
> Organize em:
>
> * conceitos fundamentais;
> * definições;
> * exemplos;
> * comandos importantes;
> * diferenças entre conceitos;
> * erros comuns.
>
> Não remova informações importantes apenas para deixar o texto menor.

---

# 17. 🎯 Prompt de Revisão Final

### Objetivo

Avaliar se o conteúdo estudado foi realmente compreendido.

### Prompt

> Com base nos conteúdos estudados sobre **[TEMA]**, avalie meu domínio do assunto.
>
> Faça perguntas progressivas, começando pelo nível básico e aumentando a dificuldade conforme minhas respostas.
>
> Não revele imediatamente se estou correto.
>
> Quando eu responder:
>
> * avalie meu raciocínio;
> * identifique lacunas;
> * faça uma pergunta de aprofundamento quando necessário;
> * registre quais conceitos preciso revisar.
>
> Ao final, produza um diagnóstico do meu nível de conhecimento e uma lista de tópicos para revisão.

---

# 💡 Como criar bons prompts

Durante o projeto, alguns elementos demonstraram ser especialmente úteis para melhorar as respostas:

### 1. Defina o contexto

Explique quem está fazendo a pergunta e qual é o objetivo.

**Exemplo:**

> Sou estudante de Sistemas de Informação e estou começando a estudar SQL.

### 2. Defina o material permitido

Quando estiver utilizando o NotebookLM:

> Utilize exclusivamente as fontes disponíveis neste caderno.

### 3. Defina o formato

Especifique se deseja:

* tabela;
* tópicos;
* exemplos;
* código;
* exercícios;
* comparação;
* passo a passo.

### 4. Estabeleça limites

Por exemplo:

> Caso as fontes não apresentem uma informação, informe que ela não está disponível em vez de inventar ou completar com conhecimento externo.

### 5. Peça validação

Uma boa resposta não precisa ser o fim da interação.

É possível solicitar:

> Agora revise criticamente sua resposta anterior e identifique possíveis simplificações ou informações não sustentadas pelas fontes.

---

# 🧠 Fórmula prática

Uma estrutura simples para criar novos prompts é:

```text
CONTEXTO
   +
OBJETIVO
   +
FONTES
   +
TAREFA
   +
FORMATO
   +
RESTRIÇÕES
   +
VALIDAÇÃO
```

### Exemplo

```text
CONTEXTO:
Sou estudante de Sistemas de Informação.

OBJETIVO:
Quero compreender JOINs.

FONTES:
Utilize exclusivamente as fontes deste caderno.

TAREFA:
Explique INNER JOIN, LEFT JOIN e RIGHT JOIN.

FORMATO:
Use exemplos com tabelas e código SQL.

RESTRIÇÕES:
Não utilize conhecimento externo às fontes.

VALIDAÇÃO:
Indique quais afirmações são diretamente sustentadas pelas fontes.
```

---

# 🚀 Aplicação além de SQL

A principal ideia deste conjunto de prompts é que eles não precisam ser utilizados exclusivamente para SQL.

A estrutura pode ser adaptada para outros assuntos técnicos, como:

* Java;
* Python;
* Engenharia de Software;
* Redes;
* Sistemas Operacionais;
* Ciência de Dados;
* Inteligência Artificial;
* Segurança da Informação.

O mais importante é manter o processo:

**perguntar → testar → analisar → validar → revisar → aplicar.**

---

# 🎓 Conclusão

A utilização de prompts estruturados transforma a Inteligência Artificial de uma simples ferramenta de respostas em um recurso de apoio ao processo de aprendizagem.

O estudante pode utilizar a IA para:

* explicar conceitos;
* criar exercícios;
* corrigir soluções;
* identificar erros;
* comparar informações;
* revisar conteúdos;
* testar conhecimentos;
* e questionar respostas anteriores.

Porém, o processo de aprendizagem continua dependendo do pensamento crítico e da validação das informações.

> **A IA pode ajudar a encontrar respostas. Aprender envolve entender por que elas estão corretas.**
