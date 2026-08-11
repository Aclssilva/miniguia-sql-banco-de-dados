# 📑 Glossário — SQL e Dados

> Principais termos estudados durante a construção do Caderno Temático.

---

## A

### Atributo

Característica ou propriedade de uma entidade. Em uma tabela relacional, normalmente corresponde a uma coluna.

**Exemplo:** `nome`, `email`, `data_nascimento`.

### Atributo Composto

Atributo que pode ser dividido em partes menores.

**Exemplo:** um atributo `Nome` pode ser dividido em `Primeiro Nome` e `Sobrenome`.

### Atributo Derivado

Atributo cujo valor pode ser obtido a partir de outros dados.

**Exemplo:** idade pode ser calculada a partir da data de nascimento.

---

## B

### Banco de Dados

Coleção organizada de dados relacionados que pode ser armazenada e manipulada por um sistema computacional.

### Banco de Dados Relacional

Modelo de banco de dados que organiza informações em relações, normalmente representadas por tabelas, e permite estabelecer relações entre elas.

---

## C

### Cardinalidade

Define quantas ocorrências de uma entidade podem estar relacionadas a ocorrências de outra entidade.

Exemplos:

* `1:1` — um para um;
* `1:N` — um para muitos;
* `N:N` — muitos para muitos.

### Chave Estrangeira — FK

Campo utilizado para estabelecer uma referência entre tabelas, normalmente apontando para uma chave primária.

### Chave Primária — PK

Campo ou conjunto de campos utilizado para identificar unicamente um registro em uma tabela.

### CRUD

Sigla para as quatro operações básicas de manipulação de dados:

* **Create** — criar;
* **Read** — consultar;
* **Update** — atualizar;
* **Delete** — excluir.

---

## D

### DELETE

Comando SQL utilizado para excluir registros de uma tabela.

```sql
DELETE FROM alunos
WHERE id_aluno = 1;
```

### Diagrama Entidade-Relacionamento — ER

Representação visual utilizada para modelar entidades, seus atributos e os relacionamentos existentes entre elas.

---

## E

### Entidade

Objeto ou conceito sobre o qual informações precisam ser armazenadas.

**Exemplos:** `Aluno`, `Cliente`, `Produto`.

### Entidade Fraca

Entidade que depende de outra entidade para sua identificação ou existência no modelo.

---

## F

### Foreign Key

Termo em inglês para **chave estrangeira (FK)**.

É utilizada para criar referências entre tabelas.

---

## G

### GROUP BY

Cláusula SQL utilizada para agrupar registros de acordo com um ou mais atributos.

```sql
SELECT curso, COUNT(*)
FROM alunos
GROUP BY curso;
```

---

## H

### HAVING

Cláusula utilizada para filtrar grupos produzidos por uma operação `GROUP BY`.

```sql
SELECT curso, COUNT(*)
FROM alunos
GROUP BY curso
HAVING COUNT(*) > 10;
```

**Diferença importante:**

`WHERE` filtra registros, enquanto `HAVING` filtra grupos.

---

## I

### INSERT

Comando SQL utilizado para inserir novos registros em uma tabela.

```sql
INSERT INTO alunos (id_aluno, nome)
VALUES (1, 'Ana');
```

### INNER JOIN

Tipo de `JOIN` que retorna registros que possuem correspondência entre as tabelas envolvidas.

---

## J

### JOIN

Operação utilizada para combinar dados provenientes de duas ou mais tabelas relacionadas.

Tipos comuns incluem:

* `INNER JOIN`;
* `LEFT JOIN`;
* `RIGHT JOIN`.

---

## L

### LEFT JOIN

Retorna todos os registros da tabela da esquerda e os registros correspondentes da tabela da direita.

---

## M

### Modelo Entidade-Relacionamento

Modelo utilizado para representar conceitualmente os dados de um sistema, suas entidades, atributos e relacionamentos.

### Muitos para Muitos — N:N

Relacionamento em que várias ocorrências de uma entidade podem estar associadas a várias ocorrências de outra.

