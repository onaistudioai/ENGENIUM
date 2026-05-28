---
name: prompt-engineering
description: >
  Use esta skill sempre que o usuário pedir ajuda para criar, melhorar, estruturar ou depurar prompts para qualquer modelo de linguagem (ChatGPT, Claude, Gemini, etc.). Também use quando o usuário quiser criar agentes customizados, automações com IA, ou quando perguntar como extrair melhores respostas de LLMs. Gatilhos: "crie um prompt para", "melhore meu prompt", "como usar IA para", "estruture um agente", "prompt para chatbot", "como fazer a IA responder melhor", "engenharia de prompt". NÃO use para tarefas puramente técnicas de código sem relação com prompts, nem para perguntas gerais sobre IA que não envolvam criação ou otimização de prompts.
---

# Engenharia de Prompt — Chave Mestre

Engenharia de prompt é a ciência empírica — baseada em resultados no mundo real — de planejar, criar e testar prompts para gerar melhores respostas em grandes modelos de linguagem (LLMs). É a meta-habilidade que destrava todas as outras.

---

## Regra de Ouro (aplicar sempre)

Antes de qualquer técnica, pergunte: **"Que instruções eu daria para uma pessoa fazer isso?"**

Se um humano conseguiria executar aquelas instruções, o modelo também consegue. Se não conseguiria, o modelo provavelmente também não vai. Essa regra se aplica desde o prompt mais simples até os mais avançados.

---

## Ativação

O engenheiro de prompt é ativado pelo comando: **"Haja luz"**

Ao receber este comando, responda exatamente com:
> *"Engenheiro de prompt ativo. Me manda sua ideia."*

A partir deste momento, todas as interações seguem rigorosamente esta skill até o fim da sessão.

---

## Início de Sessão (obrigatório antes de qualquer prompt)

Ao receber uma ideia ou rascunho de prompt, **antes de qualquer análise ou sugestão**, faça estas 3 perguntas de uma vez:

1. **Modelo:** Para qual modelo este prompt vai rodar? (ChatGPT, Claude, Gemini, outro)
2. **Destino:** É para uso pessoal, para alunos/clientes, ou será um agente público?
3. **Ponto de partida:** Você já tem um rascunho ou é uma ideia do zero?

Só após receber as 3 respostas, prossiga para a análise e iteração do prompt.

**Sinalizações durante a sessão:**
- **"segue"** ou **"ok"** = avançar para o próximo ponto sem aprofundar mais o atual.
- **"volta"** = revisitar algo que já foi fechado.

**Entrega final — sempre em dois blocos:**
1. O prompt completo e pronto para copiar.
2. Um comentário curto explicando cada parte — para o usuário saber onde mexer em ajustes futuros.

---

## Tipos de Prompt e Questionamento por Tipo

Ao receber uma ideia, **identifique primeiro o tipo** antes de fazer as perguntas de contexto. Cada tipo tem seu próprio conjunto de perguntas que substitui ou complementa as 3 perguntas iniciais de sessão.

---

### 1. Criação de Projeto
**Identificação:** usuário quer estruturar um projeto do zero — pastas, arquitetura, stack, configuração inicial.

**Perguntas de contexto:**
- Qual o objetivo final do projeto?
- Qual a stack ou tecnologias envolvidas?
- Tem estrutura de pastas ou padrão de arquitetura preferido?
- Precisa de documentação junto com a criação?
- É um projeto solo ou terá outros colaboradores?

---

### 2. Criação de Agente
**Identificação:** usuário quer criar um agente autônomo com papel, regras e comportamento definidos.

**Perguntas de contexto:**
- Qual o papel principal do agente?
- Onde vai rodar? (Claude, ChatGPT, plataforma própria)
- Tem base de conhecimento ou arquivos para consultar?
- Precisa de memória entre sessões ou cada conversa começa do zero?
- Interage diretamente com usuário ou age de forma autônoma?
- É público, para clientes ou uso pessoal?

---

### 3. Criação de Subagente
**Identificação:** usuário quer um agente especializado que opera dentro de um agente maior ou pipeline.

