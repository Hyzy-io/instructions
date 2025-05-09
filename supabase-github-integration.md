
# 🚀 Guia: Conectando Supabase a um Repositório GitHub

Este guia documenta passo a passo como conectar um projeto Supabase a um repositório privado do GitHub, útil especialmente quando a integração automática falha ou o repositório não aparece.

---

## ✅ Pré-requisitos

- Conta no Supabase
- Repositório privado no GitHub (ex: `horizontes-conectados`)
- Permissão de **Admin** sobre o repositório no GitHub

---

## 🪜 Passo a passo

### 1. Acesse as integrações do Supabase
- Acesse o projeto no Supabase Studio
- Vá para: `Settings` → `Integrations` → **GitHub Connections**

### 2. Autorize o Supabase a acessar seu GitHub
- Clique em **“Authorize GitHub”**
- Se o repositório **não aparecer**, use o link direto:

  👉 [Instalar Supabase GitHub App](https://github.com/apps/supabase/installations/new)

### 3. Instale o Supabase como GitHub App
- Marque a opção **"All repositories"** ou selecione o repositório desejado
- Confirme a instalação

### 4. Volte ao Supabase Studio
- Recarregue a página do Supabase Studio
- Volte para: `Settings > Integrations > GitHub`
- Clique em **“Choose repository to connect to”**

### 5. Selecione o repositório e o projeto
- Escolha:
  - O projeto Supabase ativo
  - O repositório GitHub (ex: `nathaliabinsvoigt/horizontes-conectados`)
- Clique em **“Connect project”**

---

## ✅ O que acontece após conectar

- O Supabase criará uma pasta `/supabase/` no repositório
- Alterações no schema podem ser **commitadas automaticamente como migrations**
- Você pode usar o **Supabase CLI** para sincronização local

---

## 🔧 Comandos úteis com Supabase CLI

```bash
# Instale o CLI se necessário
npm install supabase -g

# Vincule o projeto local ao Supabase
npx supabase link --project-ref <PROJECT_ID>

# Puxe estrutura atual do banco
npx supabase db pull

# Envie alterações para o Supabase
npx supabase db push
```

---

Pronto! Agora seu projeto Supabase está integrado com seu repositório GitHub 🚀
