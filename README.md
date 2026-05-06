🤖 Auto About: Editor Visual & Bot WhatsApp (TCC)
Este repositório contém o código-fonte do meu Trabalho de Conclusão de Curso (TCC). O projeto consiste em um ecossistema completo para criação, gerenciamento e execução de chatbots para WhatsApp, unindo um Editor de Fluxo Visual "no-code" com o poder da IA Generativa (Google Gemini).

🏗️ Arquitetura do Sistema
O projeto é dividido em três pilares fundamentais que trabalham em sincronia:

Frontend (Editor de Fluxo): Interface React baseada em nós para desenhar a lógica de conversação.

Backend (Servidor de Sincronização): API Express que traduz o gráfico visual em um arquivo de dados persistente.

WhatsApp Bot (Motor de Conversa): O executor que utiliza whatsapp-web.js para processar mensagens em tempo real.

🚀 Funcionalidades Detalhadas
Editor Drag-and-Drop: Interface intuitiva para criar fluxos complexos sem escrever código.

Nós Customizados:

Nó de Entrada: Define o gatilho inicial.

Nó de Mensagem: Envia textos pré-definidos.

Nó de IA: Consulta o Gemini para processar intenções do usuário.

Gestão de Estado: O sistema armazena o histórico e a posição atual de cada número de telefone no fluxo.

Integração com Gemini 1.5 Flash: Modelo de baixa latência para respostas inteligentes e naturais.

🛠️ Tecnologias Utilizadas
Core: Node.js & Vite

Interface Visual: React & @xyflow/react (Antigo React Flow)

Backend: Express & Cors

Comunicação WhatsApp: whatsapp-web.js

Inteligência Artificial: Google Generative AI SDK

🔧 Instalação e Execução
1. Pré-requisitos
Node.js (v18 ou superior)

NPM ou Yarn

Uma conta no Google AI Studio para obter a chave da API.

2. Clonagem e Dependências
Bash
# Clone o repositório
git clone https://github.com/daviferreira-dev/TCC.git

# Entre na pasta do projeto
cd TCC

# Instale todas as dependências
npm install
3. Variáveis de Ambiente
Crie um arquivo .env na raiz do projeto:

Snippet de código
GEMINI_API_KEY=seu_token_aqui
PORT=3001
4. Execução em Modo de Desenvolvimento
Você precisará de dois terminais:

Terminal 1: Backend & Bot

Bash
node server.js
Aguarde o QR Code aparecer no terminal e escaneie com seu WhatsApp (Configurações > Aparelhos Conectados).

Terminal 2: Frontend (Editor)

Bash
npm run dev
Acesse http://localhost:5173.

📖 Como Usar o Editor
Crie Nós: Clique com o botão direito ou use o menu lateral para adicionar blocos de mensagem.

Conecte: Ligue a saída de um bloco à entrada de outro para definir a sequência.

Configure: Clique no nó para definir o texto que o bot deve enviar ou a instrução de IA.

Salve: Clique no botão "Salvar Fluxo". O arquivo flow.json será atualizado automaticamente no servidor e o bot passará a responder com a nova lógica instantaneamente.

⚠️ Troubleshooting (Solução de Problemas)
Erro no Puppeteer/Chromium: O whatsapp-web.js utiliza um navegador em segundo plano. Se der erro de inicialização no Linux, instale as dependências: sudo apt install libatk-bridge2.0-0 libgtk-3-0.

QR Code não carrega: Verifique sua conexão com a internet e se a porta 3001 não está ocupada.

IA não responde: Verifique se sua GEMINI_API_KEY é válida e se você não atingiu o limite de requisições gratuitas.

📄 Licença
Este projeto é de fins acadêmicos e está sob a licença MIT.
