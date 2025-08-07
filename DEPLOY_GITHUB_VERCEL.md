# 🚀 Deploy via GitHub + Vercel

## 📋 Passo a Passo Completo

### 1️⃣ **Criar Repositório no GitHub**

1. Acesse [github.com](https://github.com) e faça login
2. Clique em **"New repository"** (botão verde)
3. Configure:
   - **Repository name**: `dashboard-eventos-forum`
   - **Description**: `Dashboard de Inteligência - Análise de Eventos 2024 vs 2025`
   - ✅ **Public** (recomendado para Vercel gratuito)
   - ❌ **NÃO** marque "Add a README file"
   - ❌ **NÃO** adicione .gitignore (já criamos)
4. Clique em **"Create repository"**

### 2️⃣ **Subir Código para o GitHub**

Abra o **Terminal** na pasta do projeto e execute:

```bash
# Inicializar repositório Git
git init

# Adicionar todos os arquivos
git add .

# Fazer primeiro commit
git commit -m "🎉 Dashboard de Inteligência - Análise de Eventos 2024 vs 2025"

# Adicionar repositório remoto (SUBSTITUA pelo SEU usuário)
git remote add origin https://github.com/SEU_USUARIO/dashboard-eventos-forum.git

# Enviar para o GitHub
git push -u origin main
```

**⚠️ IMPORTANTE:** Substitua `SEU_USUARIO` pelo seu nome de usuário do GitHub!

### 3️⃣ **Conectar GitHub com Vercel**

1. Acesse [vercel.com](https://vercel.com)
2. Clique em **"New Project"**
3. Selecione **"Import Git Repository"**
4. **Autorize** a Vercel a acessar seu GitHub
5. Encontre o repositório `dashboard-eventos-forum`
6. Clique em **"Import"**

### 4️⃣ **Configurar Deploy**

A Vercel detectará automaticamente:
- ✅ **Framework Preset**: Other
- ✅ **Root Directory**: `./`
- ✅ **Build Command**: (vazio - site estático)
- ✅ **Output Directory**: `./`

**Clique em "Deploy"** e aguarde!

## 🎯 **Resultado Final**

Após o deploy, você receberá:
- 🔗 **URL de produção**: `https://dashboard-eventos-forum.vercel.app`
- 🔄 **Deploy automático**: Toda vez que fizer push no GitHub
- 📊 **Dashboard completo** pronto para usar

## 🔄 **Atualizações Futuras**

Para atualizar o dashboard:

```bash
# Fazer alterações nos arquivos
# Depois:
git add .
git commit -m "📈 Atualização do dashboard"
git push
```

A Vercel fará deploy automático! 🚀

## 📁 **Estrutura do Projeto**

```
dashboard-eventos-forum/
├── index.html          # Dashboard principal
├── vercel.json         # Configuração Vercel
├── .gitignore         # Arquivos ignorados
├── DEPLOY_VERCEL.md   # Instruções originais
└── README.md          # Documentação
```

## 🆘 **Problemas Comuns**

### **Erro de autenticação Git:**
```bash
# Configure seu Git (primeira vez)
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### **Repositório já existe:**
```bash
# Se já criou o repo, apenas:
git remote add origin https://github.com/SEU_USUARIO/dashboard-eventos-forum.git
git push -u origin main
```

### **Branch main vs master:**
```bash
# Se usar master:
git branch -M main
git push -u origin main
```

---

**🎉 Pronto! Seu dashboard estará online e acessível para toda sua equipe!**