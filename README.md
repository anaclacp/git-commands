# ✨ Guia Completo de Comandos Git

<div align="center">
Um guia prático e completo para seus projetos com Git
</div>

## 📌 Índice
- [Comandos Básicos](#-comandos-básicos)
- [Branches](#-trabalhando-com-branches)
- [Repositório Remoto](#-repositório-remoto)
- [Desfazendo Alterações](#-desfazendo-alterações)
- [Boas Práticas](#-boas-práticas)
- [Situações Comuns](#-situações-comuns)

## 🌸 Comandos Básicos

### Iniciando um Repositório
```bash
git init
```

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

## 🌿 Trabalhando com Branches

### Gerenciamento de Branches
```bash
# Listar branches
git branch

# Criar novo branch
git branch nome-do-branch

# Trocar de branch
git checkout nome-do-branch

# Criar e trocar de branch em um comando
git checkout -b nome-do-branch

# Deletar branch
git branch -d nome-do-branch
```

### Merge e Rebase
```bash
# Fazer merge de outro branch
git merge nome-do-branch

# Fazer rebase
git rebase nome-do-branch
```

## 🚀 Repositório Remoto

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

## ↩️ Desfazendo Alterações

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

## 💡 Boas Práticas

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

## 🔍 Situações Comuns

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

## 📝 Arquivo .gitignore

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

---

<div align="center">

**Dúvidas?**
Consulte a [documentação oficial do Git](https://git-scm.com/doc) ou abra uma issue!

*Feito com ♥️ para a comunidade dev*

</div>
