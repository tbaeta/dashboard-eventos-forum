# Extrator de Participantes do Looker Studio

Este projeto contém scripts para extrair dados de participantes de um evento do Looker Studio e gerar um arquivo CSV com todos os 36.659 participantes.

## 📋 Arquivos Incluídos

- `extract_participants.py` - Script principal usando Selenium (automação de navegador)
- `extract_participants_simple.py` - Script alternativo mais simples
- `requirements.txt` - Dependências Python necessárias
- `README.md` - Este arquivo de instruções

## 🚀 Instalação

### 1. Instalar Python
Certifique-se de ter Python 3.8+ instalado no seu sistema.

### 2. Instalar Dependências
```bash
pip install -r requirements.txt
```

### 3. Instalar ChromeDriver
O Selenium precisa do ChromeDriver para funcionar:

**macOS (usando Homebrew):**
```bash
brew install chromedriver
```

**Ou baixe manualmente:**
1. Vá para https://chromedriver.chromium.org/
2. Baixe a versão compatível com seu Chrome
3. Adicione ao PATH do sistema

## 📊 Como Usar

### Método 1: Script Selenium (Recomendado)

```bash
python extract_participants.py
```

**Processo:**
1. O Chrome abrirá automaticamente
2. Faça login no Google se necessário
3. Aguarde a página do Looker Studio carregar
4. Pressione Enter quando solicitado
5. O script navegará automaticamente por todas as páginas
6. Um arquivo `participantes_evento.csv` será gerado

### Método 2: Script Simples

```bash
python extract_participants_simple.py
```

Este script tentará acessar diretamente a API do Looker Studio e fornecerá instruções para extração manual se necessário.

## 🔧 Solução de Problemas

### Problema: "ChromeDriver not found"
**Solução:** Instale o ChromeDriver conforme instruções acima.

### Problema: "Login required"
**Solução:** 
1. Faça login manualmente no Google quando o navegador abrir
2. Navegue até a página do relatório
3. Pressione Enter no terminal

### Problema: "Tabela não encontrada"
**Solução:**
1. Verifique se a página carregou completamente
2. Tente aguardar mais tempo antes de pressionar Enter
3. Use o método manual descrito abaixo

## 📝 Método Manual (Alternativo)

Se os scripts automáticos não funcionarem:

### Opção 1: Export Nativo do Looker Studio
1. Abra o link no navegador
2. Procure por botão "Exportar" ou "Download"
3. Selecione formato CSV
4. Configure para exportar todos os dados

### Opção 2: Developer Tools
1. Abra o link no Chrome
2. Pressione F12 (Developer Tools)
3. Vá para aba "Network"
4. Navegue pelas páginas da tabela
5. Procure requisições que retornam dados JSON
6. Copie os dados e converta para CSV

### Opção 3: Copy/Paste Manual
1. Selecione os dados da tabela (Ctrl+A)
2. Copie (Ctrl+C)
3. Cole em uma planilha (Excel/Google Sheets)
4. Exporte como CSV

## 📁 Estrutura dos Dados

O arquivo CSV gerado conterá colunas como:
- ID do Participante
- Nome
- Email
- Data de Inscrição
- Status
- Categoria
- Origem

*Nota: As colunas exatas dependem da estrutura do relatório no Looker Studio.*

## ⚠️ Limitações

- O Looker Studio pode ter proteções contra automação
- Pode ser necessário fazer login manualmente
- A estrutura da página pode mudar, exigindo ajustes no script
- Rate limiting pode afetar a velocidade de extração

## 🆘 Suporte

Se encontrar problemas:
1. Verifique se todas as dependências estão instaladas
2. Certifique-se de ter acesso ao relatório do Looker Studio
3. Tente o método manual como alternativa
4. Verifique se o Chrome está atualizado

## 📊 Informações do Projeto

- **URL do Relatório:** https://lookerstudio.google.com/u/1/reporting/01bf8f2f-71f3-4126-b907-d6021e8b8487/page/p_8ut6oqt8rd?pli=1
- **Total de Participantes:** 36.659
- **Paginação:** 20 participantes por página
- **Total de Páginas:** ~1.833 páginas

---

**Dica:** Comece sempre com o `extract_participants.py` pois ele oferece a melhor chance de sucesso automático.