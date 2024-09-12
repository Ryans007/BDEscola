# README - Esquema de Banco de Dados

## Estrutura das Tabelas

### 1. Tabela PROFESSOR
- **Nome**: Nome do professor
- **SNome**: Sobrenome do professor
- **Matricula**: Identificador único do professor (Chave Primária)
- **DataNasc**: Data de nascimento do professor
- **Sexo**: Gênero do professor
- **Salario**: Salário do professor
- **Matric_Represent_Area**: Matricula do professor que representa a área (Chave Estrangeira referenciando PROFESSOR)
- **Depto**: Código do departamento ao qual o professor está associado (Chave Estrangeira referenciando DEPARTAMENTO)

### 2. Tabela DEPARTAMENTO
- **Nome**: Nome do departamento
- **Sigla**: Sigla do departamento
- **Codigo**: Código do departamento (Chave Primária)
- **Coordenador**: Matricula do coordenador do departamento (Chave Estrangeira referenciando PROFESSOR)

### 3. Tabela PROJETO
- **Nome**: Nome do projeto
- **Codigo**: Código do projeto (Chave Primária)
- **Depto**: Código do departamento ao qual o projeto está associado (Chave Estrangeira referenciando DEPARTAMENTO)
- **Duracao**: Duração do projeto

### 4. Tabela DEPENDENTE
- **MatricProf**: Matricula do professor ao qual o dependente está associado (Chave Estrangeira referenciando PROFESSOR)
- **Nome**: Nome do dependente
- **RG**: Registro Geral do dependente (deve ter 9 dígitos)
- **Sexo**: Gênero do dependente
- **DataNasc**: Data de nascimento do dependente

### 5. Tabela EMAIL
- **MatricProf**: Matricula do professor ao qual o e-mail está associado (Chave Estrangeira referenciando PROFESSOR)
- **Email**: Endereço de e-mail do professor

## Relacionamentos Entre Tabelas

- **PROFESSOR**
  - `Depto` referencia `DEPARTAMENTO`.
  - `Matric_Represent_Area` referencia outro `PROFESSOR`.

- **DEPARTAMENTO**
  - `Coordenador` referencia `PROFESSOR`.

- **PROJETO**
  - `Depto` referencia `DEPARTAMENTO`.

- **DEPENDENTE**
  - `MatricProf` referencia `PROFESSOR`.

- **EMAIL**
  - `MatricProf` referencia `PROFESSOR`.

---

Use esta estrutura para entender como as tabelas estão inter-relacionadas e para criar consultas conforme necessário. Se precisar de ajuda com as consultas específicas ou com qualquer outra coisa, estou aqui para ajudar!
