# Git — Referência Rápida do Dia a Dia

Consulta rápida para o fluxo diário. Para explicações detalhadas, veja o [guia completo](git-guia-completo.md).

---

## Fluxo diário

```bash
git pull origin main          # 1. Sempre começa aqui
# ... edita arquivos ...
git status                    # 2. Veja o que mudou
git add .                     # 3. Manda pro stage
git commit -m "feat: ..."     # 4. Salva na história
git push origin main          # 5. Sobe pro GitHub
```

> Atalho para add + commit juntos (só arquivos já rastreados):
> `git commit -am "fix: correção rápida"`

---

## Branches

```bash
# Criar e trabalhar na branch
git checkout main
git pull origin main
git checkout -b feature/nome         # Cria e entra
# ... edita, add, commit ...
git push -u origin feature/nome      # Sobe pro GitHub

# Depois do merge no GitHub
git checkout main
git pull origin main
git branch -d feature/nome           # Limpa local
```

| Comando | O que faz |
|---|---|
| `git branch` | Lista branches locais |
| `git branch -a` | Lista todas (incluindo GitHub) |
| `git checkout main` | Volta pra main |
| `git merge feature/nome` | Mescla branch na atual |
| `git push origin --delete feature/nome` | Deleta no GitHub |

---

## Desfazer coisas

| Situação | Comando |
|---|---|
| Errei antes do `git add` | `git restore .` |
| Já fiz `git add`, não commitei | `git restore --staged .` |
| Commitei mas não subi | `git reset --soft HEAD~1` |
| Já fiz push | `git revert HEAD` + `git push` |

---

## Stash — guardar sem commitar

```bash
git stash               # Guarda o trabalho atual
git checkout outra-branch
# ... resolve o que precisava ...
git checkout feature/x
git stash pop           # Restaura onde parou
```

| Comando | O que faz |
|---|---|
| `git stash` | Guarda mudanças |
| `git stash list` | Lista stashes |
| `git stash pop` | Restaura o último |
| `git stash drop` | Descarta o último |

---

## Padrão de mensagens de commit

| Prefixo | Uso |
|---|---|
| `feat:` | Nova funcionalidade |
| `fix:` | Correção de bug |
| `docs:` | Documentação |
| `style:` | Formatação, sem mudança de lógica |
| `refactor:` | Refatoração de código |
| `test:` | Testes |
| `chore:` | Build, configs |

```bash
git commit -m "feat: adiciona autenticação OAuth"
git commit -m "fix: corrige erro no cálculo de datas"
```

---

## Emergência

| Situação | Comando |
|---|---|
| Errei antes do add | `git restore .` |
| Errei depois do add | `git restore --staged .` |
| Errei o commit (local) | `git reset --soft HEAD~1` |
| Errei o commit (já no GitHub) | `git revert HEAD` |
| Preciso trocar de branch sem commitar | `git stash` |
| Estou perdido | `git status` |

---

*Para detalhes completos: [git-guia-completo.md](git-guia-completo.md)*
