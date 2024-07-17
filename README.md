## Smart Legal Contract NDA basato su Blockchain Ethereum

Questo progetto implementa un Accordo di Non Divulgazione (NDA) utilizzando un contratto intelligente sulla blockchain di Ethereum.

### Caratteristiche

- Implementazione sicura con due indirizzi predefiniti che rappresentano le "Parti"
- Solo le "Parti" possono visualizzare il testo dell'NDA visualizzabile in risorsa esterna allo Smart Contract
- Meccanismo di firma digitale per entrambe le "Parti" per accettazione dell'NDA
- Funzionalità di accesso a seconda risorsa esterna (es. login piattaforma) solo dopo che entrambe le "Parti" hanno firmato lo Smart Contract 

### Funzioni del Contratto Intelligente

- `accessUnseenResource()`: Condivide l'URL del documento NDA ai due address prima della firma
- `signNDA()`: Consente alle parti di "firmare l'NDA" firmando lo Smart Legal Contract
- `accessMainResource()`: Recupera l'URL per l'accesso alla piattaforma (2a risorsa)

### Utilizzo

1. Deploy dello smart contract con entrambi gli indirizzi delle "Parti"
2. Condividere l'URL del documento tramite `accessUnseenResource()`
3. Entrambe le parti firmano l'NDA utilizzando `signNDA()`
4. Accedere alla piattaforma (2a risorsa) utilizzando `accessMainResource()`

### Sicurezza

- Solo le "Parti" designate possono interagire con il contratto
- La condivisione dei documenti è bloccata fino a quando entrambe le "Parti" non firmano

### Requisiti

- Solidity ^0.8.0
- Blockchain compatibile con Ethereum (es. Ethereum mainnet, testnet, o blockchain compatibili)

### Licenza

MIT
