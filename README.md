# Comida Para HomoSapiens

Site de vendas do ebook **Comida Para HomoSapiens — Guia de Nutrição Biológica 2025**.

## Estrutura de arquivos

```
/
├── index.html       → Landing page de vendas
├── obrigado.html    → Página pós-compra (thank you page)
├── ebook.html       → O ebook completo (acesso direto via /ebook)
├── vercel.json      → Configuração de rotas e headers
└── README.md        → Este arquivo
```

## URLs disponíveis

| URL | Arquivo | Descrição |
|-----|---------|-----------|
| `/` | `index.html` | Landing page principal |
| `/obrigado` | `obrigado.html` | Página de agradecimento pós-compra |
| `/ebook` | `ebook.html` | Ebook completo |

## Deploy no Vercel via GitHub

### 1. Crie o repositório no GitHub

```bash
git init
git add .
git commit -m "feat: launch comida para homo sapiens"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/comida-para-homo-sapiens.git
git push -u origin main
```

### 2. Conecte ao Vercel

1. Acesse [vercel.com](https://vercel.com) e faça login
2. Clique em **"Add New Project"**
3. Importe o repositório do GitHub
4. Deixe todas as configurações padrão — o `vercel.json` já cuida do resto
5. Clique em **"Deploy"**

O site estará no ar em menos de 1 minuto.

### 3. Domínio personalizado (opcional)

No painel do Vercel:
- Vá em **Settings → Domains**
- Adicione seu domínio (ex: `comidaparahomosapiens.com`)
- Siga as instruções para apontar o DNS

## Configuração do checkout

No arquivo `index.html`, localize o botão de compra e substitua `href="#"` pelo link do seu checkout:

```html
<!-- Linha ~240 do index.html -->
<a href="SEU_LINK_CHECKOUT_AQUI" class="btn-primary-lg">QUERO MEU EBOOK AGORA →</a>
```

Plataformas recomendadas: **Hotmart**, **Kiwify**, **Eduzz**, **Monetizze**.

### Configurar a página de obrigado na plataforma

Na sua plataforma de checkout, configure a URL de redirecionamento pós-compra para:

```
https://seudominio.com/obrigado
```

## Atualizações

Para atualizar o site, basta fazer um novo commit no GitHub — o Vercel faz o deploy automaticamente.

```bash
git add .
git commit -m "fix: atualiza copy do botão"
git push
```
