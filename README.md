# RR TECNOL - Site Pronto para Deploy (Versão Atualizada)

## 📁 Estrutura dos Arquivos

```
rr-tecnol-site/
├── index.html              # Arquivo principal do site
├── logo-rr.png            # Logotipo principal (grande e visível)
├── logo.jpg               # Logotipo alternativo
├── assets/
│   ├── index-CRhZS5ZM.css # CSS do site (atualizado)
│   └── index-BTq1U_SO.js  # JavaScript do site (atualizado)
└── README.md              # Este arquivo
```

## 🚀 Como Fazer o Deploy

### Opção 1: Upload via FTP/SFTP (Recomendado)

1. Conecte ao seu servidor via FTP/SFTP
2. Faça upload de **todos os arquivos** para a raiz do seu domínio (geralmente `public_html` ou `www`)
3. Certifique-se de que o arquivo `index.html` está na raiz
4. Mantenha a pasta `assets/` no mesmo nível que `index.html`

### Opção 2: Upload via Painel de Controle (cPanel, Plesk, etc)

1. Acesse o gerenciador de arquivos do seu painel
2. Navegue até a pasta raiz do domínio
3. Faça upload de todos os arquivos mantendo a estrutura de pastas

### Opção 3: Descompactar no Servidor (via SSH)

```bash
tar -xzf rr-tecnol-deploy.tar.gz
cp -r dist/public/* /caminho/do/seu/dominio/
```

## ⚙️ Configurações Necessárias

### Servidor Web (Apache/Nginx)

**Para Apache (.htaccess):**
```apache
<IfModule mod_rewrite.c>
  RewriteEngine On
  RewriteBase /
  RewriteRule ^index\.html$ - [L]
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_FILENAME} !-d
  RewriteRule . /index.html [L]
</IfModule>
```

**Para Nginx:**
```nginx
location / {
  try_files $uri $uri/ /index.html;
}
```

## 📋 Checklist de Deploy

- [ ] Todos os arquivos foram enviados para o servidor
- [ ] A estrutura de pastas foi mantida (assets/ na mesma pasta que index.html)
- [ ] O arquivo index.html está acessível na raiz do domínio
- [ ] Os logotipos (logo-rr.png e logo.jpg) estão na raiz
- [ ] O servidor web está configurado para servir arquivos estáticos
- [ ] O domínio rrtecnol.com.br está apontando para o servidor correto
- [ ] Testou o site em navegador e todos os links funcionam

## 🔗 Links Importantes

- **WhatsApp da Empresa:** https://wa.me/559888956818
- **CNPJ:** 63.093.541/0001-21

## 📝 Alterações Recentes

- ✅ Logotipo aumentado e mais visível no canto superior esquerdo
- ✅ Links do WhatsApp integrados em todos os botões de contato
- ✅ Design responsivo e otimizado para mobile

## 📞 Suporte

Se tiver dúvidas sobre o deploy, entre em contato com seu provedor de hospedagem.

---

**Site gerado em:** 03/11/2025  
**Versão:** 2.0.0 (Atualizado com novo logotipo)
