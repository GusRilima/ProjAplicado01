# Regras e Padrão de Branching

Este documento define o padrão de nomenclatura e fluxo de branches para garantir um desenvolvimento organizado e colaborativo.

---

## Fluxo de Trabalho (Git Flow)

Adotamos um fluxo baseado no **Git Flow**, onde as branches seguem uma estrutura padronizada para facilitar o versionamento e colaboração.  

As branches principais são:

- **`main`** → Versão estável do projeto. Apenas código testado e aprovado é mergeado aqui.
- **`develop`** → Branch de desenvolvimento. Contém código em progresso para a próxima release.

Outras branches seguem uma estrutura específica:

- **`feature/`** → Para novas funcionalidades.
- **`fix/`** → Para correções de bugs.
- **`hotfix/`** → Para correções urgentes na `main`.
- **`release/`** → Para preparar uma nova versão antes de ir para `main`.


---

## Regras de Nomeação:

- Use apenas caracteres alfanuméricos e hífens (-). 
- Sempre use letras minúsculas. 
- Separe palavras apenas com hífens (-). 
- Não use hífens consecutivos (--). 
- Não termine com hífen (-).  

---

## Exemplos de Branches:

| Tipo    | Nome da Branch                | Status                         |
|---------|--------------------------------|--------------------------------|
| Feature | `feature/autenticacao-google` | ✅ Correto                     |
| Fix     | `fix/corrigir-login-404`      | ✅ Correto                     |
| Hotfix  | `hotfix/ajuste-servidor`      | ✅ Correto                     |
| Feature | `feature/minhaFeature`        | ❌ Inválido (maiúsculas)       |
| Fix     | `fix/corrigir--bug`           | ❌ Inválido (hífens consecutivos) |
| Hotfix  | `hotfix/ajuste-servidor-`     | ❌ Inválido (hífen final)      |

---

## Padrão de Nomenclatura

Cada branch deve seguir um padrão específico para garantir clareza e organização.  

Estrutura:
```sh
[tipo]/[descrição-resumida]
```
---

## Criar uma branch
```sh
git checkout develop
git pull origin develop
git checkout -b feature/eda-mkt
```

---

## Desenvolver e commitar seguindo o padrão de commits
```sh
git commit -m "feat: Segmentação de clientes"
```

---

## Criar um Pull Request (PR)

- Antes de abrir um PR, garanta que a branch está atualizada.
- Faça um merge request para develop.
- Peça revisão para outro membro da equipe.

---

## Merge e Deploy

- Apenas após revisão e aprovação, o código será integrado ao develop.
- Quando estiver pronto para lançamento, será criada uma release/versão.
- A release será mergeada em main e develop, e uma tag será criada.