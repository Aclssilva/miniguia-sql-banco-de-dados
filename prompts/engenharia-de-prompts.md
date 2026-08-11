# 🧠 Engenharia de Prompts e Cicatrizes

## 1. Objetivo

Durante o desenvolvimento do Caderno Temático, foram realizados diferentes experimentos com prompts no NotebookLM.

O objetivo não foi apenas obter respostas sobre SQL e bancos de dados, mas observar como diferentes formas de formular perguntas influenciam a qualidade, profundidade e confiabilidade das respostas.

O processo foi dividido em etapas de exploração, aprofundamento e validação crítica.

---

# 🧪 Experimento 01 — Pergunta Inicial

## Objetivo

Obter uma visão geral sobre SQL e bancos de dados relacionais utilizando uma pergunta simples e aberta.

## Prompt

> Explique SQL e banco de dados relacionais para alguém que está começando a estudar o assunto.

## Resultado

O NotebookLM apresentou uma introdução aos principais conceitos de bancos de dados relacionais, incluindo:

* banco de dados;
* tabelas;
* linhas e colunas;
* chave primária;
* chave estrangeira;
* SQL;
* CRUD;
* SGBD;
* MySQL;
* PostgreSQL;
* SQL Server.

A resposta utilizou uma analogia com uma biblioteca para facilitar a compreensão dos conceitos iniciais.

## Análise

A resposta foi clara e adequada para iniciantes, mas apresentou uma abordagem predominantemente introdutória.

Embora tenha conseguido apresentar os principais conceitos, não foram solicitados exemplos de código, comparação entre fontes, erros comuns ou aprofundamento técnico.

## Aprendizado

Perguntas muito amplas são úteis para obter uma visão inicial do assunto, mas podem produzir respostas genéricas.

Isso levou à necessidade de desenvolver um prompt mais estruturado.

---

# 🧪 Experimento 02 — Prompt Estruturado

## Objetivo

Aumentar a profundidade e a utilidade da resposta, definindo explicitamente o público, os tópicos e o formato esperado.

## Estratégia utilizada

Foram adicionadas ao prompt:

* definição do público-alvo;
* organização por tópicos;
* exemplos práticos;
* exemplos de código SQL;
* erros comuns;
* comparação entre SGBDs;
* utilização das fontes do caderno.

## Prompt

> Com base nas fontes disponíveis neste caderno, explique os fundamentos de SQL e bancos de dados relacionais para um estudante de Sistemas de Informação que está começando a estudar o tema. Organize a resposta nas seguintes seções:
>
> 1. Banco de dados
> 2. Banco de dados relacional
> 3. Tabelas, registros e atributos
> 4. Chave primária e chave estrangeira
> 5. SGBD
> 6. SQL
> 7. Principais operações SQL
>
> Para cada conceito, apresente:
>
> * uma definição clara;
> * um exemplo prático;
> * um exemplo de código SQL quando aplicável;
> * um erro ou confusão comum de iniciantes.
>
> Utilize as fontes do caderno para fundamentar as explicações e indique quais fontes foram utilizadas em cada seção. Quando houver diferenças de terminologia ou implementação entre MySQL, PostgreSQL e SQL Server, destaque essas diferenças.
>
> Não simplifique conceitos de maneira que possa gerar uma interpretação tecnicamente incorreta.

## Resultado

A resposta apresentou uma estrutura significativamente mais detalhada.

Foram incluídos:

* definições;
* exemplos;
* código SQL;
* erros comuns;
* diferenças entre SGBDs;
* referências às fontes utilizadas.

## Comparação com o Experimento 01

O segundo prompt produziu uma resposta mais direcionada e útil para estudo.

A principal diferença foi que as instruções do prompt passaram a definir não apenas **o que deveria ser explicado**, mas também **como o conhecimento deveria ser apresentado**.

## Aprendizado

A especificidade do prompt influenciou diretamente a estrutura e a profundidade da resposta.

---

# 🔎 Experimento 03 — Exploração de Diagramas ER

## Contexto

Durante a exploração das fontes, o NotebookLM sugeriu uma pergunta relacionada a Diagramas Entidade-Relacionamento.

## Pergunta

> Poderia explicar o que são diagramas Entidade-Relacionamento (ER)?

## Resultado

A resposta apresentou os principais componentes do modelo ER, incluindo:

* entidades;
* entidades fracas;
* atributos;
* atributos-chave;
* atributos compostos;
* atributos multivalorados;
* atributos derivados;
* relacionamentos;
* cardinalidade;
* participação.

Também foram apresentados os símbolos utilizados na representação clássica de diagramas ER.

## Aprendizado

A interação demonstrou que perguntas exploratórias podem ampliar o escopo do estudo para assuntos relacionados às fontes, permitindo identificar novos conceitos importantes.

O estudo deixou de se concentrar apenas na linguagem SQL e passou a abordar também a etapa de **modelagem de dados**.

---

# 🧪 Experimento 04 — Questionando a Universalidade da Notação

## Objetivo

Verificar se a representação gráfica apresentada para Diagramas ER era universal ou se existiam diferentes formas de representação.

## Prompt

> A resposta anterior apresenta a notação clássica de diagramas Entidade-Relacionamento. Com base exclusivamente nas fontes deste caderno, explique se essa representação gráfica é universal ou se existem diferentes notações para modelagem de dados. Compare a notação ER clássica (Chen) com outras notações apresentadas ou mencionadas nas fontes.
>
> Para cada diferença, explique como entidades, atributos, relacionamentos e cardinalidades são representados. Caso alguma informação não esteja presente nas fontes, deixe isso explícito em vez de inferir ou complementar com conhecimento externo.

