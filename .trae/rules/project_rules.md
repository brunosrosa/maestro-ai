```
---
# METADADOS DO PROJETO (Para uso do Maestro.AI)
project_name: 'Maestro.AI'
codex_framework_version: '3.0' # Baseado na versão do Codex Prime Framework
tech_lead: 'Bruno S. Rosa'
status: 'ativo'
document_version: '2.0'
repository_url: 'https://github.com/brunosrosa/maestro-ai'
---
```

# Regras do Projeto: Maestro.AI

## 1. Diretrizes Gerais e Metodologia

- **Objetivo Principal:** Desenvolver o `Maestro.AI`, um **Sistema Operacional de Governança e Execução para Times Aumentados por IA**. Ele funcionará como um cockpit central para o Maestro, integrando controle de projetos (via GitHub), gestão de custos, orquestração de agentes e dashboards de Business Intelligence.
    
- **Metodologia:** Desenvolvimento Full-Stack Ágil Aumentado por IA, com um foco intenso em Design de Produto e Experiência do Usuário (UX) para criar uma interface intuitiva e poderosa.
    
- **Repositório Principal:** `https://github.com/brunosrosa/maestro-ai`
    
- **Caminho da Documentação:** A documentação viva deste projeto é uma instância do `Codex Prime Framework` e reside na pasta `./docs/` na raiz deste repositório.
    

## 2. Stack de Tecnologia e Ferramentas

- **Linguagem Principal (Backend):** Python 3.11+
    
- **Framework Principal (Backend):** FastAPI
    
- **Linguagem Principal (Frontend):** TypeScript
    
- **Framework Principal (Frontend):** React (com Next.js)
    
- **Framework de UI (Prototipagem):** Streamlit
    
- **Orquestração de Agentes:** LangGraph
    
- **Motor de Políticas (ABAC):** Open Policy Agent (OPA) com Rego
    
- **Plataforma de Deploy Alvo:** Backend como contêiner Docker em VPS (Ubuntu); Frontend em Vercel.
    
- **Ferramentas de Qualidade:**
    
    - **Backend:** Pytest, Black, Flake8, MyPy
        
    - **Frontend:** Jest, ESLint, Prettier
        

## 3. Padrões de Código e Versionamento

- **Convenção de Nomenclatura:**
    
    - **Arquivos de Documentação:** `MAIUSCULA_COM_UNDERLINE`
        
    - **Arquivos de Código Python:** `snake_case` (ex: `agent_manager_service.py`)
        
    - **Arquivos de Código TypeScript/React:** `PascalCase` para componentes (ex: `ProjectDashboard.tsx`), `camelCase` para funções e variáveis.
        
- **Estilo de Commits:** Utilizar estritamente o padrão de **Conventional Commits** (ex: `feat(ui):`, `fix(api):`, `docs:`) para manter um histórico claro e segmentado.
    
- **Guia de Estilo de Código:** Aderir rigorosamente aos guias de estilo oficiais das linguagens (PEP 8 para Python, padrões da comunidade para TypeScript/React).
    

## 4. Hierarquia e Delegação de Agentes

- **Agente Estratégico (Chefe de Gabinete):** `@Janus`
    
- **Agente Tático (Gerente de Projetos):** `@Orquestrador`
    
- **Agentes Especialistas Principais:**
    
    - `@DevPython_FastAPI` (Desenvolvimento do Backend e da lógica de orquestração)
        
    - `@DevReact_TypeScript` (Desenvolvimento da interface e componentes do frontend)
        
    - `@Designer_UI_UX` (Projeta a experiência do usuário e o design visual do cockpit)
        
    - `@Engenheiro_de_BI_e_Dados` (Desenvolve os dashboards e as visualizações de dados)
        
    - `@Arquiteto_de_Cloud_e_DevOps` (Infraestrutura, Docker, CI/CD, integrações de API)
        

## 5. Protocolo de Resolução de Conflitos

Em caso de conflito ou ambiguidade entre diferentes fontes de regras, a seguinte hierarquia de prioridade **DEVE** ser seguida:

1. **Decisão explícita e atual do Maestro:** Uma instrução direta de Bruno S. Rosa sempre tem a maior prioridade.
    
2. **`project_rules.md` (Este Documento):** As regras específicas para o projeto `Maestro.AI`.
    
3. **`user_rules.md`:** As regras e preferências globais do Maestro.
    
4. **`Regras_do_Jogo.md`:** A constituição geral do ecossistema.
    
5. **Documentação Técnica Viva do Projeto:** Decisões formalizadas em ADRs, HLDs e outros documentos na pasta `./docs/`.
    
6. **Padrões Gerais da Indústria e da Linguagem.**
    
O agente que identificar um conflito tem a responsabilidade de sinalizá-lo e solicitar orientação para garantir o alinhamento.