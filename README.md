# Traira's · Landing page

Landing page do **Traira's Restaurante e Eventos** (Patrocínio, MG), preparada pela V4 Company · Bandeira Serpa & Co.

Página estática (HTML, CSS e JavaScript puros), sem build e sem dependências. Basta subir os arquivos.

## Estrutura

```
index.html                   Landing page
politica-de-privacidade.html Modelo de política de privacidade (revisar antes de publicar)
assets/                      Logo, ícones, texturas, fotos dos pratos e fontes (assets/fonts)
favicon.ico                  Ícone da aba (mascote)
robots.txt                   Bloqueia indexação (versão de apresentação)
.nojekyll                    Faz o GitHub Pages servir os arquivos como estão
```

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub (pode ser privado se a conta tiver Pages em repositórios privados; senão, público).
2. Envie todos os arquivos desta pasta para a raiz do repositório, incluindo o `.nojekyll`.
   - Pelo navegador: **Add file → Upload files**, arraste o conteúdo da pasta e clique em **Commit changes**.
   - Pelo terminal:
     ```bash
     git init
     git add .
     git commit -m "LP Traira's: versão de apresentação"
     git branch -M main
     git remote add origin https://github.com/SEU-USUARIO/trairas-lp.git
     git push -u origin main
     ```
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**, branch **main**, pasta **/ (root)** e clique em **Save**.
5. Em 1 a 2 minutos o link fica disponível em `https://SEU-USUARIO.github.io/trairas-lp/`.

## Antes de ir para o domínio oficial

Esta é uma versão de **apresentação**. Quando for publicar em produção:

- [ ] Remover a linha `<meta name="robots" content="noindex, nofollow">` do `index.html` e apagar o `robots.txt`.
- [ ] Conferir o domínio em `canonical`, `og:url`, `og:image` e nos dados estruturados (hoje: `https://www.trairas.com.br/`).
- [ ] Colar o Google Tag Manager e o Pixel da Meta no espaço comentado do `<head>`. As tags de marketing devem disparar só após o evento `consentimento_aceito`.
- [ ] Completar a `politica-de-privacidade.html` (razão social, CNPJ, e-mail do encarregado) e revisar com o jurídico.
- [ ] Confirmar a licença web da Gotham e, se possível, enviar Gotham Book e Medium (hoje os pesos 400/600 usam Montserrat). A Erliana recebeu acentos do português feitos pela agência, pois o arquivo original não tinha.
- [ ] Trocar as fotos pelo banco de imagens profissional, mantendo os mesmos nomes de arquivo em `assets/`.

## Pontos para validar com a cliente

- Ofertas fixas da semana (prato individual, buffet de saladas, sobremesa grátis aos domingos).
- Descrições curtas dos pratos e acompanhamentos da parmegiana.
- Se drinks e prato individual estão disponíveis no Anota Aí.
- Data e link de ingressos do próximo Festival de Peixes.

## Eventos de rastreamento

`clique_cardapio`, `clique_prato`, `filtro_cardapio`, `clique_eventos`, `orcamento_evento`, `clique_festival`, `clique_como_chegar`, `clique_telefone`, `clique_whatsapp`, `clique_instagram`, `consentimento_aceito`.
