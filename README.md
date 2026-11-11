# 📚 Estudos — LangChain & LangGraph

Repositório de estudos baseado na playlist do YouTube sobre **LangChain** e **LangGraph**, focado na construção de **agentes ReAct** com grafos de execução.

> Playlist original: [YouTube — Curso LangChain & LangGraph](https://www.youtube.com/playlist?list=PLbIBj8vQhvm09IqqLYIwLF5dGrcbJzFZc)

---

## 🧠 O que estou aprendendo

### LangChain
Framework para trabalhar com LLMs. Resolve integração com modelos, RAG, tools externas e encadeamento de chamadas via **LCEL (LangChain Expression Language)**. Ideal para pipelines lineares:

```
Prompt → LLM → Resposta → FIM
```

### LangGraph
Extensão do LangChain para fluxos complexos baseados em **grafos de execução**. Permite:

- Condições (ex: se o LLM pedir uma tool, segue por um caminho; senão, por outro)
- Loops controlados
- Estado persistente ao longo da conversa

Enquanto o LangChain brilha em pipelines simples, o **LangGraph é feito para agentes**.

---

## 🗂️ Estrutura do projeto

```
.
├── docs/               # Anotações de cada aula (.md)
├── src/examples/       # Código de cada aula
│   ├── ex001/          # Chat simples com LangChain
│   ├── ex002/          # ...
│   └── ex012/
├── pyproject.toml      # Dependências (uv)
└── uv.lock
```

Cada `exNNN/` em `src/examples/` corresponde a um `NNN-*.md` em `docs/` e a uma aula no YouTube.

---

## 📖 Aulas

| # | Tema | Doc | Código |
|---|------|-----|--------|
| 001 | LangChain vs LangGraph | [doc](./docs/001-langchain-vs-langgraph.md) | [ex001](./src/examples/ex001) |
| 002 | Chat simples com LangChain | [doc](./docs/002-chat-simples-langchain.md) | [ex002](./src/examples/ex002) |
| 003 | Introdução ao LangGraph | [doc](./docs/003-introducao-ao-langgraph.md) | [ex003](./src/examples/ex003) |
| 004 | LangGraph com LLM | [doc](./docs/004-langgraph-com-llm.md) | [ex004](./src/examples/ex004) |
| 005 | LLM com Tools | [doc](./docs/005-llm-com-tools-langchain.md) | [ex005](./src/examples/ex005) |
| 006 | LangGraph Studio | [doc](./docs/006-langgraph-studio.md) | [ex006](./src/examples/ex006) |
| 007 | RunnableConfig | [doc](./docs/007-runnable-config.md) | [ex007](./src/examples/ex007) |
| 008 | ToolNode e tools_condition | [doc](./docs/008_toolnode_tools_condition.md) | [ex008](./src/examples/ex008) |
| 009 | Context e ToolRuntime | [doc](./docs/009-runtime-toolruntime-context.md) | [ex009](./src/examples/ex009) |
| 010 | Lifespan | [doc](./docs/010-lifespan.md) | [ex010](./src/examples/ex010) |
| 011 | Checkpointers | [doc](./docs/011-checkpointers.md) | [ex011](./src/examples/ex011) |
| 012 | Checkpointers pt.2 | [doc](./docs/012-checkpointers-part2.md) | [ex012](./src/examples/ex012) |

---

## 🚀 Como rodar

O projeto usa [uv](https://docs.astral.sh/uv/) para gerenciar dependências.

### 1. Instalar dependências

```bash
uv sync
```

### 2. Configurar variáveis de ambiente

Copie o arquivo de exemplo e preencha com suas chaves:

```bash
cp .env-example .env
```

### 3. Rodar um exemplo

```bash
uv run --env-file=".env" src/examples/ex004/code001.py
```

Troque `ex004/code001.py` pelo exemplo da aula que quiser rodar.

---

## 🛠️ Tecnologias

- **Python 3.13**
- **LangChain** — integração com LLMs e tools
- **LangGraph** — grafos de execução para agentes
- **Google Gemini** (`gemini-2.5-flash`) — modelo LLM principal
- **Ollama** — suporte a modelos locais
- **Rich** — output formatado no terminal
- **uv** — gerenciador de dependências

---

## 📝 Licença

MIT
