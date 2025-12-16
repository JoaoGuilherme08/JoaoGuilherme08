# 🔧 Como Configurar o GitHub Metrics

Este guia explica como configurar as métricas avançadas do seu perfil.

## 📋 Passo 1: Criar um Personal Access Token (PAT)

1. Vá para [GitHub Settings > Developer Settings > Personal Access Tokens > Tokens (classic)](https://github.com/settings/tokens)

2. Clique em **"Generate new token (classic)"**

3. Configure o token:
   - **Note**: `METRICS_TOKEN`
   - **Expiration**: Escolha "No expiration" ou um período longo
   - **Scopes** (marque estas opções):
     - ✅ `repo` (Full control of private repositories)
     - ✅ `read:user` (Read ALL user profile data)
     - ✅ `read:project` (Read access to projects)
     - ✅ `user` (Update ALL user data) - opcional, para métricas extras

4. Clique em **"Generate token"**

5. **COPIE O TOKEN** (você só verá ele uma vez!)

## 📋 Passo 2: Adicionar o Token como Secret no Repositório

1. Vá para o seu repositório `JoaoGuilherme08`

2. Acesse **Settings** > **Secrets and variables** > **Actions**

3. Clique em **"New repository secret"**

4. Configure:
   - **Name**: `METRICS_TOKEN`
   - **Secret**: Cole o token que você copiou

5. Clique em **"Add secret"**

## 📋 Passo 3: Executar os Workflows

1. Vá para a aba **Actions** do seu repositório

2. Você verá dois workflows:
   - **Generate Metrics**
   - **Generate Snake Animation**

3. Para cada um, clique em **"Run workflow"** > **"Run workflow"**

4. Aguarde alguns minutos para os SVGs serem gerados

## ✅ Pronto!

Após a execução, as métricas serão geradas automaticamente:
- A cada 6 horas (metrics)
- A cada 12 horas (snake)
- Em cada push para a branch main

## 🎨 O que cada métrica mostra

| Métrica | Descrição |
|---------|-----------|
| **Isometric Calendar** | Calendário 3D das suas contribuições |
| **Achievements** | Conquistas estilo gaming baseadas na sua atividade |
| **Languages** | Análise profunda das linguagens que você usa |
| **Code Snippets** | Trechos de código recentes dos seus commits |
| **Coding Habits** | Seus hábitos de programação (horários, dias, etc) |
| **Stargazers** | Evolução das stars nos seus repositórios |

## 🐛 Troubleshooting

Se algo não funcionar:

1. Verifique se o token tem as permissões corretas
2. Verifique se o secret `METRICS_TOKEN` está configurado corretamente
3. Olhe os logs do workflow em **Actions** para ver erros específicos

---

**Dica**: Após configurar, delete este arquivo se quiser manter o repo limpo!

