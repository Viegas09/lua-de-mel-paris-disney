# 🚀 Passo a Passo: Subir no GitHub e GitHub Pages

## ⚡ RESUMO RÁPIDO (5 MINUTOS)

Se você já tem GitHub instalado, é só:
```bash
git init
git add .
git commit -m "Lua de Mel Paris & Disney"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/lua-de-mel-paris-disney.git
git push -u origin main
```

Depois ativar GitHub Pages nas configurações do repositório.

---

## 📋 PASSO A PASSO COMPLETO

### PASSO 1: Criar Conta no GitHub (Se não tiver)

1. Abra https://github.com
2. Clique em **"Sign up"** (canto superior direito)
3. Preencha:
   - Email
   - Senha
   - Username (será usado na URL: github.com/SEU-USERNAME)
4. Confirme no email
5. Pronto! Você tem conta

---

### PASSO 2: Baixar Git no Seu Computador

**Windows:**
1. Acesse https://git-scm.com
2. Clique em **"Download for Windows"**
3. Abra o instalador
4. Clique "Next" em tudo (configuração padrão está ótima)
5. Termine a instalação

**Mac:**
1. Instale Homebrew (se não tiver):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. Instale Git:
   ```bash
   brew install git
   ```

**Linux:**
```bash
sudo apt install git
```

**Verificar se instalou corretamente:**
- Abra Terminal/Prompt de Comando
- Digite: `git --version`
- Deve mostrar versão (ex: `git version 2.36.0`)

---

### PASSO 3: Configurar Git Localmente

Abra Terminal/Prompt de Comando e digite:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@gmail.com"
```

Exemplo:
```bash
git config --global user.name "Vinicius Santana"
git config --global user.email "vinicius@example.com"
```

---

### PASSO 4: Criar Repositório no GitHub

1. Acesse https://github.com
2. No canto superior direito, clique no **"+"** (símbolo de mais)
3. Selecione **"New repository"**
4. Preencha:
   - **Repository name**: `lua-de-mel-paris-disney`
   - **Description**: `App para organizar lua de mel em Paris & Disney`
   - **Public** (deixe selecionado)
   - **NÃO selecione** "Add a README file" (você já tem)
5. Clique **"Create repository"**

**Pronto! Você tem um repositório vazio no GitHub**

---

### PASSO 5: Preparar Pasta No Seu Computador

1. **Crie uma pasta no seu computador:**
   - Crie pasta: `lua-de-mel-paris-disney`
   - Exemplo: `C:\Users\Seu Usuário\Documents\lua-de-mel-paris-disney`

2. **Coloque seus arquivos lá:**
   - `index.html` (seu app)
   - `README.md`
   - `PASSO_A_PASSO_GITHUB.md`
   - `.gitignore` (vou criar abaixo)
   - `LICENSE` (opcional)

---

### PASSO 6: Criar .gitignore (Arquivo de Configuração)

1. Abra **Bloco de Notas** (Notepad)
2. Copie e cole isto:
```
# Arquivos do sistema
.DS_Store
Thumbs.db

# IDEs
.vscode
.idea
*.code-workspace

# Node (se usar no futuro)
node_modules/
package-lock.json

# Logs
*.log
npm-debug.log*
```

3. Salve como `.gitignore` (sem extensão .txt!)
   - **Importante**: Na hora de salvar, escolha tipo **"Todos os arquivos"** e escreva `.gitignore`

4. Coloque na pasta `lua-de-mel-paris-disney`

---

### PASSO 7: Abrir Terminal na Pasta

**Windows:**
1. Abra a pasta `lua-de-mel-paris-disney`
2. Aperte **Ctrl + L** (barra de endereço)
3. Digite **`cmd`** e aperte Enter
4. Terminal abre na pasta certa

**Mac/Linux:**
1. Abra Terminal
2. Digite: `cd ~/Documents/lua-de-mel-paris-disney`
3. (Ajuste o caminho para seu local)

---

### PASSO 8: Inicializar Git Localmente

No terminal (na pasta lua-de-mel-paris-disney), execute:

```bash
git init
```

Resultado esperado:
```
Initialized empty Git repository in C:\Users\...\lua-de-mel-paris-disney\.git
```

---

### PASSO 9: Adicionar Arquivos

```bash
git add .
```

Isto adiciona TODOS os arquivos da pasta.

**Verificar se funcionou:**
```bash
git status
```

Deve mostrar algo como:
```
On branch master
Changes to be committed:
  new file:   index.html
  new file:   README.md
  ...
```

---

### PASSO 10: Fazer Commit (Guardar Alterações)

```bash
git commit -m "Lua de Mel Paris & Disney - App completo"
```

Resultado:
```
[master (root-commit) a1b2c3d] Lua de Mel Paris & Disney - App completo
 4 files changed, 1500 insertions(+)
 ...
```

---

### PASSO 11: Conectar ao GitHub

Você vai precisar do link do seu repositório. Volta no GitHub:

1. Acesse seu repositório (deve estar vazio)
2. Clique no botão verde **"Code"** (topo direito)
3. Copie o link HTTPS (algo como: `https://github.com/SEU-USUARIO/lua-de-mel-paris-disney.git`)

No terminal, execute:

```bash
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/lua-de-mel-paris-disney.git
```

