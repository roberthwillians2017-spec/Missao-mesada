# Missão Mesada · como publicar

O pacote tem tudo pronto. Você só precisa criar o projeto no Firebase, colar a configuração e publicar.

## 1. Criar o projeto
1. Entre em https://console.firebase.google.com com a sua conta Google pessoal.
2. Clique em **Adicionar projeto**, dê o nome `missao-mesada` e desative o Google Analytics.
3. Anote o **ID do projeto** (aparece embaixo do nome, ex.: `missao-mesada-1a2b3`).

## 2. Criar o banco
1. No menu lateral: **Criação > Realtime Database > Criar banco de dados**.
2. Escolha o local sugerido e o **modo bloqueado**. As regras certas sobem junto na publicação.

## 3. Pegar a configuração
1. Clique na engrenagem > **Configurações do projeto**.
2. Em **Seus apps**, clique no ícone **</>** (Web), dê o nome `Missão Mesada` e registre. Não precisa marcar o Hosting aqui.
3. Copie o bloco `firebaseConfig`.
4. Abra `public/index.html`, procure **CONFIGURAÇÃO DO FIREBASE** e troque os `COLE_AQUI` pelos valores copiados.
5. Confira se o `databaseURL` está preenchido. Se não vier no bloco, copie o endereço que aparece no topo da tela do Realtime Database.

## 4. Publicar (uma vez no computador)
1. Instale o Node.js (https://nodejs.org), versão LTS.
2. Abra o terminal nesta pasta e rode:

```
npm install -g firebase-tools
firebase login
firebase deploy --project SEU-ID-DO-PROJETO
```

3. No fim aparece o link, no formato `https://SEU-ID-DO-PROJETO.web.app`.

Para atualizar depois, troque o `index.html` e rode só o `firebase deploy --project SEU-ID-DO-PROJETO`.

## 5. Virar app no celular
- **iPhone:** abra o link no Safari > Compartilhar > **Adicionar à Tela de Início**.
- **Android:** abra no Chrome > menu ⋮ > **Instalar app** (ou Adicionar à tela inicial).

Faça isso no seu celular, no da sua esposa e no do Junior.

## Como funciona o acesso
- Todos usam o mesmo link. Sem o PIN, a tela fica em modo jogador, só para ver.
- Para lançar, toque em **Sou pai ou mãe** e digite o PIN. O PIN que vocês criaram no Claude continua o mesmo.
- Tudo atualiza na hora nos três celulares. Sem internet, o lançamento fica guardado e sobe quando a conexão volta.

## Limite de segurança
O PIN protege a tela, não o banco. Quem tiver o link e conhecimento técnico consegue gravar direto no Firebase. Para uma família isso costuma bastar. Se um dia quiser fechar de vez, dá para trocar o PIN por login com e-mail e senha para pai e mãe.