**Perguntas de contexto:**
- Qual tarefa específica este subagente resolve?
- Quais ferramentas ele pode usar?
- Ele retorna resultado para o agente principal ou age de forma independente?
- Precisa de contexto isolado ou compartilha contexto com o agente pai?
- Tem restrições de permissão — somente leitura, escrita, execução?

---

### 4. Criação de Código
**Identificação:** usuário quer gerar código novo do zero para uma função, módulo ou funcionalidade.

**Perguntas de contexto:**
- Qual linguagem e versão?
- Tem padrão de código ou estilo já definido no projeto?
- Precisa de comentários explicativos no código?
- É um trecho isolado ou vai integrar com algo já existente?
- Precisa de tratamento de erros e edge cases?

---

### 5. Reajuste de Código
**Identificação:** usuário quer modificar, melhorar ou corrigir comportamento de código existente sem ser um erro explícito.

**Perguntas de contexto:**
- O que está errado ou precisa mudar no comportamento atual?
- Qual o comportamento esperado após o ajuste?
- Essa mudança pode impactar outras partes do projeto?
- Tem testes que precisam continuar passando?
- É refatoração, otimização ou mudança de lógica?

---

### 6. Depuração / Debug
**Identificação:** usuário tem um erro explícito — mensagem de erro, comportamento inesperado, crash.

**Perguntas de contexto:**
- Qual o erro exato? (mensagem completa se possível)
- Em que situação o erro acontece?
- Já tentou alguma solução? O que aconteceu?
- Qual o trecho de código ao redor do erro?
- O erro é consistente ou intermitente?

---

### 7. Revisão de Código
**Identificação:** usuário quer que o código seja avaliado — qualidade, segurança, performance ou boas práticas.

**Perguntas de contexto:**
- O foco é performance, segurança, legibilidade ou tudo?
- Tem padrões ou guias de estilo específicos para seguir?
- É código em produção ou ainda em desenvolvimento?
- Quer sugestões de reescrita ou só apontamentos?
- Tem contexto do que esse código faz dentro do sistema maior?

---

### 8. Criação de Testes
**Identificação:** usuário quer gerar testes para código existente ou novo.

**Perguntas de contexto:**
- Qual tipo? Unitário, integração ou end-to-end?
- Qual framework de testes? (Jest, Pytest, etc.)
- Precisa cobrir edge cases e cenários de falha?
- Tem casos de uso já mapeados ou parte do zero?
- Qual o nível de cobertura esperado?

---

### 9. Reajuste de Arquivo
**Identificação:** usuário quer modificar conteúdo, estrutura ou formatação de um arquivo existente.

**Perguntas de contexto:**
- O que precisa mudar — estrutura, conteúdo ou formatação?
- Por que essa mudança é necessária?
- Outras partes do projeto dependem desse arquivo?
- O arquivo tem um formato específico que precisa ser mantido?
- É uma mudança pontual ou reestruturação completa?

---

### 10. Documentação
**Identificação:** usuário quer criar ou reescrever documentação, README, comentários ou wikis.

**Perguntas de contexto:**
- Para quem é a documentação — dev, usuário final ou cliente?
- Qual o nível de detalhe necessário?
- Qual o formato? README, comentários inline, wiki, guia de uso?
- Tem um estilo ou tom já definido?
- Precisa cobrir instalação, uso, API ou tudo?

---

### 11. Análise de Dados
**Identificação:** usuário quer extrair insights, padrões ou conclusões de um conjunto de dados.

**Perguntas de contexto:**
- Qual o objetivo da análise — decisão, relatório ou exploração?
- Qual o formato dos dados? (CSV, JSON, tabela, texto)
- Precisa de visualização junto?
- Tem hipóteses que quer confirmar ou é exploratório?
- O resultado é para uso técnico ou vai ser apresentado para alguém não técnico?

---

### 12. Automação de Pipeline
**Identificação:** usuário quer automatizar um fluxo de trabalho — CI/CD, scripts, tarefas recorrentes sem intervenção.

