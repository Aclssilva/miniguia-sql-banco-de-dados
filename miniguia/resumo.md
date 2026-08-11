# 📘 Miniguia de Estudo — SQL e Dados

> Material de revisão elaborado a partir das fontes selecionadas no NotebookLM durante o desenvolvimento deste projeto.

---

# 1. 🗄️ Fundamentos de Bancos de Dados

## O que é um banco de dados?

Um banco de dados é uma coleção organizada de dados relacionados, armazenada de forma que as informações possam ser consultadas e manipuladas.

Em sistemas computacionais, bancos de dados são utilizados para armazenar informações como:

* clientes;
* produtos;
* pedidos;
* funcionários;
* alunos;
* pagamentos;
* registros de acesso.

Um banco de dados não deve ser confundido com o software utilizado para gerenciá-lo.

### Exemplo

Um sistema de uma faculdade pode armazenar:

```text
Alunos
Cursos
Professores
Disciplinas
Matrículas
Notas
```

Essas informações podem estar relacionadas entre si e serem consultadas por diferentes aplicações.

---

# 2. 🧩 Banco de Dados Relacional

O modelo relacional organiza os dados em estruturas chamadas **relações**, normalmente representadas como tabelas.

Uma tabela é composta por:

* **colunas:** representam atributos;
* **linhas:** representam registros ou tuplas.

### Exemplo

| id_aluno | nome  | curso                  |
| -------: | ----- | ---------------------- |
|        1 | Ana   | Sistemas de Informação |
|        2 | João  | História               |
|        3 | Maria | Administração          |

Nesse exemplo:

* `id_aluno`, `nome` e `curso` são atributos;
* cada linha representa um registro;
* a tabela representa uma relação.

O modelo relacional permite relacionar informações armazenadas em diferentes tabelas.

---

# 3. ⚙️ SGBD

**SGBD** significa **Sistema Gerenciador de Banco de Dados**.

É o software responsável por permitir a criação, manutenção, consulta e controle dos bancos de dados.

Alguns exemplos de SGBDs relacionais são:

* MySQL;
* PostgreSQL;
* Microsoft SQL Server;
* Oracle.

### SQL × Banco de Dados × SGBD

É importante não confundir esses conceitos:

| Conceito       | O que é?                                                  |
| -------------- | --------------------------------------------------------- |
| Banco de dados | Conjunto organizado de dados                              |
| SGBD           | Software que gerencia os dados                            |
| SQL            | Linguagem utilizada para interagir com bancos relacionais |

---

# 4. 🧱 Modelagem de Dados

Antes de criar as tabelas de um banco de dados, é importante compreender quais informações precisam ser armazenadas e como elas se relacionam.

A **modelagem de dados** ajuda a representar essa estrutura antes da implementação.

Um dos modelos utilizados nessa etapa é o **modelo Entidade-Relacionamento (ER)**.

---

# 5. 📐 Diagramas Entidade-Relacionamento

O Diagrama Entidade-Relacionamento é uma representação visual utilizada para descrever entidades e os relacionamentos existentes entre elas.

Ele pode ser utilizado como uma representação intermediária entre os requisitos do sistema e a estrutura que será implementada no banco de dados.

## Principais elementos

### Entidade

Representa um objeto ou conceito sobre o qual queremos armazenar informações.

Exemplos:

```text
Aluno
Professor
Produto
Cliente
Pedido
```

Na representação ER clássica, entidades são representadas por **retângulos**.

### Atributo

Representa uma característica de uma entidade.

Exemplo:

```text
Aluno
 ├── id
 ├── nome
 ├── email
 └── data_nascimento
```

Na representação ER clássica, atributos são representados por **ovais**.

### Relacionamento

Representa uma associação entre entidades.

Exemplo:

```text
Cliente ─── realiza ─── Pedido
```

Na representação ER clássica, relacionamentos são representados por **losangos**.

---

# 6. 🔑 Chaves

As chaves são fundamentais para identificar registros e estabelecer relações entre tabelas.

## Chave Primária — Primary Key (PK)

A chave primária identifica unicamente cada registro de uma tabela.

Exemplo:

```sql
CREATE TABLE alunos (
    id_aluno INT PRIMARY KEY,
    nome VARCHAR(100)
);
```

Nesse exemplo, `id_aluno` é a chave primária.

### Características

Uma chave primária:

* identifica registros de forma única;
* não pode possuir valores nulos;
* não pode possuir valores duplicados.

---

## Chave Estrangeira — Foreign Key (FK)

A chave estrangeira é utilizada para estabelecer uma relação entre tabelas.

Exemplo:

```sql
CREATE TABLE cursos (
    id_curso INT PRIMARY KEY,
    nome VARCHAR(100)
);

CREATE TABLE alunos (
    id_aluno INT PRIMARY KEY,
    nome VARCHAR(100),
    id_curso INT,
    FOREIGN KEY (id_curso) REFERENCES cursos(id_curso)
);
```

Nesse exemplo, `id_curso` em `alunos` funciona como chave estrangeira relacionada a `cursos`.

---

# 7. 🔗 Relacionamentos e Cardinalidade

