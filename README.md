# Nexus API

Projeto desenvolvido durante a disciplina **Automação e Testes em API**, com foco na execução de testes funcionais e implementação de uma pipeline de Integração Contínua (CI) utilizando **GitHub Actions**.

<img width="1235" height="507" alt="Image" src="https://github.com/user-attachments/assets/015b21b3-9a6f-4115-a8ed-6d46f74d2c02" />

---

## Objetivo do projeto

Este projeto demonstra a aplicação prática de conceitos de QA, Integração Contínua (CI), automação de testes, análise estática de código (SAST) e GitHub Actions, simulando um fluxo de desenvolvimento utilizado em ambientes DevOps.

---

## Sobre o projeto

A Nexus API simula uma aplicação de e-commerce, permitindo realizar operações de autenticação, cadastro de usuários, consulta de produtos e fluxo de checkout.

Durante a atividade foram executados testes funcionais (Smoke, Sanity e Regression), testes automatizados da API e a configuração de uma pipeline CI seguindo o conceito de **Fail Fast**.

---

## Tecnologias utilizadas

- Node.js
- Express.js
- Jest
- ESLint
- Git
- GitHub
- GitHub Actions
- Curl

---

## Estrutura do projeto

```text
nexus-api
│
├── src/
├── tests/
├── scripts/
├── .github/
│   └── workflows/
│       └── ci.yml
├── index.js
├── package.json
└── README.md
```

---

## Como executar

### 1. Clonar o projeto

```bash
git clone https://github.com/alexsabrasil/nexus-api.git
```

### 2. Acessar a pasta

```bash
cd nexus-api
```

### 3. Instalar as dependências

```bash
npm install
```

### 4. Executar a API

```bash
npm start
```

A API ficará disponível em:

```
http://localhost:3000
```

---

## Health Check

```http
GET /api/health
```

Resposta esperada:

```json
{
  "status": "UP",
  "message": "Nexus API is running"
}
```

---

## Produtos

```http
GET /api/products
```

Retorna a lista de produtos cadastrados.

---

# Testes

## Executar testes unitários

```bash
npm test
```

---

## Executar análise estática

```bash
npm run lint
```

---

## Pipeline CI

A pipeline foi implementada utilizando **GitHub Actions**.

Etapas executadas:

- ✅ SAST
- ✅ Build Validation
- ✅ Unit Tests
- ✅ Lint Quality
- ✅ API E2E Tests (Curl)

Fluxo da pipeline:

```text
Push
 │
 ▼
SAST
 │
 ▼
Build Validation
 │
 ▼
Unit Tests
 │
 ▼
Lint Quality
 │
 ▼
API E2E Tests
```

---

## ✅ Testes Funcionais Executados

Foram documentados seis cenários de teste:

- CT-001 – Login com credenciais válidas
- CT-002 – Cadastro de usuário
- CT-003 – Proteção contra força bruta
- CT-004 – Integração com pagamento PIX
- CT-005 – Validação dos dados do cartão
- CT-006 – Jornada completa de compra

---

## Documentação

O relatório técnico contém:

- Casos de teste
- Evidências
- Pipeline CI/CD
- Resultados obtidos

---

## Professor

**Bruno Álexy**

## Colaboradora

**Alexsandra Tavares**

Formação DevOps – FAP Softex Pernambuco

Julho/2026

## Projeto acadêmico

Este projeto foi desenvolvido como atividade prática da disciplina **Automação e Testes em API**, com o objetivo de aplicar conceitos de QA, Integração Contínua (CI), GitHub Actions e automação de testes em aplicações Node.js.