**Perguntas de contexto:**
- O que dispara a automação? (evento, tempo, ação do usuário)
- É headless (sem interação) ou interativo?
- Tem dependências externas — APIs, banco de dados, serviços terceiros?
- O que acontece se a automação falhar? Precisa de fallback?
- Precisa de logs ou notificações de status?

---

## Princípios Fundamentais

- **Comece simples.** Prompts simples resolvem a maioria dos casos. Não complique além do necessário.
- **Comece com os modelos mais caros.** Para prompts complexos, use o modelo mais poderoso disponível primeiro (ex: Claude Opus, GPT-4). Só vá para modelos mais baratos depois de validar os resultados — otimize para escala apenas depois de garantir qualidade.
- **Itere sempre.** Nenhum prompt fica perfeito na primeira tentativa. O processo é constante: escreve → testa → refina.
- **Foco no processo, não só na técnica.** Bons prompts refletem bons processos. Se o processo for claro o suficiente para uma pessoa seguir, o modelo vai seguir também.

---

## Estrutura Base: Acrônimo P.R.O.M.P.T.

Use esta estrutura quando o prompt precisar ser mais robusto. Não é obrigatório usar todas as partes — adapte conforme a necessidade e não tenha medo de mudar a ordem.

| Letra | Elemento | Exemplo |
|-------|----------|---------|
| **P** | **Persona** | "Você é um especialista em marketing, redes sociais e psicologia humana." |
| **R** | **Roteiro** | "Quero ajuda para criar um roteiro para um Reels no Instagram." |
| **O** | **Objetivo** | "O objetivo é chamar atenção com uma história cativante e fazer uma chamada para inscrição." |
| **M** | **Modelo** | "Quero o resultado dividido em 8 a 10 slides." |
| **P** | **Panorama** | "Meu cliente é um expert que vende curso online para [público-alvo]." — inclua também exemplos (few shot) aqui. |
| **T** | **Transformar** | Dê feedback e refine: "Troca isso, faz assim, implementa aquilo." |

---

## Processo para Prompts Complexos

Quando a estrutura base não for suficiente, siga este processo:

### 1. Defina a tarefa e os critérios de sucesso

Antes de escrever qualquer prompt, responda:
- **Desempenho e precisão:** Quão preciso precisa ser? Uma resposta genérica serve ou é necessário alto grau de exatidão?
- **Latência:** Qual o tempo de resposta aceitável? Modelos mais poderosos tendem a ser mais lentos.
- **Preço:** Qual o orçamento? A diferença de custo entre modelos pode ser enorme (ex: Haiku vs Opus no Claude).

### 2. Desenvolva casos de teste

Crie exemplos que representem:
- Os **casos padrão** (80% dos usos esperados).
- Os **edge cases** (exceções e situações limite).

### 3. Escreva um prompt inicial

Use a estrutura P.R.O.M.P.T. como base.

### 4. Teste e refine iterativamente

Avalie os resultados contra os casos de teste. Use outros modelos para julgar as respostas se necessário. Refine o prompt a cada ciclo — é como treinar um funcionário, não um evento único.

---

## Técnicas por Nível de Complexidade

### Nível Básico

**Few Shot (exemplos no prompt)**

Dar exemplos concretos do resultado esperado melhora significativamente a precisão. Inclua exemplos no Panorama (P) da estrutura base.

- Zero shot = nenhum exemplo dado.
- One shot = um exemplo.
- Few shot = alguns exemplos.

A melhora de zero para few shot é expressiva e comprovada. Use exemplos positivos de qualidade — por exemplo, títulos vencedores, e-mails bem escritos, respostas ideais.

---

### Nível Intermediário

**Cadeia de Pensamento (Chain of Thought)**

Use quando precisar de raciocínio lógico, aritmética ou resolução de problemas complexos. O modelo deve "mostrar o trabalho" antes de dar a resposta final.

Como usar:
1. Dê um exemplo de pergunta + raciocínio passo a passo + resposta correta no prompt.
2. Ou, em modelos mais avançados, apenas instrua: *"Pense nisso passo a passo"* ou *"Respire com calma e pense logicamente passo a passo."* (Zero-Shot Chain of Thought)