A cardinalidade representa quantas instâncias de uma entidade podem estar relacionadas a instâncias de outra.

Os relacionamentos mais comuns são:

### 1:1 — Um para Um

Uma ocorrência de uma entidade está relacionada a uma ocorrência de outra.

```text
Pessoa ─── possui ─── CPF
```

### 1:N — Um para Muitos

Uma ocorrência de uma entidade pode estar relacionada a várias ocorrências de outra.

```text
Cliente ─── possui ─── Pedidos
```

Um cliente pode realizar vários pedidos.

### N:N — Muitos para Muitos

Várias ocorrências de uma entidade podem estar relacionadas a várias ocorrências de outra.

```text
Aluno ─── cursa ─── Disciplina
```

Um aluno pode cursar várias disciplinas e uma disciplina pode possuir vários alunos.

No modelo relacional, relacionamentos N:N normalmente são representados por uma tabela intermediária.

---

# 8. 💻 SQL

**SQL (Structured Query Language)** é a linguagem utilizada para interagir com bancos de dados relacionais.

Com SQL é possível:

* consultar dados;
* inserir registros;
* atualizar informações;
* excluir registros;
* criar estruturas;
* definir restrições;
* trabalhar com diferentes objetos do banco.

---

# 9. 🔍 SELECT

O comando `SELECT` é utilizado para consultar dados.

### Selecionando todas as colunas

```sql
SELECT *
FROM alunos;
```

### Selecionando colunas específicas

```sql
SELECT nome, curso
FROM alunos;
```

Selecionar apenas as colunas necessárias pode tornar as consultas mais claras e evitar o retorno de dados desnecessários.

---

# 10. 🎯 WHERE

A cláusula `WHERE` permite filtrar os registros retornados.

```sql
SELECT *
FROM alunos
WHERE curso = 'Sistemas de Informação';
```

Também podemos utilizar operadores de comparação:

```sql
SELECT *
FROM produtos
WHERE preco > 100;
```

---

# 11. ↕️ ORDER BY

`ORDER BY` permite ordenar os resultados.

### Ordem crescente

```sql
SELECT *
FROM produtos
ORDER BY preco ASC;
```

### Ordem decrescente

```sql
SELECT *
FROM produtos
ORDER BY preco DESC;
```

---

# 12. 📊 Funções de Agregação

Funções de agregação permitem realizar cálculos sobre conjuntos de registros.

Algumas das principais são:

| Função    | Utilização            |
| --------- | --------------------- |
| `COUNT()` | Contar registros      |
| `SUM()`   | Somar valores         |
| `AVG()`   | Calcular média        |
| `MIN()`   | Encontrar menor valor |
| `MAX()`   | Encontrar maior valor |

### Exemplo

```sql
SELECT COUNT(*) AS total_alunos
FROM alunos;
```

---

# 13. 📦 GROUP BY

`GROUP BY` permite agrupar registros que possuem valores em comum.

Exemplo:

```sql
SELECT curso, COUNT(*) AS quantidade
FROM alunos
GROUP BY curso;
```

O resultado permite descobrir quantos alunos existem em cada curso.

---

# 14. 🔎 HAVING

`HAVING` permite filtrar grupos produzidos pelo `GROUP BY`.

Exemplo:

```sql
SELECT curso, COUNT(*) AS quantidade
FROM alunos
GROUP BY curso
HAVING COUNT(*) > 10;
```

### Diferença importante

```text
WHERE  → filtra registros antes do agrupamento
HAVING → filtra grupos depois do agrupamento
```

---

# 15. 🔗 JOINs

`JOIN` permite combinar informações provenientes de diferentes tabelas.

Imagine:

```text
CLIENTES
id_cliente
nome

PEDIDOS
id_pedido
id_cliente
valor
```

Podemos combinar as tabelas:

```sql
SELECT clientes.nome, pedidos.valor
FROM clientes
INNER JOIN pedidos
    ON clientes.id_cliente = pedidos.id_cliente;
```

## INNER JOIN

Retorna registros que possuem correspondência nas duas tabelas.

## LEFT JOIN

Retorna todos os registros da tabela da esquerda e os registros correspondentes da tabela da direita.

## RIGHT JOIN

Retorna todos os registros da tabela da direita e os correspondentes da tabela da esquerda.

### Atenção

A disponibilidade e a sintaxe de determinados tipos de `JOIN` podem variar entre diferentes SGBDs.

Por isso, diferenças entre implementações devem ser verificadas na documentação do SGBD utilizado.

---

# 16. 🧮 Subconsultas

Uma subconsulta é uma consulta SQL utilizada dentro de outra consulta.

Exemplo:

```sql
SELECT nome
FROM alunos
WHERE id_curso IN (
    SELECT id_curso
    FROM cursos
    WHERE nome = 'Sistemas de Informação'
);
```

Subconsultas podem ser utilizadas para criar consultas mais complexas a partir do resultado de outra consulta.

---

# 17. 🛡️ Integridade e Restrições

Os bancos de dados utilizam restrições para ajudar a manter a consistência dos dados.

Algumas restrições comuns incluem:

