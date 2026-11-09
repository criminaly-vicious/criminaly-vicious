# Installation instructions (pt-BR)

Este pacote foi preparado para o perfil `criminaly-vicious`.

## 1. Criar o repositório de perfil

No GitHub, crie um repositório **público** chamado `criminaly-vicious`, dentro da conta `criminaly-vicious`.
Ele precisa ficar em `github.com/criminaly-vicious/criminaly-vicious`.
O README na raiz será exibido automaticamente no perfil da conta.

## 2. Enviar os arquivos

Preserve exatamente a estrutura abaixo, incluindo a pasta oculta `.github`:

```text
criminaly-vicious/
├── README.md
├── assets/
│   └── profile-header.svg
└── .github/
    └── workflows/
        └── profile-3d.yml
```

`SETUP.md` é só para suas instruções e **não precisa subir**.

## 3. Habilitar e rodar a Action

No repositório de perfil, abra **Actions → GitHub Profile 3D Contributions → Run workflow**.

O workflow gera os SVGs de contribuição e os grava automaticamente no diretório
`profile-3d-contrib/`. O README mostra `profile-night-view.svg`.

A imagem 3D só aparece após a **primeira execução com sucesso** e o commit dos SVGs.
Depois disso, o workflow tenta atualizar diariamente às 03:17 (horário de São Paulo).

Se o workflow falhar ao fazer push, confira as configurações de Actions do repositório:
**Settings → Actions → General → Workflow permissions**, e se o token tem permissão de escrita
ou se há branch protection bloqueando o push.

## 4. Contribuições privadas (opcional)

Se quiser que o gráfico contabilize também a atividade privada que o GitHub permite mostrar,
abra seu perfil → Contribution settings e habilite a inclusão das contribuições privadas.
Isso não revela detalhes de repositórios privados, apenas contagens agregadas.
O comportamento exato do SVG depende da visibilidade e das permissões concedidas ao workflow.

## Notas

- A visualização é SVG isométrica/3D, não uma cena 3D interativa rotacionável.
- O autor da ferramenta é `yoshi389111/github-profile-3d-contrib`.
- Evite deixar credenciais ou dados pessoais sensíveis em um README público.
