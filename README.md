# 📱 Mobile - App de Gerenciamento de Produtos

Aplicativo móvel desenvolvido com **React Native** e **Expo** para gerenciamento de estoque. O app realiza operações completas de CRUD (Criar, Ler, Atualizar, Deletar) consumindo uma API Backend local.

## 🚀 Tecnologias Utilizadas

- **[React Native](https://reactnative.dev/)**: Framework para desenvolvimento híbrido.
- **[Expo](https://expo.dev/)**: Plataforma para facilitar a criação, build e teste de apps React Native.
- **[Axios](https://axios-http.com/)**: Cliente HTTP para realizar as requisições à API.

---

## ⚠️ Configuração Obrigatória (Antes de Rodar)

Para que o aplicativo no seu celular consiga se comunicar com o backend rodando no seu computador, **é necessário configurar o endereço IP**. O celular não entende `localhost` como sendo o seu computador.

1. **Descubra seu IP Local (IPv4):**
   - **Windows:** Abra o terminal e digite `ipconfig`.
   - **Mac/Linux:** Abra o terminal e digite `ifconfig` ou `ip a`.
   - Copie o endereço IPv4 (ex: `192.168.0.15` ou `192.168.1.10`).

2. **Configure no Código:**
   - Abra o arquivo `App.js` na raiz do projeto.
   - Localize a constante `API_URL` (logo no início do arquivo).
   - Substitua o IP pelo número que você copiou:

   ```javascript
   // ❌ Errado para celular físico:
   // const API_URL = 'http://localhost:3000/produtos';

   // ✅ Correto (Exemplo):
   const API_URL = '[http://192.168.0.15:3000/produtos](http://192.168.0.15:3000/produtos)';


   Verifique a Rede:

Certifique-se de que o seu celular e o seu computador estão conectados na mesma rede Wi-Fi.

📦 Como rodar o projeto
# 1. Instalação das Dependências
Abra o terminal na pasta do projeto e execute:

Bash

npm install


# 2. Executando o App
Inicie o servidor de desenvolvimento do Expo:

Bash

npx expo start
# 3. Abrindo no Celular
Após rodar o comando acima, um QR Code aparecerá no terminal.

Android:

Instale o app Expo Go na Play Store.

Abra o app e toque em "Scan QR Code".

Aponte a câmera para o terminal.

iOS (iPhone):

Instale o app Expo Go na App Store.

Abra o aplicativo de Câmera nativo do iPhone.

Aponte para o QR Code e toque na notificação para abrir no Expo Go.

🛠 Funcionalidades
O aplicativo possui uma tela única intuitiva com as seguintes funções:

Listagem: Carrega automaticamente todos os produtos cadastrados ao abrir.

Cadastro: Permite inserir Nome e Preço para criar um novo registro.

Edição: Ao clicar em "Editar", os campos são preenchidos e o botão muda para "Atualizar".

Exclusão: Ao clicar em "Excluir", uma confirmação é solicitada antes de remover o item.

Feedback Visual: Indicadores de carregamento (loading) e alertas nativos de sucesso ou erro.

❓ Solução de Problemas Comuns
Erro: "Network request failed" ou "Não foi possível conectar ao backend"

Verifique se o Backend está rodando (npm run dev na pasta do backend).

Verifique se o IP no App.js está correto. O IP da máquina pode mudar se você reiniciar o roteador.

Desative temporariamente o Firewall do Windows para testar se ele está bloqueando a porta 3000.

Garanta que ambos os dispositivos (PC e Celular) estão no mesmo Wi-Fi.

📝 Estrutura do Projeto
Plaintext

/projeto-mobile
├── assets/             # Ícones e imagens do Expo
├── node_modules/       # Dependências (não versionado)
├── .gitignore          # Arquivos ignorados pelo Git
├── App.js              # Código principal da aplicação
├── app.json            # Configurações do Expo
├── package.json        # Lista de dependências e scripts
└── README.md           # Documentação
