# Setup Profissional do N8N Local com Docker

Este repositório apresenta um guia completo para configurar um ambiente local do **N8N** utilizando Docker, integrando também **Postgres**, **Redis**, **Waha** e **Cloudflare**. O objetivo é proporcionar um setup robusto, seguro e escalável, ideal tanto para estudos quanto para ambientes profissionais.

---

## 🚀 Visão Geral

Você aprenderá a:

- Registrar um domínio próprio
- Configurar o domínio na Cloudflare
- Preparar o ambiente Docker com todos os serviços necessários
- Garantir segurança e praticidade no acesso ao seu N8N

---

## 📋 Passo a Passo

### 1. Registre um Domínio

**Por que usar um domínio próprio?**

- Permite um setup mais profissional, mesmo para estudos.
- Evita limitações de serviços gratuitos como Ngrok (que possui limites de uso e pode interromper seus testes).
- Usar Cloudflare sem domínio próprio deixa o acesso público e pode gerar alertas de segurança nos navegadores.

**Dica:** Domínios baratos podem ser adquiridos na [Hostinger](https://hostinger.com.br?REFERRALCODE=kendylopes). Exemplo: `kendylopes.fun` por menos de $8.

---

### 2. Configure seu Domínio na Cloudflare

- Crie uma conta gratuita na [Cloudflare](https://dash.cloudflare.com/).
- Adicione seu domínio seguindo o passo a passo da plataforma.

**Tutorial recomendado:**  
[Como configurar Cloudflare para seu domínio (YouTube)](https://www.youtube.com/watch?v=dW_G-C3OyVQ&t=901s)  
> ⚠️ O vídeo mostra um setup diferente, mas a configuração da Cloudflare é a mesma. Siga até a parte em que o N8N já está funcionando no domínio.

---

### 3. Instale o Docker

Baixe e instale o Docker Desktop em sua máquina:  
[Download Docker Desktop](https://www.docker.com/products/docker-desktop/)

---

### 4. Estruture o Projeto

- Crie uma pasta chamada `n8n` (exemplo: `C:\n8n`).
- Abra a pasta no [Visual Studio Code](https://code.visualstudio.com/) para facilitar a edição dos arquivos.
- Crie seu arquivo `.env` baseado no `example.env` fornecido.

**Exemplo de variáveis no `.env`:**
```env
TIMEZONE=America/Sao_Paulo
POSTGRES_PASSWORD=<sua_senha_segura>
N8N_ENCRYPTION_KEY=<sua_chave_segura>
WAHA_API_KEY=<sua_api_key_segura>
```
> 🔒 Utilize um gerador de senhas para criar valores seguros para as variáveis acima.

---

### 5. Suba o Setup com Docker Compose

No terminal, execute:

```sh
docker compose up -d
```

Se ocorrer algum erro:

1. Pare os containers:
   ```sh
   docker compose down
   ```
2. Corrija o problema apontado.
3. Suba novamente:
   ```sh
   docker compose up -d
   ```

> 💡 Se precisar de ajuda, consulte a documentação oficial ou utilize assistentes de IA.

---

### 6. Acesse seu N8N

Se tudo estiver correto, seu N8N estará disponível no seu domínio configurado, por exemplo:  
`https://n8n.seudominio.fun`

Você pode utilizar qualquer extensão de domínio: `.fun`, `.com`, `.site`, `.tech`, etc.

---

## 📝 Observações Finais

- Sempre utilize senhas e chaves seguras.
- Mantenha seu Docker e dependências atualizados.
- Para dúvidas ou sugestões, abra uma issue neste repositório.

---

**Bons estudos e automações! 🚀**