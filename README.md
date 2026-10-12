<div align="center">

# Germano Dev — Portfolio Pessoal

> Site de portfolio pessoal com painel admin dinâmico, banco de dados Firebase Realtime Database e deploy automático.

[![Deploy](https://img.shields.io/badge/Ver_ao_vivo-germanodev--portfolio.netlify.app-00C7B7?style=for-the-badge)](https://germanodev-portfolio.netlify.app/)
[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
[![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/pt-BR/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript)
[![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)](https://firebase.google.com)
[![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://netlify.com)

</div>

---

## Demo ao vivo

[germanodev-portfolio.netlify.app](https://germanodev-portfolio.netlify.app/)

---

## Sobre o Projeto

Portfolio pessoal desenvolvido do zero, sem frameworks, para apresentar projetos, habilidades e formas de contato de maneira profissional.

O diferencial deste portfolio é o painel administrativo integrado: projetos e cursos são gerenciados dinamicamente via banco de dados, sem precisar editar código para atualizar o conteúdo.

---

## Funcionalidades

| Funcionalidade | Descrição |
|--------|-----------|
| Hero Section | Apresentação com disponibilidade para novos projetos |
| Projetos Dinâmicos | Listagem de projetos com imagem, tags, descrição e link, gerenciados via admin |
| Cursos & Certificações | Lista de cursos adicionados dinamicamente pelo painel |
| Tech Skills | Exibição visual das tecnologias dominadas |
| IA & Ferramentas | Seção dedicada a ferramentas de IA utilizadas |
| Contato direto | Botões de WhatsApp e Instagram integrados |
| Painel Admin | Área protegida por senha para gerenciar projetos e cursos em tempo real |
| Responsivo | Layout adaptado para mobile, tablet e desktop |

---

## Tecnologias Utilizadas

| Tecnologia | Uso no Projeto |
|-----------|---------------|
| HTML5 | Estrutura semântica de toda a página |
| CSS3 | Estilização, animações, variáveis CSS e responsividade |
| JavaScript (Vanilla) | Lógica do painel admin, autenticação e manipulação do DOM |
| Firebase Realtime Database | Persistência do conteúdo editado no painel, acessada pela API REST do Firebase |
| localStorage | Cópia local do conteúdo, usada quando o banco está indisponível |
| Netlify e GitHub Pages | Hospedagem com deploy contínuo a partir deste repositório |

Vanilla JS foi uma escolha intencional para demonstrar domínio dos fundamentos do JavaScript sem depender de frameworks. A lógica de CRUD, autenticação e renderização dinâmica foi implementada manualmente.

---

## Estrutura do Projeto

```
portfolio-germano-dev/
├── index.html              # Aplicação completa (HTML + CSS + JS em um arquivo):
│                           # layout, estilos, painel admin e integração com o Firebase
├── cv.html                 # Currículo em página web
├── carta_apresentacao.html # Carta de apresentação
├── tabela_precos.html      # Tabela de preços de serviços
├── database.rules.json     # Regras de acesso do Firebase Realtime Database
├── assets/                 # Imagens
├── .github/workflows/      # Deploy no GitHub Pages
├── LICENSE
└── README.md
```

---

## Persistência (Firebase Realtime Database)

O conteúdo gerenciado pelo painel (projetos, cursos, skills e ferramentas) é salvo como um único documento JSON no Firebase Realtime Database, lido e gravado pela API REST com `fetch`, sem SDK.

Na carga da página, o site tenta buscar esse documento. Se o banco estiver indisponível, usa a cópia guardada no `localStorage` e, na falta dela, os dados padrão definidos no próprio `index.html`. Assim a página nunca fica vazia.

As regras de acesso ficam em `database.rules.json`.

---

## Como Rodar Localmente

```bash
git clone https://github.com/victor-germano/portfolio-germano-dev.git
cd portfolio-germano-dev
python -m http.server 8000
# abra http://localhost:8000
```

Para usar o seu próprio banco, crie um Realtime Database no [console do Firebase](https://console.firebase.google.com), publique as regras de `database.rules.json` e troque o valor de `FIREBASE_URL` no início do script em `index.html`.

---

## Deploy

O projeto está publicado no Netlify e no GitHub Pages ([victor-germano.github.io/portfolio-germano-dev](https://victor-germano.github.io/portfolio-germano-dev/)), ambos com deploy automático a partir deste repositório.

A cada `git push` na branch `main`, as duas hospedagens publicam a nova versão automaticamente, sem intervenção manual.

```
GitHub push → deploy automático → site atualizado
```

---

## Sobre o Desenvolvedor

**Victor Germano** — Estudante de Engenharia de Software (Universidade Cruzeiro do Sul) com foco em desenvolvimento web front-end e ferramentas de IA aplicadas.

[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=flat&logo=whatsapp&logoColor=white)](https://wa.me/5511953570476)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=flat&logo=instagram&logoColor=white)](https://instagram.com/v_.germano)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victor-germano-65787b2b1/)

---

## Licença

MIT License
