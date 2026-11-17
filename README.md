# 📚 Plataforma: Onde Estudo? — Back-end

![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Contexto](https://img.shields.io/badge/Contexto-Projeto%20Pessoal-blueviolet)
![Status](https://img.shields.io/badge/Status-Em%20andamento-yellow)

API da plataforma **Onde Estudo?**, um projeto pessoal inspirado na experiência da W3Schools, mas voltado ao ensino brasileiro e alinhado à **BNCC**. Este repositório concentra a camada de Back-end: autenticação, modelagem do conteúdo escolar e endpoints para o [Front-end](https://github.com/OndeJoaoGularte/OndeEstudo-Frontend).

---

## 🎯 Objetivo do Projeto

Expor uma API REST para organizar e servir o conteúdo de estudos em uma hierarquia clara (matérias → séries → unidades → aulas), com autenticação de usuários e base para progresso, feedback e gestão administrativa, permitindo evoluir a plataforma com regras de negócio bem definidas no servidor.

---

## 🚀 Funcionalidades

1. **Autenticação:** Registro e login de usuários com senha criptografada e emissão de JWT.
2. **CRUD de conteúdo:** Endpoints para matérias, séries, unidades e aulas.
3. **Rotas protegidas:** Middleware de autenticação nas operações de criação, edição e exclusão.
4. **Dashboard admin:** Endpoint de estatísticas para a área administrativa.
5. **Modelo de domínio educacional:** Estrutura pensada para blocos de conteúdo (texto, vídeo, quiz, recursos), progresso do aluno, matrículas em matérias e feedbacks de aulas.

---

## 🛠️ Tecnologias Utilizadas

* **Node.js + Express:** Runtime e framework HTTP para a API REST.
* **TypeScript:** Tipagem estática em controllers, services e entities.
* **TypeORM:** ORM para mapeamento das entidades e persistência no banco.
* **PostgreSQL:** Banco relacional para o conteúdo e os usuários.
* **JWT + bcrypt:** Autenticação via token e hash de senhas.
* **CORS + dotenv:** Liberação de origem para o front e configuração por variáveis de ambiente.

---

## 🧠 Conceitos Aplicados

* **Arquitetura em camadas:** Separação entre `routes`, `controllers`, `services`, `entities` e `middlewares`.
* **ORM e relacionamentos:** Modelagem com TypeORM (`OneToMany`, `ManyToOne`, cascade) refletindo a hierarquia do conteúdo.
* **Autenticação stateless:** Login com JWT e validação via middleware nas rotas sensíveis.
* **Segurança básica de credenciais:** Hash de senha com bcrypt e exclusão do campo `password` nas respostas.
* **API REST:** Endpoints organizados por recurso (`/subjects`, `/grades`, `/units`, `/lessons`, `/register`, `/login`).