---

## N

### NOT NULL

Restrição utilizada para impedir que uma coluna receba valores nulos.

### NULL

Representação utilizada em bancos de dados para indicar ausência ou desconhecimento de um valor.

> `NULL` não deve ser confundido com uma string vazia ou com o número zero.

---

## O

### ORDER BY

Cláusula SQL utilizada para ordenar os resultados de uma consulta.

```sql
SELECT *
FROM alunos
ORDER BY nome ASC;
```

---

## P

### PostgreSQL

SGBD relacional de código aberto que suporta SQL e diversos recursos avançados de gerenciamento de dados.

### Primary Key

Termo em inglês para **chave primária (PK)**.

---

## R

### Registro

Uma ocorrência individual armazenada em uma tabela. Também pode ser chamado de linha ou tupla.

### Relacionamento

Associação existente entre entidades em um modelo de dados.

### Relação

No modelo relacional, representa uma estrutura de dados que pode ser visualizada como uma tabela.

---

## S

### SGBD

Sigla para **Sistema Gerenciador de Banco de Dados**.

É o software responsável por gerenciar bancos de dados, permitindo operações como criação, consulta, alteração e exclusão de dados.

### SQL

**Structured Query Language**.

Linguagem utilizada para interagir com bancos de dados relacionais.

### SELECT

Comando utilizado para consultar dados.

```sql
SELECT nome
FROM alunos;
```

### SQL Server

SGBD relacional desenvolvido pela Microsoft.

---

## T

### Tabela

Estrutura utilizada no modelo relacional para armazenar dados organizados em linhas e colunas.

### Tupla

Termo utilizado no modelo relacional para representar uma linha ou registro de uma relação.

---

## U

### UPDATE

Comando SQL utilizado para modificar registros existentes.

```sql
UPDATE alunos
SET curso = 'Sistemas de Informação'
WHERE id_aluno = 1;
```

### UNIQUE

Restrição utilizada para impedir valores duplicados em uma coluna ou conjunto de colunas.

---

## W

### WHERE

Cláusula utilizada para filtrar registros em uma consulta ou determinar quais registros serão modificados ou excluídos.

```sql
SELECT *
FROM alunos
WHERE curso = 'Sistemas de Informação';
```

---

# 🧠 Conceitos para não confundir

| Conceitos             | Diferença                                                                                   |
| --------------------- | ------------------------------------------------------------------------------------------- |
| Banco de dados × SGBD | O banco contém os dados; o SGBD gerencia esses dados.                                       |
| PK × FK               | PK identifica registros; FK estabelece referências entre tabelas.                           |
| Tabela × Registro     | Tabela contém registros; registro representa uma ocorrência individual.                     |
| Coluna × Linha        | Coluna representa um atributo; linha representa um registro.                                |
| WHERE × HAVING        | WHERE filtra registros; HAVING filtra grupos.                                               |
| SQL × SGBD            | SQL é a linguagem; SGBD é o software que a executa e gerencia os dados.                     |
| Entidade × Atributo   | Entidade representa o objeto/conceito; atributo representa uma característica desse objeto. |
| 1:N × N:N             | 1:N relaciona uma ocorrência a várias; N:N permite múltiplas ocorrências de ambos os lados. |

---

# 📌 Resumo para Memorização

```text
BANCO DE DADOS
      ↓
organiza informações
      ↓
SGBD
      ↓
gerencia os dados
      ↓
SQL
      ↓
permite interagir com o banco
      ↓
TABELAS
      ↓
LINHAS + COLUNAS
      ↓
PK + FK
      ↓
estabelecem identificação e relações
```

---

## 🎯 Dica de estudo

Ao revisar SQL, tente explicar cada conceito com três elementos:

**1. O que é?**

Defina o conceito com suas próprias palavras.

**2. Para que serve?**

Explique qual problema ele resolve.

**3. Como aparece na prática?**

Crie um exemplo utilizando uma tabela ou comando SQL.

Essa estratégia ajuda a transformar memorização em compreensão.