## Resultado

O NotebookLM identificou que as fontes apresentavam principalmente:

* Diagramas ER clássicos;
* representação de esquemas relacionais/tabelas.

Também identificou que os nomes de notações específicas, como Chen e Crow's Foot, não estavam explicitamente presentes nas fontes fornecidas.

## Aprendizado

O experimento demonstrou a importância de estabelecer limites claros para a IA.

Ao solicitar que ela utilizasse exclusivamente as fontes, foi possível observar não apenas o que os materiais apresentavam, mas também quais informações **não estavam disponíveis no conjunto de fontes**.

---

# 🩹 Experimento 05 — Auditoria Crítica

## Objetivo

Verificar se a resposta anterior continha simplificações ou possíveis imprecisões técnicas.

## Prompt

> Revise criticamente sua resposta anterior como se você fosse um professor avaliando uma resposta de aluno de Sistemas de Informação.
>
> Identifique especificamente quais afirmações da resposta podem estar:
>
> 1. corretas e diretamente sustentadas pelas fontes;
> 2. corretas, mas simplificadas;
> 3. tecnicamente imprecisas ou potencialmente equivocadas;
> 4. não sustentadas pelas fontes fornecidas.
>
> Dê atenção especial às afirmações sobre participação total/parcial, NOT NULL, ON DELETE CASCADE, entidades fracas, chaves estrangeiras e cardinalidade.
>
> Para cada possível problema, explique por que ele pode estar incorreto ou simplificado e indique a fonte que permite verificar a questão.
>
> Não acrescente conhecimento externo às fontes. Se as fontes não forem suficientes para determinar se uma afirmação está correta, declare explicitamente que não há evidência suficiente no material disponível.

## Resultado

A auditoria identificou diferentes níveis de confiabilidade nas afirmações anteriores.

Entre os principais pontos encontrados estavam:

* conceitos diretamente sustentados pelas fontes;
* conceitos apresentados de forma simplificada;
* possíveis inconsistências na representação de relacionamentos identificadores;
* associação excessivamente direta entre participação total e `ON DELETE CASCADE`;
* ausência de evidência suficiente nas fontes para algumas relações entre conceitos de modelagem e restrições SQL.

## Aprendizado

A etapa de auditoria demonstrou que uma resposta aparentemente correta pode conter simplificações ou interpretações que precisam ser verificadas.

A IA foi mais útil quando utilizada não apenas como geradora de respostas, mas também como ferramenta para **questionar e revisar informações previamente produzidas**.

---

# 🩹 Cicatrizes e Troubleshooting

## Cicatriz 01 — Prompt excessivamente amplo

O primeiro prompt produziu uma resposta correta e acessível, porém relativamente genérica.

### Problema

A pergunta não especificava:

* profundidade;
* estrutura;
* público;
* necessidade de exemplos;
* necessidade de código;
* necessidade de comparação entre fontes.

### Solução

Criar um prompt estruturado com instruções específicas sobre conteúdo e formato.

---

## Cicatriz 02 — Detalhamento não garante precisão

Mesmo com um prompt mais detalhado, algumas afirmações permaneceram simplificadas.

### Problema

Uma resposta mais extensa pode transmitir uma falsa impressão de maior precisão.

### Solução

Adicionar uma etapa específica de auditoria e validação das afirmações.

---

## Cicatriz 03 — Limitações das fontes

Durante a investigação sobre Diagramas ER, algumas informações procuradas não estavam presentes nas fontes.

### Problema

As fontes não apresentavam explicitamente algumas nomenclaturas e notações de modelagem.

### Solução

Solicitar ao NotebookLM que não utilizasse conhecimento externo e que declarasse explicitamente quando as fontes não fossem suficientes.

### Aprendizado

A ausência de informação nas fontes também é um resultado relevante da curadoria.

---

# 📊 Evolução da Estratégia

O processo de engenharia de prompts evoluiu da seguinte maneira:

```text
Pergunta ampla
      ↓
Prompt estruturado
      ↓
Exploração de novos conceitos
      ↓
Questionamento das respostas
      ↓
Auditoria crítica
      ↓
Validação baseada nas fontes
```

Essa evolução demonstrou que a qualidade do processo de aprendizagem não depende apenas da geração de uma boa resposta, mas também da capacidade de formular perguntas, estabelecer restrições, verificar evidências e reconhecer limitações.

---

# 💡 Principais Aprendizados

Durante os experimentos, foram identificados os seguintes aprendizados:

1. Prompts mais específicos tendem a produzir respostas mais estruturadas.
2. Definir o público-alvo ajuda a adequar a profundidade da explicação.
3. Solicitar exemplos práticos torna conceitos abstratos mais fáceis de compreender.
4. Respostas geradas por IA devem ser analisadas criticamente.
5. A qualidade e a diversidade das fontes influenciam diretamente os resultados.
6. É importante diferenciar informações sustentadas pelas fontes de inferências da IA.
7. Restringir a IA às fontes pode ajudar a identificar lacunas no material.
8. Uma resposta detalhada não é necessariamente uma resposta tecnicamente precisa.
9. A IA pode ser utilizada tanto para explicar conceitos quanto para revisar criticamente explicações anteriores.
10. O estudante continua sendo responsável por validar e interpretar o conhecimento obtido.
