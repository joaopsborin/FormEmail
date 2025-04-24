
# Formulário de Contato

Este projeto consiste em um formulário de contato simples, desenvolvido em HTML e estilizado com CSS inline. Ele permite que usuários enviem mensagens diretamente para um e-mail especificado, utilizando o serviço gratuito **FormSubmit**.

---

## 🚀 Como o formulário foi criado

1. **Estrutura HTML**  
   Criei um arquivo `.html` com a estrutura básica de um formulário contendo os seguintes campos:
   - Nome
   - E-mail
   - Telefone
   - Upload de Currículo (arquivo)
   - Mensagem

2. **Estilização**  
   Foi utilizado CSS inline diretamente nos elementos para simplificar o layout e garantir responsividade em dispositivos móveis, com `max-width` e margens automáticas.

---

## ✉️ Como o formulário ficou funcional (envio para e-mail)

1. **Integração com FormSubmit**  
   No atributo `action` da tag `<form>`, foi inserido o seguinte endereço:
   ```
   https://formsubmit.co/seu-email@exemplo.com
   ```
   No caso deste projeto:
   ```html
   <form action="https://formsubmit.co/paulo.r.silva125@aluno.senai.br" method="post">
   ```

2. **Configurações adicionais do FormSubmit:**
   - Redirecionamento após envio com o campo oculto `_next`:
     ```html
     <input type="hidden" name="_next" value="http://127.0.0.1:5500/thankyou.html">
     ```
   - Desabilitar CAPTCHA:
     ```html
     <input type="hidden" name="_captcha" value="false">
     ```

3. **Observações importantes:**
   - O e-mail precisa ser verificado na primeira vez que receber um formulário.
   - O serviço **não suporta envio de arquivos**, então o campo de currículo pode não funcionar corretamente (limitação do FormSubmit).

---

## 🧪 Teste Local

Você pode testar o formulário abrindo o arquivo `.html` diretamente no navegador.  
Para testar o redirecionamento corretamente, é recomendável utilizar uma extensão como "Live Server" no VS Code.

---

## 🧾 Comandos Git utilizados para criar e publicar o repositório no GitHub

```bash
# Inicializa o repositório Git local
git init

# Adiciona todos os arquivos ao controle de versão
git add .

# Cria um commit inicial
git commit -m "Versão inicial do formulário de contato"

# Cria o repositório remoto no GitHub e copia a URL (exemplo abaixo)
git remote add origin https://github.com/joaopsborin/FormEmail.git

# Define o branch principal como 'main'
git branch -M main

# Envia os arquivos para o GitHub
git push -u origin main
```

---

## ✅ Resultado Final

O formulário permite que qualquer pessoa entre em contato rapidamente, com um design limpo e responsivo, utilizando um serviço gratuito de envio de e-mails sem necessidade de backend.
