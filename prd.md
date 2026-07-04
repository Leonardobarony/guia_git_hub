# PRD — README de Referência Diária Git

## Objetivo

Transformar o `README.md` deste repositório numa referência rápida e prática para uso diário com Git e GitHub, extraída do guia completo `git-guia-completo.md`.

---

## Problema

O `git-guia-completo.md` é completo mas longo demais para consulta rápida no dia a dia. Precisamos de um `README.md` que sirva como cola imediata: o desenvolvedor abre o repo, vê o que precisa e volta ao trabalho.

---

## Público-alvo

Desenvolvedor que já conhece Git mas precisa de um lembrete rápido dos comandos e do fluxo correto.

---

## Escopo do README

### Seções obrigatórias

| # | Seção | Justificativa |
|---|---|---|
| 1 | Fluxo diário (pull → add → commit → push) | Usado toda vez que se trabalha |
| 2 | Branches — criar, publicar, deletar | Fluxo mais comum depois do básico |
| 3 | Desfazer coisas — tabela por situação | Alta frequência de erro, precisa ser rápido |
| 4 | Stash — guardar trabalho sem commitar | Situação comum ao trocar de contexto |
| 5 | Padrão de mensagens de commit | Consistência no histórico |
| 6 | Emergência — tabela de socorro | Primeiro lugar que o dev olha quando algo vai mal |

### Seções excluídas (estão no guia completo)

- Configuração inicial (faz-se uma vez só)
- Tags
- Inspecionar histórico (git log / git diff) — seção secundária

---

## Critérios de sucesso

- Leitura em menos de 2 minutos
- Todos os comandos copiáveis sem adaptação
- Sem explicações longas — frases curtas ou tabelas
- Link para o guia completo ao final

---

## Entregável

`README.md` atualizado com as seções acima, em português, formato markdown limpo.
