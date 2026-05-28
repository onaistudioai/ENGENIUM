# ENGENIUM

> *Engenheiro de prompt como skill ativável — transforma ideias brutas em prompts robustos para qualquer LLM.*

Skill que vira o agente em um **engenheiro de prompt** sob demanda. Recebe uma ideia bruta e devolve um prompt pronto para copiar, com comentário explicando cada parte para você saber onde mexer depois.

---

## ⚡ Ativação

Comando de ativação: **`Haja luz`**

Resposta esperada:
> *"Engenheiro de prompt ativo. Me manda sua ideia."*

A partir daí toda interação segue o protocolo da skill até o fim da sessão.

---

## 🔑 Regra de Ouro

> **"Que instruções eu daria para uma pessoa fazer isso?"**

Se um humano consegue executar, o modelo também. Se não, provavelmente nem o modelo.

---

## 📋 O que a skill cobre

### Início de sessão (3 perguntas obrigatórias)
Modelo • Destino • Ponto de partida — antes de qualquer análise.

### 12 tipos de prompt, cada um com seu questionário
Criação de Projeto • Agente • Subagente • Código • Reajuste de Código • Debug • Revisão • Testes • Reajuste de Arquivo • Documentação • Análise de Dados • Automação de Pipeline.

### Estrutura base P.R.O.M.P.T.
**P**ersona • **R**oteiro • **O**bjetivo • **M**odelo • **P**anorama • **T**ransformar

### Técnicas por nível
- **Básico:** Few Shot
- **Intermediário:** Chain of Thought, Contrastive CoT, tags XML
- **Avançado:** Self-Consistency, Tree of Thought, Skeleton of Thought

### 7 camadas de evolução para agentes
Memória entre projetos • Origem do tráfego • A/B • Loop de feedback • Validação pré-entrega • SEO on-page • Atualização de catálogo.

### Referência rápida
Tabela situação → técnica recomendada na seção final do `engenheiro.md`.

---

## 🎯 Sinalizações durante a sessão

| Comando | Efeito |
| --- | --- |
| `segue` / `ok` | Avançar sem aprofundar o ponto atual |
| `volta` | Revisitar algo já fechado |

---

## 📦 Entrega final

Sempre dois blocos:
1. **Prompt completo** pronto para copiar
2. **Comentário curto** explicando cada parte — para ajustes futuros

---

## 🚀 Como usar

1. Abra Claude Code (ou outro cliente) → **Custom Instructions / System Prompt**
2. Cole o conteúdo de [`engenheiro.md`](./engenheiro.md)
3. Em uma nova conversa, digite **`Haja luz`**
4. Mande sua ideia bruta — o engenheiro conduz o resto

---

## 🔗 Pipeline com outras skills

ENGENIUM produz o `PROJECT_SPEC.md` que alimenta pipelines de execução, ex.: [DOMINIUMM](https://github.com/onaistudioai/DOMINIUMM) (Arquiteto de Projetos / Orchestrador de Agentes Paralelos).

```
Ideia bruta
   ↓
ENGENIUM (engenheiro de prompt) → PROJECT_SPEC.md
   ↓
DOMINIUMM (arquiteto / orchestrador) → projeto executado
```

---

## 🙏 Créditos

Conteúdo baseado no vídeo [**"Engenharia de Prompt: Guia definitivo"**](https://www.youtube.com/watch?v=1VDcke66TRE) de **Bruno Picinini** no YouTube.

---

## 📄 Licença

MIT.
