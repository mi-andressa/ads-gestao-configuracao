# ads-gestao-configuracao

Atividade da disciplina **Gestão de Projetos de Software** (IFSP, ADS): simular o
versionamento e as releases de uma miniaplicação web feita em HTML/JS puro, sem CSS,
praticando gestão de configuração (branches, Pull Requests, tags e changelog).

## Integrantes

- Victor Lis
- Andressa (completar nome completo)

## Páginas da aplicação

| Página | Descrição |
|---|---|
| `index.html` | Login: campo de usuário e botão de entrada. |
| `msg.html` | Mensagem de erro: "Preencher usuário" em vermelho e botão VOLTAR. |
| `pg001.html` | Página do administrador: menu HOME, ATUALIZAÇÕES, RELATÓRIOS, CONFIGURAÇÃO, ADMINISTRAÇÃO, SAIR; título "Administrador" em azul. |
| `pg002.html` | Página do operador: menu HOME, ATUALIZAÇÕES, RELATÓRIOS, SAIR; título "Operador" em verde. |

## Plano de releases

### v0.1.0
- `index.html` (login)
- `working.html` (aviso "em construção")

### v0.2.0
- Login chama `pg001.html` sem validar o usuário
- `pg001.html` (administrador)

### v1.0.0
- Funcionamento completo do login:
  - usuário vazio -> `msg.html`
  - usuário `admin` -> `pg001.html`
  - qualquer outro usuário -> `pg002.html`
- `pg002.html` e `msg.html`
- `CHANGELOG.md`

## Estratégia de branches

- `main`: código estável; recebe apenas releases e é marcada com tags.
- `develop`: integração; recebe as features e correções antes da release.
- `feature/*`: novas funcionalidades, criadas a partir de `develop`.
- `fix/*`: correções, criadas a partir de `develop`.

## Fluxo de trabalho

- Todo trabalho entra por Pull Request, com revisão de outro membro do grupo.
- Features e fixes são integradas em `develop`; ao fechar uma release, `develop` é integrada em `main`.
- Cada release é marcada com uma tag no formato `vX.Y.Z` (ex.: `v0.1.0`).
- Commits em português, no estilo Conventional Commits.