* `PRIMARY KEY`;
* `FOREIGN KEY`;
* `NOT NULL`;
* `UNIQUE`;
* `CHECK`.

### Exemplo

```sql
CREATE TABLE alunos (
    id_aluno INT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    email VARCHAR(150) UNIQUE
);
```

Nesse exemplo:

* `id_aluno` identifica o registro;
* `nome` não pode ser nulo;
* `email` não pode ser duplicado.

---

# 18. 📝 INSERT

Utilizado para inserir novos registros.

```sql
INSERT INTO alunos (id_aluno, nome, curso)
VALUES (1, 'Ana', 'Sistemas de Informação');
```

---

# 19. ✏️ UPDATE

Utilizado para modificar registros existentes.

```sql
UPDATE alunos
SET curso = 'Engenharia de Software'
WHERE id_aluno = 1;
```

### ⚠️ Atenção

É importante utilizar uma condição adequada no `WHERE`.

Um `UPDATE` sem `WHERE` pode modificar todos os registros da tabela.

---

# 20. 🗑️ DELETE

Utilizado para remover registros.

```sql
DELETE FROM alunos
WHERE id_aluno = 1;
```

### ⚠️ Atenção

Um `DELETE` sem `WHERE` pode remover todos os registros da tabela.

Por isso, comandos de alteração e exclusão devem ser utilizados com cuidado.

---

# 21. 🔄 CRUD

CRUD é uma forma de representar quatro operações fundamentais sobre dados:

| Operação | Significado   | Exemplo  |
| -------- | ------------- | -------- |
| Create   | Criar/Inserir | `INSERT` |
| Read     | Ler/Consultar | `SELECT` |
| Update   | Atualizar     | `UPDATE` |
| Delete   | Excluir       | `DELETE` |

O conceito de CRUD é útil para relacionar operações realizadas pelas aplicações com as operações de manipulação de dados.

---

# 22. 🧠 Diferenças entre SGBDs

SQL possui padrões, mas diferentes SGBDs podem apresentar diferenças de implementação, sintaxe e recursos.

Entre os SGBDs estudados estão:

* MySQL;
* PostgreSQL;
* Microsoft SQL Server.

Por isso, uma consulta SQL aprendida em um ambiente pode precisar de adaptações quando executada em outro.

### Boa prática

Ao estudar ou desenvolver uma aplicação, é importante consultar a documentação do SGBD utilizado.

---

# 23. ⚠️ Erros Comuns de Iniciantes

### Confundir banco de dados com SGBD

Banco de dados é o conjunto de dados. SGBD é o software responsável por gerenciá-lo.

### Confundir PK com FK

A PK identifica registros dentro de uma tabela.

A FK estabelece uma referência entre tabelas.

### Usar `SELECT *` indiscriminadamente

Embora seja útil para testes e exploração, selecionar explicitamente as colunas necessárias pode tornar as consultas mais claras.

### Esquecer o `WHERE` em `UPDATE` e `DELETE`

Pode resultar na alteração ou exclusão de todos os registros.

### Confundir `WHERE` e `HAVING`

```text
WHERE  → filtra registros
HAVING → filtra grupos
```

### Assumir que todo SQL funciona exatamente igual em qualquer SGBD

Diferentes sistemas podem implementar recursos e sintaxes de maneiras diferentes.

---

# 24. 🎯 Checklist de Revisão

Antes de considerar os fundamentos dominados, você deve conseguir explicar:

* [ ] O que é um banco de dados;
* [ ] O que é um banco de dados relacional;
* [ ] O que é um SGBD;
* [ ] A diferença entre banco de dados e SGBD;
* [ ] O que são tabelas, registros e atributos;
* [ ] O que é uma chave primária;
* [ ] O que é uma chave estrangeira;
* [ ] O que é cardinalidade;
* [ ] O que é um Diagrama ER;
* [ ] Para que serve o `SELECT`;
* [ ] Como utilizar `WHERE`;
* [ ] Como utilizar `ORDER BY`;
* [ ] Para que serve `GROUP BY`;
* [ ] A diferença entre `WHERE` e `HAVING`;
* [ ] O que é um `JOIN`;
* [ ] O que são subconsultas;
* [ ] O que significa CRUD;
* [ ] Para que servem `INSERT`, `UPDATE` e `DELETE`;
* [ ] Por que diferentes SGBDs podem apresentar diferenças.

---

# 📌 Observação sobre as fontes

Este resumo foi consolidado a partir das fontes selecionadas para o projeto e das interações realizadas no NotebookLM.

Durante o processo de validação, foi adotada a estratégia de não tratar automaticamente toda informação produzida pela IA como fato. Conceitos potencialmente ambíguos ou dependentes de implementação foram considerados com cautela e devem ser consultados na documentação específica do SGBD quando necessário.

---

## 📚 Próximos conteúdos

* [Glossário](glossario.md)
* [Prompts Reutilizáveis](prompts-reutilizaveis.md)
* [Engenharia de Prompts](../prompts/engenharia-de-prompts.md)
* [Curadoria de Fontes](../fontes/fontes.md)
