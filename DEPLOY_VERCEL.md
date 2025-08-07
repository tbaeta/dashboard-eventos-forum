# 🚀 Deploy do Dashboard na Vercel

## Opção 1: Deploy via Interface Web da Vercel (Recomendado)

### Passo a Passo:

1. **Acesse a Vercel**: Vá para [vercel.com](https://vercel.com) e faça login

2. **Novo Projeto**: Clique em "New Project" ou "Add New..."

3. **Import do Projeto**: 
   - Selecione "Import Git Repository"
   - Ou faça upload da pasta do projeto diretamente

4. **Configuração**:
   - Nome do projeto: `dashboard-eventos-forum`
   - Framework Preset: `Other`
   - Root Directory: `./`
   - Build Command: (deixe vazio)
   - Output Directory: `./`

5. **Deploy**: Clique em "Deploy"

## Opção 2: Deploy via Drag & Drop

1. Acesse [vercel.com/new](https://vercel.com/new)
2. Arraste a pasta do projeto para a área de upload
3. A Vercel detectará automaticamente que é um site estático
4. Clique em "Deploy"

## Opção 3: Via CLI (se conseguir instalar)

```bash
# Instalar Vercel CLI
npm install -g vercel

# Fazer login
vercel login

# Deploy
vercel --prod
```

## 📁 Arquivos Importantes

- `index.html` - Dashboard principal
- `vercel.json` - Configuração de deploy
- `.vercel/project.json` - Configuração do projeto

## 🔗 URL do Dashboard

Após o deploy, você receberá uma URL como:
`https://dashboard-eventos-forum.vercel.app`

## ✅ Funcionalidades do Dashboard

- ✅ Upload de arquivos Excel (.xls/.xlsx)
- ✅ Análise automática de dados 2024 vs 2025
- ✅ Métricas de participantes e retenção
- ✅ Gráficos interativos
- ✅ Insights automáticos
- ✅ Interface responsiva
- ✅ Processamento local (sem envio de dados)

## 📊 Como Usar

1. Acesse a URL do dashboard
2. Faça upload dos arquivos Excel (certifique-se que contenham "2024" e "2025" nos nomes)
3. Clique em "Analisar Dados"
4. Visualize as análises e insights gerados

## 🔒 Segurança

Todos os dados são processados localmente no navegador. Nenhuma informação é enviada para servidores externos.

---

**Pronto para compartilhar com sua equipe!** 🎉