# Mise en Place

App de treinamento do produto Takeat no estilo Duolingo (antigo TakeatHub Academy).
O app se chama **Mise en Place**; a **Mise** é a personagem (a ratinha chef, de *mice*), que também é a voz do app.

- **Web (PWA):** https://produto-takeat.github.io/mise/
- **Android e iOS:** [Releases](https://github.com/produto-takeat/mise/releases)

## Como publicar

O código do app vai em `projeto.zip` (fonte em `mise-src`). Cada push na `main` dispara:

| Workflow | Gera |
|---|---|
| `pages.yml` | o site (PWA) no GitHub Pages |
| `android.yml` | o APK de produção assinado (`mise-build-N.apk`), publicado como release `build-N` |
| `ios.yml` | o IPA de iOS **não assinado** (`mise-ios-build-N.ipa`), release `ios-build-N` |

O IPA sem assinatura instala no iPhone reassinado com um Apple ID (Sideloadly/AltStore, renovação a cada 7 dias).
Com a conta Apple Developer dá para assinar no workflow e distribuir pelo TestFlight.

As perguntas vêm do banco do TakeatHub (`mise_questoes`) e acompanham a wiki pela edge `mise-auto`.
