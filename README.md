# 🤖 Auto About: Editor Visual & Bot WhatsApp (TCC)

Este repositório contém o código-fonte do meu Trabalho de Conclusão de Curso (TCC). O projeto consiste em um ecossistema completo para criação, gerenciamento e execução de chatbots para WhatsApp, unindo um **Editor de Fluxo Visual** "no-code" com o poder da **IA Generativa (Google Gemini)**.

---

## 🏗️ Arquitetura do Sistema

O projeto é dividido em três pilares fundamentais que trabalham em sincronia:

1.  **Frontend (Editor de Fluxo):** Uma interface desenvolvida em React que permite desenhar a árvore de decisão do bot visualmente através de nós e conexões.
2.  **Backend (Servidor de Sincronização):** Uma API Node.js/Express que recebe a estrutura do fluxo e a armazena em um arquivo JSON persistente.
3.  **WhatsApp Bot (Motor de Conversa):** O cérebro que interpreta o fluxo salvo e interage com os usuários reais no WhatsApp, utilizando IA para conversas não estruturadas.

---

## 🚀 Funcionalidades Principais

*   **Editor Drag-and-Drop:** Criação intuitiva de blocos de conversa com múltiplos handles de saída.
*   **Gestão de Estado Dinâmica:** O bot rastreia individualmente em qual etapa do fluxo cada usuário se encontra.
*   **Híbrido IA/Fluxo:** O bot prioriza o fluxo estruturado (keywords), mas utiliza o **Google Gemini** como fallback para responder perguntas livres de forma natural.
*   **Persistência Instantânea:** O fluxo é salvo no servidor e atualizado no bot sem necessidade de reinicialização do motor.

---

## 🛠️ Tecnologias Utilizadas

*   **Core:** [Node.js](https://nodejs.org/) & [Vite](https://vitejs.dev/)
*   **Interface Visual:** [React](https://reactjs.org/) & [@xyflow/react](https://reactflow.dev/)
*   **Backend:** [Express](https://expressjs.com/) & [Cors](https://www.npmjs.com/package/cors)
*   **Comunicação:** [whatsapp-web.js](https://wwebjs.dev/)
*   **Inteligência Artificial:** [Google Generative AI (Gemini 1.5 Flash)](https://ai.google.dev/)

---

## 🔧 Instalação e Execução

### 1. Preparação do Ambiente
```bash
# Clone o repositório
git clone [https://github.com/daviferreira-dev/TCC.git](https://github.com/daviferreira-dev/TCC.git)

# Instale as dependências gerais
npm install express cors body-parser whatsapp-web.js qrcode-terminal @google/generative-ai node-fetch @xyflow/react