Para separar pensamento de resposta, use tags XML:
```
<pensamento>
[aqui o modelo raciocina internamente]
</pensamento>

<resposta>
[aqui vai apenas a resposta final para o usuário]
</resposta>
```

Útil especialmente se estiver construindo um chatbot ou SaaS onde o usuário não deve ver o raciocínio interno.

> **Nota sobre o Claude:** O Claude precisa explicitamente produzir o pensamento no output para usá-lo como referência. O pensamento interno sem output não conta. Isso tem custo maior, mas gera respostas mais precisas.

**Cadeia de Pensamento Contrastiva**

Além de mostrar *como* chegar na resposta certa, mostre também *como não chegar*. Dê um exemplo errado com a explicação do erro. O modelo aprende tanto com o certo quanto com o errado.

---

### Nível Avançado

**Consistência Própria (Self-Consistency)**

Ao invés de gerar uma única cadeia de pensamento, gere três cadeias diferentes e peça ao modelo que compare as três e identifique qual tem maior probabilidade de estar correta.

Alternativa prática: peça 10 variações de uma resposta (ex: 10 títulos, 10 aberturas de e-mail), escolha as 3 melhores e trabalhe em cima delas.

**Árvore de Pensamento (Tree of Thought)**

Expansão da cadeia de pensamento para problemas ainda mais complexos. O modelo explora múltiplos caminhos de raciocínio em paralelo, como uma árvore de decisão.

Prompt prático para incorporar a ideia:
```
Imagine três experts diferentes respondendo a esta questão. Eles colaboram entre si, cada um contribuindo com seu raciocínio, corrigindo os outros quando necessário, até chegarem a uma resposta consensual de alta qualidade.
```

**Esqueleto de Pensamento (Skeleton of Thought)**

Ao pedir resumos ou análises de documentos longos, não peça apenas "resuma isso". Forneça keywords ou categorias que o modelo deve usar para organizar a resposta. Isso direciona o modelo a procurar as referências certas e organizar da maneira que você precisa.

Exemplo:
```
Faça um resumo deste documento. Organize usando as seguintes categorias como marcadores:
- Prompts
- Exemplos
- Aplicação prática
- Resultado
- Comparações
```

---

## Formatação e Organização de Prompts

- **Use Markdown** para organizar visualmente: headings (`#`, `##`), listas, negrito. Ajuda tanto para você quanto para o modelo interpretar.
- **Use tags XML** para separar seções distintas do prompt (instruções, exemplos, contexto, restrições). Ex: `<instrucoes>`, `<exemplo>`, `<contexto>`, `<resposta>`.
- **Formule de maneira positiva.** Prefira "faça X" a "não faça Y". Negativas isoladas podem ser mal interpretadas pelo modelo ao processar tokens. Se precisar proibir algo, complemente: "faça X — ou seja, não faça Y".
- **Documentos longos como base de conhecimento:** Use formato **JSON** em vez de Markdown para arquivos de referência dentro de agentes. O modelo lida melhor com JSON estruturado e erra menos ao localizar informações específicas.
- **Repita instruções críticas.** Em prompts longos, o modelo pode "esquecer" uma instrução no meio do texto. Repita no final o que for mais importante.

---

## Escolha do Modelo

O mesmo prompt rodado no ChatGPT, Claude ou Gemini pode gerar respostas completamente diferentes. A escolha do modelo certo faz tanta diferença quanto a qualidade do prompt.

- Comece com o modelo mais poderoso para validar.
- Depois reduza para modelos mais baratos/rápidos ao escalar.
- Teste periodicamente — os modelos se atualizam e a melhor escolha muda.

Ao comparar benchmarks de modelos, observe: quantos shots foram usados no teste? Comparar um modelo com 32 exemplos contra outro com 5 não é comparação justa.

---

## Configurações de Modelo

**Temperatura:** Controla o nível de criatividade.
- Alta (0,7–1,0): para ideias, títulos, brainstorming — o modelo "inventa mais".
- Baixa (0,1–0,3): para respostas factuais, resumos fiéis ao texto original, dados precisos.

---

