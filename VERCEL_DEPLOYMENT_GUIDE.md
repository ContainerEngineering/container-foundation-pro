# Container Foundation Pro - Vercel Deployment Guide

## ✅ Pré-requisitos

Você precisa ter:
- [ ] Conta no Vercel (você já tem)
- [ ] Conta no GitHub (crie em https://github.com/signup se não tiver)
- [ ] Git instalado no seu computador (https://git-scm.com/download)

---

## 📋 Passo a Passo Completo

### **PASSO 1: Criar Repositório no GitHub**

1. Acesse https://github.com/new
2. Preencha assim:
   - **Repository name**: `container-foundation-pro`
   - **Description**: `Professional foundation calculator for container homes`
   - **Visibility**: Escolha **Public** (necessário para Vercel grátis)
3. Clique em **Create repository**
4. **Copie a URL** do repositório (algo como `https://github.com/seu-usuario/container-foundation-pro.git`)

---

### **PASSO 2: Preparar o Código Localmente**

1. Abra o terminal/prompt de comando no seu computador
2. Navegue até a pasta do projeto:
   ```bash
   cd /home/ubuntu/container-foundation-saas
   ```
   *(Se você estiver no Windows, pode ser algo como `C:\Users\seu-usuario\container-foundation-saas`)*

3. Inicialize o Git:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Container Foundation Pro SaaS"
   ```

4. Conecte ao repositório do GitHub (substitua pela URL que você copiou):
   ```bash
   git branch -M main
   git remote add origin https://github.com/seu-usuario/container-foundation-pro.git
   git push -u origin main
   ```

   *Quando pedir login, use seu usuário e senha do GitHub (ou token de acesso)*

---

### **PASSO 3: Conectar Vercel ao GitHub**

1. Acesse https://vercel.com/dashboard
2. Clique em **Add New...** → **Project**
3. Clique em **Import Git Repository**
4. Cole a URL do seu repositório GitHub
5. Clique em **Continue**

---

### **PASSO 4: Configurar Variáveis de Ambiente no Vercel**

Antes de fazer o deploy, você precisa adicionar as variáveis de ambiente:

1. Na página de configuração do Vercel, procure por **Environment Variables**
2. Adicione estas variáveis (você pode deixar em branco por enquanto, pois o Vercel fornecerá):

   ```
   DATABASE_URL=
   JWT_SECRET=
   VITE_APP_ID=
   OAUTH_SERVER_URL=
   VITE_OAUTH_PORTAL_URL=
   OWNER_OPEN_ID=
   OWNER_NAME=
   BUILT_IN_FORGE_API_URL=
   BUILT_IN_FORGE_API_KEY=
   VITE_FRONTEND_FORGE_API_KEY=
   VITE_FRONTEND_FORGE_API_URL=
   ```

   **Importante**: Você pode deixar essas variáveis vazias por enquanto. O Vercel vai usar valores padrão.

3. Clique em **Deploy**

---

### **PASSO 5: Aguardar o Deploy**

1. O Vercel vai começar a compilar seu projeto
2. Você verá uma barra de progresso
3. Quando terminar, você receberá um **URL público** (algo como `https://container-foundation-pro.vercel.app`)

---

## 🎉 Pronto!

Seu site está online! Você pode:

1. **Acessar seu site**: Clique no link que o Vercel forneceu
2. **Compartilhar no Linktree**: Coloque o link na descrição do seu Linktree
3. **Compartilhar no YouTube**: Coloque o link na descrição dos seus vídeos

---

## 🔧 Se Algo Der Errado

### Erro: "Git not found"
- Instale Git em https://git-scm.com/download

### Erro: "Authentication failed"
- Use um **Personal Access Token** em vez de senha
- Crie em: https://github.com/settings/tokens
- Gere um novo token com permissão `repo`
- Use esse token como senha

### Erro: "Build failed"
- Verifique se todas as dependências foram instaladas
- Execute `pnpm install` antes de fazer o push

### Seu site está offline
- Verifique o status no dashboard do Vercel
- Clique em **Deployments** para ver logs de erro

---

## 📞 Próximos Passos

Após o deploy bem-sucedido:

1. **Teste a calculadora** no seu novo domínio
2. **Atualize seu Linktree** com o novo link
3. **Mencione nos vídeos do YouTube** que você tem uma calculadora profissional gratuita
4. **Monitore o tráfego** no Vercel Analytics

---

## 💡 Dicas

- **Domínio personalizado**: Depois, você pode comprar um domínio (tipo `containerengineeringcalculator.com`) e conectar ao Vercel
- **Atualizações**: Sempre que você fizer mudanças, faça `git push` e o Vercel vai atualizar automaticamente
- **Banco de dados**: Por enquanto, o banco de dados está local. Se precisar de um banco remoto, avise

---

**Pronto? Comece pelo PASSO 1!**
