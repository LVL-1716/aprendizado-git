# Boas Práticas para Uso do Git e GitHub

## 1. Escreva Mensagens de Commit Claras e Descritivas

Sempre adicione mensagens de commit que expliquem **o que** foi alterado e **por que**. Evite mensagens genéricas como "ajustes" ou "correções". 

**Exemplo:**
```
git commit -m "Adiciona validação de email no formulário de cadastro"
```

## 2. Organize e Nomeie Branches de Forma Consistente

Use nomes descritivos para branches que indiquem claramente o propósito da mudança. Boas convenções incluem:
- `feature/nome-da-funcionalidade` - para novas funcionalidades
- `bugfix/descricao-do-bug` - para correção de bugs
- `hotfix/descricao-do-problema` - para correções urgentes em produção

**Exemplo:**
```
git checkout -b feature/adicionar-login
```

## 3. Faça Commits Pequenos e Frequentes

Commits pequenos e focados facilitam a revisão de código e tornam mais fácil identificar quando e onde um bug foi introduzido. Cada commit deve representar uma unidade lógica de mudança.

**Dica:** Se você precisa usar "e" na mensagem de commit, provavelmente deveria ser dois commits separados.

## 4. Sempre Faça Pull Antes de Push

Antes de enviar suas alterações para o repositório remoto, sempre puxe as últimas alterações para evitar conflitos:

```
git pull origin main
git push origin sua-branch
```

## 5. Use .gitignore para Evitar Arquivos Desnecessários

Mantenha seu repositório limpo evitando commits de arquivos temporários, dependências, ou configurações locais. Crie um arquivo `.gitignore` apropriado para seu projeto.

**Exemplo de .gitignore:**
```
node_modules/
.env
*.log
.DS_Store
```

## 6. Revise Seu Código Antes de Fazer Commit

Use `git diff` para revisar suas alterações antes de fazer commit. Isso ajuda a evitar commits acidentais de código de debug ou alterações não intencionais.

```
git diff
git add -p  # permite adicionar mudanças de forma interativa
```
