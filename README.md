# 🪄 Maestro.AI

> **O Cockpit de Orquestração para Times de Engenharia de Software Aumentados por IA**
> 
> _Onde a Intenção Humana encontra a Execução Autónoma._

[![Status do Projeto](https://img.shields.io/badge/status-em_desenvolvimento-yellow)](https://github.com/) [![Versão](https://img.shields.io/badge/versão-v0.1_(Arquitetura)-blue)](./docs/CHANGELOG.md) [![Linguagem](https://img.shields.io/badge/python-3.11+-3776AB?logo=python&logoColor=white)](https://www.python.org/) [![Framework de Agentes](https://img.shields.io/badge/framework_agentes-LangGraph-orange)](https://langchain-langgraph.smith.langchain.com/) [![API](https://img.shields.io/badge/api-FastAPI-009688?logo=fastapi)](https://fastapi.tiangolo.com/) [![UI](https://img.shields.io/badge/ui-Streamlit-ff4b4b?logo=streamlit)](https://streamlit.io/) [![Licença](https://img.shields.io/badge/licença-pendente-lightgrey)](./LICENSE)

## 🎯 O Que é o Maestro.AI?

O **Maestro.AI** é o **cérebro operacional e a interface de governança** de todo o nosso ecossistema de desenvolvimento, a "Fábrica Janus". Ele não é apenas um dashboard; é o hub central que traduz a **intenção estratégica humana** em fluxos de trabalho executáveis para uma equipe de agentes de IA especializados.

Sua missão é atuar como o "Maestro" de uma orquestra, garantindo que cada "músico" (agente) toque sua parte na hora certa e em harmonia, para produzir uma sinfonia coesa: software de alta qualidade, documentado e testado.

## ✨ Filosofia de Operação

O `Maestro.AI` opera sob três princípios chave que definem nossa abordagem à colaboração Humano-IA:

1. **Autonomia Supervisionada:** Agentes têm a máxima autonomia para resolver tarefas. O `Maestro.AI` fornece ao supervisor humano os "portões de decisão" (`gatekeepers`) para intervir, aprovar ou corrigir o curso em momentos críticos.
    
2. **Governança Dinâmica (ABAC):** As permissões não são estáticas. O `Maestro.AI` consulta um motor de políticas (`Open Policy Agent`) em tempo real para decidir se um agente pode executar uma ação, com base em seus atributos, no contexto da tarefa e no estado do projeto.
    
3. **Orquestração Transparente:** Todas as ações, decisões e comunicações dos agentes são registradas e visualizadas no cockpit do Maestro. O objetivo é eliminar as "caixas pretas" e fornecer total observabilidade sobre o processo.

## 🏗️ Arquitetura de Alto Nível

O `Maestro.AI` posiciona-se como o hub central do ecossistema, comunicando-se com os outros componentes através de APIs bem definidas e interagindo nativamente com o GitHub.

```
graph TD
    subgraph "Maestro Humano (Cockpit)"
        UI[Dashboard - Streamlit/React]
    end

    subgraph "Maestro.AI Core"
        direction LR
        GH_APP[GitHub App Webhooks] --> API[API - FastAPI]
        API --> ORC[Lógica de Orquestração - LangGraph]
    end

    subgraph "Sistemas Externos"
        SE[Synapse Engine]
        PE[Motor de Políticas - OPA]
        VCS[API do GitHub]
    end
    
    AG(Equipe de Agentes de IA)

    UI --> API;
    ORC -->|1. Pede Contexto| SE;
    ORC -->|2. Valida Permissão| PE;
    ORC -->|3. Atribui Tarefa| AG;
    AG -->|4. Executa Ação| VCS;
    AG -->|5. Reporta Progresso| ORC;
```

1. **Interface Humana:** O "Maestro Humano" interage com o sistema através do **Cockpit**.
    
2. **Orquestração Core:** A lógica central, implementada como uma **GitHub App**, recebe eventos, consulta o **`Synapse Engine`** para obter contexto, valida ações contra o **Motor de Políticas** e delega tarefas aos **Agentes de IA**.
    
3. **Execução:** Os agentes executam suas tarefas na plataforma GitHub, interagindo através da **API do GitHub** para criar branches, commits e pull requests.
    

## 🚀 Principais Funcionalidades (Visão do Produto)

O cockpit do `Maestro.AI` será seu centro de comando, oferecendo:

- **Monitoramento de Agentes:** Visualizar o status de cada agente (`ocioso`, `trabalhando`, `bloqueado`), seu `trust_score` e histórico de performance.
    
- **Gestão de Tarefas:** Acompanhar o progresso em um quadro Kanban integrado que reflete o estado real do **GitHub Projects**.
    
- **Gestão de Perfis de Agentes:** Criar, editar e refinar os perfis dos agentes (prompts, ferramentas, especializações) a partir de templates do `Codex Prime`.
    
- **Painel de Custos:** Monitorar o consumo de tokens e os custos de API de cada agente e tarefa.
    
- **Explorador de Conhecimento:** Visualizar e interagir com o grafo de conhecimento do `Synapse Engine`.
    

## 🛠️ Como Começar (Getting Started)

Instruções para configurar e executar o `Maestro.AI` localmente.

### Pré-requisitos

- Python 3.11+
    
- Docker e Docker Compose
    
- Acesso à API do `Synapse Engine` e credenciais de uma GitHub App.
    

### Instalação

1. **Clone o repositório:**
    
    ```
    git clone [URL_DO_REPOSITORIO_MAESTRO]
    cd Maestro.AI
    ```
    
2. **Configure as variáveis de ambiente:**
    
    - Crie um arquivo `.env` a partir do `.env.example` e preencha as chaves de API e credenciais necessárias.
        
3. **Inicie os serviços:**
    
    ```
    # Este comando irá iniciar a API e o Dashboard do Maestro.AI
    docker-compose up -d --build
    ```
    
4. **Acesse o Cockpit:**
    
    - Abra seu navegador e vá para `http://localhost:8501` para acessar o dashboard do Streamlit.
        

## 📖 Documentação

A documentação arquitetural completa do `Maestro.AI`, uma instância do `Codex Prime Framework`, pode ser encontrada na pasta [`/docs`](https://www.google.com/search?q=./docs/ "null").

## 🤝 Como Contribuir

As contribuições para o `Maestro.AI` são vitais. Por favor, consulte nosso [guia de contribuição](https://www.google.com/search?q=./CONTRIBUTING.md "null") para mais detalhes.

## 📄 Licença

Distribuído sob a licença [Nome da Licença]. Veja `LICENSE.txt` para mais informações.

## 📞 Contato

Maestro (Desenvolvedor Principal): Bruno S. Rosa

LinkedIn: [/In/BrunoSRosa](https://linkedin.com/in/brunosrosa)