**Substitua `SEU-USUARIO` pelo seu username no GitHub!**

---

### PASSO 12: Fazer Upload (Push) para GitHub

```bash
git push -u origin main
```

**Primeira vez pode pedir autenticação:**

**Opção A: Token (Mais Seguro - RECOMENDADO)**

1. Abra https://github.com/settings/tokens
2. Clique **"Generate new token"** → **"Generate new token (classic)"**
3. Na seção **"Select scopes"**, marque:
   - ☑️ `repo` (acesso ao repositório)
4. Clique **"Generate token"** (no final da página)
5. **Copie o token** (você só vê uma vez!)
6. Na janela do terminal que pediu autenticação:
   - Login: Seu username do GitHub
   - Password: Cole o token aqui
7. Aperte Enter
8. Pronto! Upload feito!

**Opção B: SSH (Mais Técnico)**
Se você já usa SSH no GitHub, pode usar isso também (não vou detalhar aqui).

---

### PASSO 13: Verificar Upload no GitHub

1. Acesse seu repositório: `https://github.com/SEU-USUARIO/lua-de-mel-paris-disney`
2. Deve aparecer seus arquivos:
   - ✅ index.html
   - ✅ README.md
   - ✅ PASSO_A_PASSO_GITHUB.md
   - ✅ .gitignore

---

### PASSO 14: Ativar GitHub Pages (Para Acessar Online)

**Agora vem o melhor! Seu app vai ficar online gratuitamente!**

1. Abra seu repositório no GitHub
2. Clique em **"Settings"** (engrenagem, topo direito)
3. No menu esquerdo, clique **"Pages"**
4. Em **"Source"**, selecione:
   - Branch: **main**
   - Folder: **/ (root)**
5. Clique **"Save"**

**Aguarde alguns segundos...**

Vai aparecer uma mensagem verde:
```
Your site is published at https://seu-usuario.github.io/lua-de-mel-paris-disney
```

---

### PASSO 15: Acessar Seu App Online! 🎉

1. Abra o link: `https://seu-usuario.github.io/lua-de-mel-paris-disney`
2. Seu app está ONLINE!
3. Funciona em qualquer dispositivo
4. Compartilhe com seu amor! 💕

---

## ✅ CHECKLIST FINAL

- ✅ Conta GitHub criada
- ✅ Git instalado no computador
- ✅ Repositório criado no GitHub
- ✅ Arquivos na pasta localmente
- ✅ Git inicializado (`git init`)
- ✅ Arquivos adicionados (`git add .`)
- ✅ Commit feito (`git commit`)
- ✅ Conectado ao GitHub (`git remote add origin`)
- ✅ Push feito (`git push`)
- ✅ GitHub Pages ativado
- ✅ App online! 🎉

---

## 🆘 Erros Comuns e Soluções

### Erro: "git não é reconhecido"
**Solução**: Git não foi instalado ou não foi adicionado ao PATH. Reinstale Git.

### Erro: "fatal: 'origin' does not appear to be a 'git' repository"
**Solução**: Você mudou de pasta. Execute `git status` para confirmar que está na pasta certa.

### Erro: "Authentication failed"
**Solução**: Token/senha incorreta. Gere novo token no GitHub e tente novamente.

### GitHub Pages não funcionando
**Solução**: 
1. Aguarde 1-2 minutos após ativar
2. Limpe cache do navegador (Ctrl+Shift+Delete)
3. Verifique se está em "main" branch, não "master"

### Quero fazer alterações no futuro
```bash
# Faça as alterações nos arquivos
git add .
git commit -m "Descrição das alterações"
git push
```

---

## 📚 Referências Rápidas

**Git Comandos Importantes:**
```bash
git status          # Ver status dos arquivos
git log             # Ver histórico de commits
git diff            # Ver diferenças antes de commitar
git pull            # Atualizar repositório local
git branch          # Ver branches
```

**GitHub Pages:**
- Documentação: https://pages.github.com
- Ajuda: https://docs.github.com/en/pages

---

## 💡 DICAS BÔNUS

### 1. Criar Atalho para Adicionar Mudanças Rápido
```bash
git add . && git commit -m "Atualização" && git push
```

### 2. Mudar Descrição do Repositório Depois
1. Abra seu repositório
2. Clique **"Settings"**
3. Edite "Description"
4. Pronto!

### 3. Adicionar Imagem/Screenshot no README
```markdown
![App Screenshot](https://seu-site.com/imagem.png)
```

### 4. Compartilhar com Seu Amor
- Link da página: `https://seu-usuario.github.io/lua-de-mel-paris-disney`
- Link do repositório: `https://github.com/seu-usuario/lua-de-mel-paris-disney`
- Ele/ela pode fazer download clicando em "Code" → "Download ZIP"

---

## 🎉 PRONTO!

Seu app está online e funcionando! 

**Próximas ações:**
1. ✅ Compartilhe com seu amor 💕
2. ✅ Use durante a viagem
3. ✅ Atualize com fotos/memórias quando voltar
4. ✅ Mostre para amigos!

---

**Boa viagem! 🇫🇷✨**

*Dúvidas? Procure ajuda em:*
- GitHub Help: https://docs.github.com
- Stack Overflow: https://stackoverflow.com
- Google: "seu erro aqui + github"

