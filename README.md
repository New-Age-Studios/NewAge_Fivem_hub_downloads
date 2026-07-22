# NewAge Fivem Hub - Downloads API

Este repositório serve como um "banco de dados" externo e estático para o aplicativo **NewAge Fivem Hub**.

## 📌 Para que serve?

O objetivo principal deste repositório é hospedar o arquivo `downloads.json`. 
Em vez de ter os mods, scripts e mapas "presos" dentro do código do aplicativo (o que exigiria que os usuários baixassem uma nova versão do `.exe` toda vez que você quisesse adicionar um novo download), o aplicativo agora se conecta a este repositório toda vez que é aberto.

Isso significa que **qualquer alteração feita neste repositório será refletida imediatamente em todos os aplicativos** instalados pelos seus usuários, sem necessidade de atualizações de software!

## 🚀 Como adicionar um novo Download

Para adicionar um novo mod na Central de Downloads do app, siga os passos abaixo:

1. Abra o arquivo `downloads.json`.
2. Adicione um novo objeto na lista, seguindo exatamente este padrão:

```json
  {
    "id": 3,
    "name": "Nome do Seu Mod ou Script",
    "version": "v1.0.0",
    "downloaded": false,
    "thumbnail": "LINK_DE_UMA_IMAGEM_HOSPEDADA_NA_INTERNET",
    "description": "Descrição detalhada sobre o que este mod faz e porque ele é útil.",
    "installGuide": [
      { "type": "text", "content": "1. Baixe o arquivo..." },
      { "type": "text", "content": "2. Adicione 'ensure script' no server.cfg" }
    ]
  }
```

3. Salve o arquivo e faça o `commit/push` para o GitHub.
4. Abra o **NewAge Fivem Hub**, e o seu novo mod já estará disponível na aba "Central de Downloads"!

## ⚠️ Regras Importantes
- **NÃO** mude o nome do arquivo `downloads.json`, caso contrário o aplicativo perderá a conexão.
- O link da `thumbnail` deve ser uma imagem válida e direta (ex: `.png`, `.jpg`).
- Para novos IDs, tente manter a ordem crescente (1, 2, 3, 4, 5...).
