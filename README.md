<div style="color: #FF69B4;">

# ✨ Guia Completo de Comandos Git

<div align="center" style="color: #DB7093;">
Um guia prático e completo para seus projetos com Git
</div>

## 📌 Índice
- [Comandos Básicos](#-comandos-básicos)
- [O que é um Branch?](#-o-que-é-um-branch)
- [Trabalhando com Branches](#-trabalhando-com-branches)
- [Repositório Remoto](#-repositório-remoto)
- [Desfazendo Alterações](#-desfazendo-alterações)
- [Boas Práticas](#-boas-práticas)
- [Situações Comuns](#-situações-comuns)

## 🌸 Comandos Básicos

### Iniciando um Repositório
```bash
git init
```

<div style="color: #FFB6C1;">

### Configurações Iniciais
```bash
# Configurar seu nome
git config --global user.name "Seu Nome"

# Configurar seu email
git config --global user.email "seu.email@exemplo.com"
```

### Adicionando Arquivos
```bash
# Adicionar todos os arquivos
git add .

# Adicionar arquivo específico
git add nome-do-arquivo

# Adicionar apenas arquivos de uma extensão
git add *.js
```

### Criando Commits
```bash
# Commit básico
git commit -m "Mensagem descritiva"

# Commit com descrição detalhada
git commit -m "Título do commit" -m "Descrição detalhada do commit"

# Adicionar e commitar em um comando
git commit -am "Mensagem"
```
</div>

## 🌿 O que é um Branch?

<div style="color: #DB7093;">

Um branch (ramificação) no Git é como uma linha alternativa de desenvolvimento que permite você trabalhar em diferentes versões do seu projeto ao mesmo tempo. É como ter "universos paralelos" do seu código, onde você pode:

- Desenvolver novas funcionalidades
- Corrigir bugs
- Testar ideias
- Tudo isso sem afetar o código principal!

### 📌 Exemplo Prático

Imagine que você tem um site funcionando (na branch `main`). Você precisa adicionar um novo formulário de contato. Em vez de mexer diretamente no site principal, você:

1. Cria uma nova branch chamada `feature/novo-formulario`
2. Trabalha no formulário tranquilamente
3. Testa tudo para garantir que está funcionando
4. Só depois junta (faz o merge) com o site principal

### 🔄 Branches Mais Comuns

- `main` ou `master`: Branch principal, código estável
- `feature/nome-da-funcionalidade`: Para novas funcionalidades
- `bugfix/nome-do-bug`: Para correções de problemas
- `hotfix/nome-do-problema`: Para correções urgentes
- `develop`: Branch de desenvolvimento (em alguns fluxos de trabalho)
</div>

## 🌿 Trabalhando com Branches

<div style="color: #FF69B4;">

### Gerenciamento de Branches
```bash
# Ver em qual branch você está
git branch

# Criar uma nova branch
git branch nome-da-branch

# Mudar para outra branch
git checkout nome-da-branch

# Criar e já mudar para a nova branch
git checkout -b nome-da-branch

# Deletar branch
git branch -d nome-da-branch
```

### Merge e Rebase
```bash
# Fazer merge de outro branch
git merge nome-do-branch

# Fazer rebase
git rebase nome-do-branch
```
</div>

## 🚀 Repositório Remoto

<div style="color: #DB7093;">

### Conectando e Enviando
```bash
# Adicionar repositório remoto
git remote add origin https://github.com/usuario/repositorio

# Enviar alterações
git push origin main

# Buscar alterações
git pull origin main

# Clonar repositório
git clone https://github.com/usuario/repositorio
```
</div>

## ↩️ Desfazendo Alterações

<div style="color: #FFB6C1;">

### Correções e Reversões
```bash
# Desfazer alterações em arquivo específico
git checkout -- nome-do-arquivo

# Desfazer último commit mantendo alterações
git reset --soft HEAD~1

# Desfazer último commit removendo alterações
git reset --hard HEAD~1

# Reverter um commit específico
git revert id-do-commit
```
</div>

## 💡 Boas Práticas

<div style="color: #FF69B4;">

### Commits
- Escreva mensagens claras e descritivas
- Use verbos no imperativo (Add, Update, Fix, Remove)
- Mantenha commits pequenos e focados
- Faça commits frequentes

### Branches
- Mantenha a main/master sempre estável
- Use branches para novas features
- Nomeie branches de forma descritiva
  - `feature/nova-funcionalidade`
  - `fix/correcao-bug`
  - `docs/atualizacao-readme`
</div>

## 🔍 Situações Comuns

<div style="color: #DB7093;">

### Verificando Status e Histórico
```bash
# Ver status atual
git status

# Ver histórico de commits
git log

# Ver histórico resumido
git log --oneline

# Ver alterações específicas
git diff
```

### Salvando Trabalho Temporário
```bash
# Guardar alterações temporárias
git stash

# Listar alterações guardadas
git stash list

# Recuperar alterações
git stash pop
```

### Resolvendo Conflitos
1. Identifique os arquivos com conflito usando `git status`
2. Abra os arquivos e procure por marcações de conflito
3. Escolha quais alterações manter
4. Adicione os arquivos resolvidos
5. Faça o commit das resoluções
</div>

## 📝 Arquivo .gitignore

<div style="color: #FFB6C1;">

Exemplo de conteúdo para `.gitignore`:
```plaintext
# Dependências
node_modules/
vendor/

# Arquivos de ambiente
.env
.env.local

# Arquivos de build
dist/
build/

# Logs
*.log

# Sistema operacional
.DS_Store
Thumbs.db
```
</div>

---

<div align="center" style="color: #FF69B4;">

**Dúvidas?**
Consulte a [documentação oficial do Git](https://git-scm.com/doc) ou abra uma issue!

*Para a comunidade dev*

</div>

</div>
