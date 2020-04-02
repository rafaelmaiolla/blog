---
title: Blog com Gatsby rodando no Netlify
date: "2020-04-02T21:45:23.412Z"
description: "Este é basicamente o primeiro post e eu vou escrever um pouco da minha experiência colocando um blog para rodar usando o Gatsby e Netlify."
---

Este é basicamente o primeiro post e eu vou escrever um pouco da minha experiência
colocando um blog para rodar usando o Gatsby e Netlify.

O que eu posso dizer é que foi muito rápido, em uma noite eu criei o repositório no Github, usei o `gatsby-starter-blog`,
fiz algumas alterações para o Português, adicionei alguns outro detalhes, conectei com o Netlify, apontei um subdomínio e
[https://rafael.maiolla.com](https://rafael.maiolla.com) estava disponível.

## Github

Como primeiro passo, criei um novo repositório no Github e é onde o código desse blog vai ficar disponível.
Você pode acessa-lo [aqui](https://github.com/rafaelmaiolla/rafael.maiolla.com).

## Gatsby

Se ainda não conhece o [Gatsby](https://www.gatsbyjs.org/), ele é um gerador de sites que usa React. Eu não vou entrar em detalhes,
já que a documentação é bem completa.

Se você já tem NodeJS instalado na sua máquina, basta instalar `gatsby` globalmente:

```bash
npm install -g gatsby
```

E então você dar bootstrap com o starter.

```bash
gatsby new gatsby-starter-blog https://github.com/gatsbyjs/gatsby-starter-blog
```

Então entre na pasta criada e rode:
```bash
gatsby develop
```

Você já pode acessar o seu blog localmente [http://localhost:8000/](http://localhost:8000/)

### Alterações

Como o `starter` é em Inglês, tive que fazer algumas poucas mudanças pra que visualmente ele ficasse
com cara ser escrito em Português.

Você pode conferir essas mudanças nesse [commit](https://github.com/rafaelmaiolla/rafael.maiolla.com/commit/d724c0ee84f3ab86c56c6ff3a46aaf537bc9573d).

Algumas observações:
* Imagino que ainda deve existir alguns outros pontos que precisam ser traduzidos, mas por enquanto parece que é tudo que preciso;
* Se você notar, os elementos de data não foram traduzidos, mas em vez de usar o nome dos meses, eu mudei para o número do mes;

## Netlify

Conheci essa plataforma junto com o Gatsby, [Netlify](https://www.netlify.com/) oferece hospedagem de site gratuitamente para projetos
pessoais e se integra facilmente com o Github.

A integração e o deploy foi muito fácil, basta criar uma conta, seguir o tutorial, conectar ela com a sua conta GitHub, escolher o repositório, o branch,
ele já vai reconhecer que o seu projeto usa Gatsby, mais alguns outros detalhes e pronto.

Seu site vai estar disponível em um subdomínio da netlify [https://rafaelmaiolla.netlify.com](https://rafaelmaiolla.netlify.com).

E a melhor parte é que o processo de build e deploy são feitos automaticamente pelo Netlify assim que ele identificar
alguma mudança no branch que você selecionou no Github.

## Subdomínio

Esse é um passo opcional, mas como eu já tenho um domínio próprio, criei uma entrada `CNAME` no meu provedor de domínio
apontando para a URL da Netlify.

Assim que esse subdomínio for propagado, que as vezes pode levar um tempo, você pode cadastrar ele como um domínio customizado
no Netlify que ele vai automaticamente gerar os certificados para o site.

Resumidamente, isso é tudo o que você precisa fazer pra ter o seu blog disponível.
