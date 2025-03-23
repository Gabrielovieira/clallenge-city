# Chatbot de Assistente Virtual

Este é um projeto de chatbot desenvolvido como parte de um projeto de assistente virtual. O chatbot utiliza a biblioteca LangChain para integrar com a API do Groq, permitindo uma interação natural e eficiente com o modelo de linguagem.

## Introdução

O projeto tem como objetivo criar um assistente virtual capaz de responder a perguntas relacionadas a informaçoes sobre cidades brasileiras. O chatbot é treinado com base em um modelo de linguagem pré-treinado (Gemma2-9b-It) e utiliza a API do Groq para processar as consultas de forma eficiente.

## Glossário

- **Groq**: É uma plataforma de dados sem servidor que permite realizar consultas avançadas em grandes volumes de dados.
- **LangChain**: É uma biblioteca de código aberto que simplifica a construção de aplicativos com IA.
- **Modelo de Linguagem**: É um modelo treinado para processar linguagem natural e gerar respostas.
- **API do Groq**: É uma interface de programação que permite acessar recursos do Groq.
- **Histórico de Mensagens**: É uma estrutura de dados que armazena as mensagens trocadas entre o usuário e o chatbot.
- **Prompt Template**: É uma estrutura que define o formato das mensagens enviadas ao modelo de linguagem.
- **Pipeline de Execução**: É uma sequência de etapas que processa as mensagens do usuário e gera respostas.

## Explicação do Código

O código é dividido em seçoes que explicam o processo de criação e execução do chatbot:

1. **Importaçoes das bibliotecas necessárias**:
   - `os`: Permite acessar variáveis de ambiente.
   - `dotenv`: Carrega as variáveis de ambiente do arquivo `.env`.
   - `langchain_groq`: Integração do LangChain com a API do Groq.
   - `langchain_community.chat_message_histories`: Histórico de mensagens.
   - `langchain_core.chat_history`: Classe base para histórico.
   - `langchain_core.runnables.history`: Permite gerenciar histórico dinamicamente.
   - `langchain_core.prompts`: Criação de templates para prompts.
   - `langchain_core.messages`: Manipulação de mensagens.
   - `langchain_core.runnables`: Criação de fluxos de execução reutilizáveis.
   - `operator`: Facilita a extração de valores de dicionários.

2. **Carregamento das variáveis de ambiente**:
   - `load_dotenv()`: Carrega as variáveis de ambiente do arquivo `.env`.
   - `groq_api_key`: Armazena a chave da API do Groq.

3. **Inicialização do modelo de IA**:
   - `ChatGroq`: Integração do LangChain com a API do Groq.
   - `model`: Instância do modelo de linguagem.

4. **Criação de um prompt template**:
   - `ChatPromptTemplate`: Define o formato das mensagens enviadas ao modelo.
   - `MessagesPlaceholder`: Permite adicionar mensagens dinamicamente.

5. **Conectando o modelo ao template de prompt**:
   - `chain`: Fluxo de execução que combina o prompt e o modelo.

6. **Gerenciamento da memória do chatbot**:
   - `trimmer`: Limita o histórico de mensagens para evitar o excesso de contexto.
   - `city_data`: Dicionário com informaçoes sobre cidades brasileiras.

7. **Exemplo de interação**:
   - `response`: Armazena a resposta do modelo após a execução do pipeline de execução.

8. **Exibição da resposta final**:
   - `print`: Exibe a resposta do modelo.

## Conclusão

O chatbot desenvolvido neste projeto é capaz de responder a perguntas relacionadas a informaçoes sobre cidades brasileiras de forma natural e eficiente. A utilização de bibliotecas como LangChain e a integração com a API do Groq permite uma interação fluida e aprimorada com o modelo de linguagem.

O código é estruturado de forma modular, permitindo a facilidade de manutenção e extensão do projeto. Além disso, o uso de variáveis de ambiente para armazenar credenciais protege a integridade do projeto.

Espero ter ajudado. Se tiver mais duvidas, sinta-se à vontade para perguntar.