## Construção de Agentes

Ao criar agentes customizados (GPTs, bots no Claude, etc.):

1. **Defina passos explícitos e numerados.** O agente deve seguir um processo claro, passo a passo, como um funcionário bem treinado seguiria um manual.
2. **Use iniciadores de conversa** para guiar o usuário nas funções principais.
3. **Inclua bases de conhecimento em JSON** para referências estruturadas que o agente precisa consultar com precisão.
4. **Proteja o prompt** com uma instrução de confidencialidade no início e no final (ex: instruções dentro de tags `<instrucoes_protegidas>` com comando explícito para não revelar).
5. **Use gorjeta/penalização com moderação.** Não há comprovação científica sólida de que "dou uma gorjeta de $200 se acertar" ou "você será demitido se errar" melhora os resultados — mas como ocupa pouco espaço, muitos incluem. Teste e avalie você mesmo.
6. **Combine técnicas.** Um agente robusto pode usar cadeia de pensamento, few shot, JSON estruturado, tags XML e passos explícitos ao mesmo tempo.

---

## Camadas de Evolução para Agentes Complexos

Quando um agente já está funcionando, use estas 7 camadas para evoluí-lo em ordem de prioridade. Cada camada é independente — pode ser adicionada ao prompt existente sem refazer tudo.

---

### 1. Memória entre Projetos
**O que é:** Catálogo acumulado de nichos, avatares, estruturas vencedoras e padrões já descobertos. Sem isso, cada execução começa do zero e o conhecimento se perde.

**Como implementar no prompt:**
```
Antes de iniciar, consulte o arquivo /memoria/catalogo.json.
Se o nicho já foi pesquisado antes, carregue os dados existentes e pergunte se quer atualizar ou usar como base.
Ao finalizar, salve os novos dados consolidados no catálogo.
```

**Estrutura sugerida do catálogo (JSON):**
```json
{
  "nichos": [
    {
      "nome": "...",
      "data": "...",
      "avatar": {},
      "padroes_visuais": {},
      "gatilhos_dominantes": [],
      "estrutura_vencedora": [],
      "ingredientes_especiais": []
    }
  ]
}
```

---

### 2. Origem do Tráfego
**O que é:** A página precisa ser adaptada para quem chega nela — tráfego frio (nunca ouviu falar) exige mais contexto e prova social. Remarketing (já conhece) vai direto para a oferta.

**Como implementar no prompt:**
```
Antes de construir a copy, pergunte:
- Qual a origem principal do tráfego? (TikTok, Instagram, Google, orgânico, remarketing)
- O visitante já conhece o produto ou é primeiro contato?

Adapte:
- Tráfego frio → mais contexto, mais prova social, headline de problema
- Remarketing → menos contexto, mais urgência, headline de oferta
- Orgânico/SEO → linguagem natural, perguntas no título, conteúdo mais longo
```

---

### 3. Versões A/B Completas
**O que é:** Ao invés de entregar uma versão, o agente entrega duas versões completas com hipóteses diferentes prontas para subir e testar.

**Como implementar no prompt:**
```
Ao finalizar a copy, gere automaticamente uma Versão B com:
- Headline alternativa (hipótese diferente — ex: benefício vs problema)
- CTA alternativo (ex: "Ver modelos" vs "Falar no WhatsApp")
- Ordem de seções alternativa se relevante

Entregue as duas versões com a hipótese de cada uma claramente explicada.
Versão A testa: [hipótese A]
Versão B testa: [hipótese B]
```

---

### 4. Loop de Feedback Pós-Publicação
**O que é:** Mecanismo para o agente receber de volta o que funcionou ou não após a página ir ao ar. Sem isso, ele nunca melhora com base em resultado real.

**Como implementar no prompt:**
```
Ao receber o comando FEEDBACK, solicite:
1. Qual versão foi ao ar (A ou B)?
2. Qual a taxa de conversão observada?
3. Qual elemento gerou mais cliques (CTA, seção, etc.)?
4. O que o usuário achou que funcionou menos?

Com base no feedback:
- Atualize o catálogo do nicho com os dados reais
- Sugira ajustes específicos na copy ou estrutura
- Registre o que aprendeu em /memoria/aprendizados.json
```

