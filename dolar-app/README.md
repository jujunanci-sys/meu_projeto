# Dólar Hoje, Fácil

App simples para acompanhar o dólar americano (USD → BRL), pensado para quem não entende de finanças.

## Como usar

- **No computador:** abra o arquivo `index.html` no navegador (duplo clique).
- **No celular, como app:** o app precisa estar publicado num endereço `https`. Veja "Publicar no GitHub Pages" abaixo.

## Publicar no GitHub Pages

1. No GitHub, abra o repositório e vá em **Settings → Pages**.
2. Em **Source**, escolha **Deploy from a branch**.
3. Em **Branch**, escolha a branch com o app e a pasta **/ (root)**, e clique em **Save**.
4. Em um ou dois minutos o endereço aparece no topo da página, no formato
   `https://jujunanci-sys.github.io/meu_projeto/` (ele abre o app direto).

O GitHub Pages em repositório **privado** só funciona em planos pagos. No plano gratuito,
torne o repositório público (Settings → General → Danger Zone → Change visibility).

## Instalar no celular

- **Android (Chrome):** abra o endereço e use o menu ⋮ → **Instalar app** (ou **Adicionar à tela inicial**).
- **iPhone (Safari):** abra o endereço, toque em **Compartilhar** e depois em **Adicionar à Tela de Início**.

O ícone aparece junto com os outros apps e abre em tela cheia, sem a barra do navegador.

## O que ele faz

- **Preço ao vivo**: consulta a cotação a cada segundo e mostra se subiu ou caiu.
- **Termômetro de compra**: compara o preço de agora com os últimos 30 dias e diz, em linguagem simples,
  se é bom momento, preço normal ou caro.
- **Gráfico dos últimos 30 dias** com a média do mês.
- **Simulador**: digite quantos dólares quer e veja quanto custa em reais.
- **Meus preços salvos**: o botão "Salvar este preço" guarda o valor e a data/hora. A tabela mostra se hoje
  está mais caro ou mais barato que naquele dia. Os dados ficam salvos no próprio navegador.

## Observações

- Fonte dos dados: [AwesomeAPI](https://docs.awesomeapi.com.br/) (cotação comercial), com reserva na Frankfurter.
  O app pergunta a cada segundo, mas a fonte só muda o valor de tempos em tempos.
- O preço em casas de câmbio e no cartão costuma ser maior (taxas e IOF).
- É um app informativo, não é recomendação de investimento.
