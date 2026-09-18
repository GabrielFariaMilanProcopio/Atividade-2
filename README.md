# Atividade 2 - Autenticação com Cookies e JWT

## Objetivo

Desenvolver uma aplicação Web utilizando Node.js, Express, HTML, CSS, JavaScript Vanilla, fetch(), cookie-parser e JWT para compreender autenticação utilizando HTTP e cookies.

## Tecnologias utilizadas

- Node.js
- Express
- HTML
- CSS
- JavaScript Vanilla
- Fetch API
- cookie-parser
- jsonwebtoken

## Usuários para teste

### Ana

Login: ana

Senha: 123

### Carlos

Login: carlos

Senha: 456

## Funcionalidades

- Login de usuários
- Validação de login e senha
- Criação de cookie
- Consulta do usuário autenticado
- Logout
- Cookie HttpOnly
- SameSite
- Secure
- Autenticação utilizando JWT
- Middleware de autenticação
- Expiração do JWT em 30 minutos

## Questões para reflexão

### 1. O que é um cookie?

É um pequeno dado armazenado pelo navegador que pode ser utilizado para manter informações entre requisições HTTP.

### 2. Quem armazena o cookie: cliente ou servidor?

O servidor envia o cookie e o navegador, que é o cliente, armazena.

### 3. Quem envia o cookie nas próximas requisições?

O navegador envia automaticamente o cookie nas requisições correspondentes.

### 4. O que muda quando utilizamos HttpOnly?

O JavaScript da página não consegue acessar o cookie através de document.cookie.

### 5. Por que um cookie HttpOnly continua funcionando mesmo não aparecendo em document.cookie?

Porque o navegador continua enviando o cookie automaticamente nas requisições HTTP para o servidor.

### 6. Qual é a finalidade de Secure?

Fazer com que o cookie seja enviado somente através de conexões HTTPS.

### 7. Qual é a finalidade de SameSite?

Controlar o envio do cookie em requisições relacionadas a outros sites e ajudar na proteção contra CSRF.

### 8. Qual a diferença entre armazenar simplesmente um identificador de usuário e armazenar um JWT?

Um identificador simples apenas representa o usuário. Um JWT contém informações e uma assinatura que permite verificar sua autenticidade e pode possuir uma data de expiração.

### 9. O conteúdo de um JWT é secreto?

Não. O conteúdo de um JWT pode ser decodificado. A assinatura serve para verificar sua autenticidade. Informações secretas não devem ser colocadas no payload.

### 10. Por que armazenar um JWT em um cookie HttpOnly pode ser mais seguro do que disponibilizá-lo diretamente ao JavaScript?

Porque o JavaScript não consegue acessar diretamente o token através de document.cookie, reduzindo sua exposição a determinados ataques XSS.

## Evolução da atividade

A atividade foi desenvolvida seguindo a evolução:

Cookie simples
→ HttpOnly
→ SameSite
→ JWT
→ JWT + HttpOnly + Secure + SameSite

## Observação

As senhas foram armazenadas diretamente no código somente para fins didáticos. Em uma aplicação real, devem ser armazenadas utilizando técnicas adequadas de hash.

Durante o desenvolvimento local, Secure permanece false porque a aplicação utiliza HTTP.

Na versão publicada utilizando HTTPS, Secure deve ser true.