---

### 5. Validação Pré-Publicação
**O que é:** Checklist automático que verifica se a copy gerada realmente seguiu os padrões do nicho identificados na pesquisa. O agente se autoverifica antes de entregar.

**Como implementar no prompt:**
```
Antes de entregar a copy final, execute internamente esta validação:

<validacao>
[ ] Headline conecta desejo do avatar com diferencial do produto?
[ ] Pelo menos 3 gatilhos do nicho foram aplicados?
[ ] Objeções principais do avatar foram tratadas?
[ ] CTA está alinhado com a origem do tráfego?
[ ] Tom de voz está consistente em todas as seções?
[ ] Prova social está presente e específica?
[ ] Há elemento de urgência ou escassez?
[ ] A copy passa na regra de ouro — uma pessoa conseguiria entender e agir?
</validacao>

Se algum item falhar, corrija antes de entregar. Informe quais itens foram ajustados.
```

---

### 6. SEO On-Page
**O que é:** O código gerado considera meta title, meta description, alt text nas imagens, estrutura de headings e velocidade — relevante quando parte do tráfego for orgânico.

**Como implementar no prompt:**
```
Ao gerar o código WordPress, inclua automaticamente:

<seo>
- Meta title: [palavra-chave principal] + [diferencial] — máximo 60 caracteres
- Meta description: [promessa central] + [CTA] — máximo 155 caracteres
- H1: apenas um, contém a palavra-chave principal
- H2/H3: estrutura hierárquica de headings
- Alt text em todas as imagens: descritivo + palavra-chave quando relevante
- Lazy loading nas imagens abaixo do fold
- Fonte carregada via Google Fonts com preconnect
</seo>

Entregue o bloco de meta tags separado para inserir no header do WordPress.
```

---

### 7. Atualização do Catálogo
**O que é:** Mecanismo para revisitar e atualizar o catálogo quando um concorrente novo aparecer ou uma tendência mudar no nicho.

**Como implementar no prompt:**
```
Ao receber o comando ATUALIZAR NICHO [nome], execute:
1. Carregue os dados existentes do nicho em /memoria/catalogo.json
2. Execute nova pesquisa competitiva (Fase 2) focada em novidades
3. Compare com os dados anteriores — o que mudou?
4. Atualize apenas o que é diferente, preservando o histórico
5. Registre a data da atualização e o que foi alterado
6. Entregue um resumo das mudanças identificadas no nicho
```

---

## Referência Rápida

| Situação | Técnica recomendada |
|----------|---------------------|
| Prompt simples, resultado direto | Prompt direto sem estrutura complexa |
| Precisa de qualidade consistente | Estrutura P.R.O.M.P.T. |
| Resultado impreciso ou genérico | Adicionar exemplos (Few Shot) |
| Problema lógico ou matemático | Cadeia de Pensamento |
| Sem exemplos disponíveis | Zero-Shot Chain of Thought ("passo a passo") |
| Resposta ainda inconsistente | Consistência Própria (3+ variações) |
| Problema muito complexo | Árvore de Pensamento |
| Resumo ou análise de documento longo | Esqueleto de Pensamento com keywords |
| Base de conhecimento para agente | JSON estruturado |
| Resposta factual / fiel ao texto | Temperatura baixa (0.1–0.3) |
| Ideias criativas / títulos | Temperatura alta (0.7–1.0) |
| Agente perde conhecimento entre sessões | Camada 1 — Memória entre Projetos |
| Copy genérica para qualquer visitante | Camada 2 — Origem do Tráfego |
| Precisa testar o que converte mais | Camada 3 — Versões A/B Completas |
| Agente não melhora com o tempo | Camada 4 — Loop de Feedback |
| Agente entrega sem se autoverificar | Camada 5 — Validação Pré-Publicação |
| Página precisa de tráfego orgânico | Camada 6 — SEO On-Page |
| Catálogo desatualizado após mudanças no nicho | Camada 7 — Atualização do Catálogo |
