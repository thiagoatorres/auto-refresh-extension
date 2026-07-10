# Auto Refresh

Extensão de navegador que recarrega automaticamente a página atual em um intervalo definido pelo usuário.

## Funcionalidades

- Define o intervalo de atualização em segundos por aba.
- Cada aba tem seu próprio estado (ativo/inativo).
- Estado persiste mesmo se o navegador reiniciar o service worker da extensão.

## Instalação (modo desenvolvedor)

1. Abra `chrome://extensions` no Chrome (ou o equivalente no Edge/Brave).
2. Ative o **Modo do desenvolvedor**.
3. Clique em **Carregar sem compactação** e selecione a pasta do projeto.
4. Clique no ícone da extensão, defina o intervalo em segundos e clique em **Iniciar**.

## Estrutura do projeto

```
.
├── manifest.json     # Configuração da extensão
├── background.js     # Service worker: gerencia os alarmes e recarrega as abas
├── popup.html         # Interface do popup
├── popup.js           # Lógica do popup
└── icons/              # Ícones da extensão
```

## Limitações conhecidas

- O Chrome impõe um intervalo mínimo de ~30 segundos para alarmes periódicos em extensões publicadas.

## Licença

MIT
