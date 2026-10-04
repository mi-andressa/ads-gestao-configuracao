# Changelog

Todas as mudanças relevantes deste projeto são documentadas neste arquivo.

O formato segue o [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/)
e o projeto adota o [Versionamento Semântico](https://semver.org/lang/pt-BR/).

## [1.0.0] - 2026-10-04

Funcionamento completo do sistema hipotético.

### Adicionado

- Página inicial do operador (`pg002.html`) com título "Operador" em verde e
  menu HOME, ATUALIZAÇÕES, RELATÓRIOS e SAIR (SAIR volta para `index.html`)
  (#19, fecha #7).
- Página de mensagem de erro (`msg.html`) com o texto "Preencher usuário" em
  vermelho e botão VOLTAR para `index.html` (#20, fecha #8).
- Este `CHANGELOG.md` (fecha #9).

### Alterado

- O login (`index.html`) passa a validar somente o campo usuário, após remover
  espaços nas pontas: vazio leva a `msg.html`, `admin` leva a `pg001.html` e
  qualquer outro valor leva a `pg002.html`. A comparação com `admin` é exata e
  diferencia maiúsculas de minúsculas. A senha não é validada (#21, fecha #6).

### Corrigido

- Pressionar ENTER no formulário de login não fazia nada; agora o login também
  é disparado pela tecla ENTER (#22).

## [0.2.0] - 2026-10-04

### Adicionado

- Página inicial do administrador (`pg001.html`) com título "Administrador" em
  azul e menu HOME, ATUALIZAÇÕES, RELATÓRIOS, CONFIGURAÇÃO, ADMINISTRAÇÃO e
  SAIR (#16, fecha #5).

### Alterado

- O botão ENTRAR do login passa a chamar `pg001.html`, ainda sem validação dos
  campos (#17, fecha #4).

## [0.1.0] - 2026-10-04

### Adicionado

- Página de login (`index.html`) com campos USUÁRIO e SENHA e botão ENTRAR
  (#12, fecha #2).
- Página de aviso "Em construção" (`working.html`) com botão VOLTAR, chamada
  pelo botão ENTRAR do login (#13, fecha #3).
- Workflow hipotético de release (`.github/workflows/release.yml`), acionado
  por tags `v*`, que empacota as páginas `.html` e usa este changelog como
  notas da versão (#14).
- README com integrantes, propósito e plano de releases.

[1.0.0]: https://github.com/mi-andressa/ads-gestao-configuracao/compare/v0.2.0...v1.0.0
[0.2.0]: https://github.com/mi-andressa/ads-gestao-configuracao/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/mi-andressa/ads-gestao-configuracao/releases/tag/v0.1.0
