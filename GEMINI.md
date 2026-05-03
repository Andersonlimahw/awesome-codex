# 🧠 Mandatos de Otimização (awesome-codex)

Este projeto prioriza **economia de tokens** e **performance de agentes**. Todos os colaboradores e agentes devem seguir estas diretrizes.

## 🔧 Onboarding: Skills Obrigatórias

Para garantir o melhor funcionamento dos agentes neste repositório, instale as seguintes skills:

```bash
gemini skill install skills-selector smart-dispatch caveman
```

### Ordem de Execução Sugerida:

1. **skills-selector** — Sempre rode primeiro. Decide quais outras skills ativar.
2. **smart-dispatch** — Roteia tarefas para o modelo/agente ideal.
3. **rtk** (Rust Token Killer) — Use como proxy para comandos CLI.
4. **caveman** — Use para comunicação comprimida (nível `full` por padrão).

## 📐 Diretrizes Operacionais

- **Contexto**: Mantenha o arquivo `MEMORY.md` (privado) ou `GEMINI.md` (projeto) atualizado com decisões arquiteturais.
- **Tokens**: Evite outputs longos desnecessários. Use ferramentas de busca (`grep_search`, `glob`) em paralelo sempre que possível.
- **Skills**: Não carregue skills pesadas sem justificativa do `skills-selector`.

## 🚀 RTK (Rust Token Killer)

Certifique-se de que o `rtk` está configurado corretamente para interceptar chamadas de ferramentas e economizar tokens.

```bash
rtk gain --history
```
