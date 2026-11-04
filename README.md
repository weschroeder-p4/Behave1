# PV Behave — V.1

Página de vendas da Behave · https://behave.joaochesca.com.br/

## Configurações já aplicadas

- Botões antes da oferta (topo, dobras 1, 4, 5 e 8) rolam até a seção da oferta (`#oferta`).
- Botões da oferta, do convite final e do FAQ levam ao checkout: https://pay.hotmart.com/Y108166341M
- Meta Pixel: 1242073104404770 (dispara PageView). O token da API de Conversões (CAPI) vai no painel da Hotmart, nunca na página.
- Suporte: psicologojoaochesca@gmail.com
- Termos de uso (`termos.html`) e Política de privacidade (`privacidade.html`). Recomenda-se revisão jurídica.
- Microsoft Clarity: deixado comentado no `<head>`. Para ativar, troque `CLARITY_ID_AQUI` pelo ID e remova `<!--` e `-->`.

## Imagens

Todas as imagens da página estão em WebP (leves). As capas têm duas versões: `nome-400.webp` (mosaico/celular) e `nome.webp` (800px).

- `assets/joao-chesca.webp` — foto do João.
- Prints dos seguidores: já inseridos em `assets/prints/` (avatar e @ borrados). Para trocar, substitua os arquivos mantendo os nomes.

## Módulos "Em breve"

No carrossel, os módulos além de Fundamentos, Comportamento Verbal e Relacionamentos têm o selo "Em breve". Quando um módulo for publicado, apague o `<span class="selo-breve">Em breve</span>` dele.

## Estrutura

```
/ (raiz do repositório)
├── CNAME              behave.joaochesca.com.br
├── .nojekyll
├── index.html
├── termos.html / privacidade.html
├── robots.txt / sitemap.xml / site.webmanifest
├── favicon.ico, favicon-*.png, apple-touch-icon.png, android-chrome-*.png
├── og-image.jpg       prévia no WhatsApp/Instagram (1200x630)
└── assets/
    ├── logo-behave-*.webp / simbolo-behave-*.webp
    ├── joao-chesca.webp
    ├── area-membros-desktop.webp / area-membros-mobile.webp
    ├── prints/*.webp  (12 prints de seguidores)
    └── modulos/*.webp (16 capas, em 400px e 800px)
```

## Publicação (GitHub Pages + Cloudflare)

1. Criar repositório **público** no GitHub (ex.: `pv-behave`).
2. Add file → Upload files → arrastar **o conteúdo** desta pasta (não a pasta em si). O `.nojekyll` é oculto no Mac: `Cmd + Shift + .` no Finder para enxergá-lo.
3. Settings → Pages → Source: branch `main`, pasta `/ (root)` → Save.
4. Cloudflare → DNS do `joaochesca.com.br` → novo registro **CNAME**: nome `behave`, destino `SEU_USUARIO.github.io`, **DNS only (nuvem cinza)**.
5. GitHub → Settings → Pages → Custom domain: `behave.joaochesca.com.br` → aguardar "DNS check successful".
6. Marcar **Enforce HTTPS** quando liberar.
7. Validar: cadeado HTTPS, Meta Pixel Helper, prévia colando o link no WhatsApp, sessão no Clarity.

Para atualizar depois: subir o arquivo com o mesmo nome na mesma pasta — ele sobrescreve, não precisa apagar o antigo.
