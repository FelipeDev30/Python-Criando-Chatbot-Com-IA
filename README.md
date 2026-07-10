# 🤖 ChatBot com IA (Gemini 3.5 Flash & Streamlit)

Este é um projeto de Chatbot inteligente desenvolvido em **Python** utilizando **Streamlit** para a interface gráfica e o novíssimo SDK **Google GenAI** integrado com o modelo **Gemini 3.5 Flash**. 

O projeto foi originalmente concebido durante a **Imersão de Inteligência Artificial da Hashtag Treinamentos** (originalmente planejado com OpenAI/GPT-4o) e posteriormente aprimorado e adaptado para consumir a API do Gemini de forma nativa e segura.

---

## 🚀 Funcionalidades

- **Interface Moderna e Fluida**: Construído com o Streamlit, o chatbot possui um visual limpo e adaptado para chat de conversação em tempo real.
- **Histórico de Conversas (Memória)**: O chatbot mantém o contexto da conversa utilizando o gerenciamento de estados (`st.session_state`), enviando o histórico completo para a API em cada interação.
- **Integração com Gemini**: Respostas rápidas e precisas utilizando o modelo `gemini-3.5-flash` por meio do SDK de última geração da Google.
- **Segurança de Credenciais**: As chaves de API são gerenciadas através do mecanismo nativo de segredos do Streamlit e devidamente protegidas contra commit acidental via `.gitignore`.

---

## 🛠️ Tecnologias Utilizadas

- [Python 3.12](https://www.python.org/)
- [Streamlit](https://streamlit.io/)
- [Google GenAI SDK](https://github.com/googleapis/python-genai) (Modelo `gemini-3.5-flash`)

---

## ⚙️ Instalação e Execução

### 1. Clonar o repositório
```bash
git clone https://github.com/FelipeDev30/Python-Criando-Chatbot-Com-IA.git
cd Python-Criando-Chatbot-Com-IA
```

### 2. Instalar as dependências
Certifique-se de ter as bibliotecas `streamlit` e `google-genai` instaladas:
```bash
pip install streamlit google-genai
```

### 3. Configurar sua chave de API
Crie um diretório chamado `.streamlit` na raiz do projeto (se ainda não existir) e adicione um arquivo `secrets.toml`:

```toml
# .streamlit/secrets.toml
[general]
GEMINI_API_KEY = "SUA_CHAVE_DE_API_AQUI"
```

> ⚠️ **Atenção:** O arquivo `secrets.toml` está listado no `.gitignore` para garantir que sua chave privada não seja enviada acidentalmente ao GitHub.

### 4. Executar o Chatbot
Inicie a aplicação localmente rodando:
```bash
streamlit run main.py
```

A aplicação abrirá automaticamente no seu navegador padrão (geralmente em `http://localhost:8501`).

---

## 🔒 Segurança

Este repositório possui uma configuração estrita no arquivo `.gitignore` para proteger dados sensíveis. Arquivos de configuração de ambiente de desenvolvimento local (como `.vscode/`), caches do Python (`__pycache__/`) e, principalmente, as credenciais da API (`.streamlit/secrets.toml`) não são rastreados pelo Git, garantindo boas práticas de segurança cibernética.

---
Feito com 💙 por [Felipe Lamas](https://github.com/FelipeDev30)
