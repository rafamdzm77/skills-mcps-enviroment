---
description: Planeja, implementa, integra, otimiza e valida experiências visuais, animadas, audiovisuais e tridimensionais para a web. Use quando uma tarefa envolver GSAP, ScrollTrigger, Three.js, WebGL, Blender, modelos GLTF/GLB, vídeos, image sequences, animações ligadas ao scroll ou interações visuais avançadas.
name: creative-development
---

# Creative Development

**Manual operacional de engenharia de experiências criativas para a web**

- **Nome da Skill:** `creative-development`
- **Arquivo de entrada:** `SKILL.md`
- **Responsabilidade central:** transformar objetivos e referências criativas em experiências web implementáveis, acessíveis, responsivas, eficientes e verificáveis.
- **Público deste documento:** agentes de programação, designers técnicos e desenvolvedores — inclusive pessoas que ainda estão aprendendo essas tecnologias.

---

## 1. Propósito e definição

Creative Development é a área que conecta intenção criativa e implementação técnica. Ela trata de experiências nas quais movimento, tempo, interação, mídia ou elementos tridimensionais fazem parte importante do produto.

Exemplos:

- Uma seção de abertura em que um produto se movimenta conforme a pessoa rola a página.
- Uma cena Three.js em que a pessoa pode girar e explorar um objeto.
- Uma sequência de imagens que conta a transformação de um produto.
- Um vídeo cuja reprodução é sincronizada com o scroll.
- Uma transição entre seções que comunica continuidade.
- Uma experiência 3D produzida no Blender e apresentada no navegador.

A Skill não existe para adicionar efeitos por padrão. Existe para escolher e executar a solução que melhor atende ao objetivo do projeto.

**Princípio central:** a tecnologia deve servir à experiência; a experiência deve servir ao usuário. Nenhum efeito visual justifica comprometer conteúdo, navegação, acessibilidade, segurança, desempenho ou manutenção.

### 1.1 O que significa fazer um bom trabalho

Uma implementação só pode ser considerada bem-sucedida quando:

1. Resolve o objetivo que motivou a experiência.
2. Está integrada à arquitetura e ao design existentes.
3. Funciona nos ambientes e dispositivos definidos para o projeto.
4. Não impede o acesso ao conteúdo ou às ações essenciais.
5. Respeita preferências de movimento e formas alternativas de interação.
6. Tem custo de carregamento e execução compatível com o público esperado.
7. Trata falhas de carregamento, redimensionamento e interrupção.
8. Pode ser mantida por outra pessoa desenvolvedora.
9. Foi verificada por testes adequados.
10. Declara claramente o que foi e o que não foi testado.

Uma animação que funciona apenas no computador de quem a desenvolveu não é, por esse motivo, uma implementação pronta para produção.

---

## 2. Escopo e limites de responsabilidade

### 2.1 Responsabilidades do Creative Development

O agente deverá:

- Entender a intenção da experiência e traduzi-la em requisitos técnicos.
- Investigar o projeto existente antes de modificar código.
- Comparar alternativas de implementação.
- Planejar movimento, ritmo, sequência, câmera, profundidade e interação.
- Escolher tecnologias com justificativa.
- Implementar animações, cenas 3D, vídeos e sequências de imagens.
- Integrar essas experiências à estrutura da aplicação.
- Planejar adaptação a diferentes áreas de visualização e capacidades de dispositivos.
- Otimizar carregamento, renderização, memória e execução.
- Prever estados de carregamento, erro, pausa e alternativa.
- Testar e documentar o resultado.
- Comunicar riscos, limitações e decisões ainda pendentes.

### 2.2 O que não deve assumir sozinho

O Creative Development não deve:

- Definir sozinho a identidade visual completa do produto.
- Substituir pesquisa de usuário, arquitetura de informação ou decisões gerais de UX.
- Alterar a arquitetura do projeto sem necessidade e justificativa.
- Instalar bibliotecas apenas por preferência ou popularidade.
- Introduzir 3D, vídeo ou animação quando uma solução simples atende melhor.
- Declarar uma experiência acessível, segura ou performática sem verificação.
- Criar uma versão independente para cada resolução sem antes avaliar adaptação.
- Remover conteúdo, controles ou funcionalidades para facilitar uma animação.
- Tratar uma referência visual como autorização para copiar integralmente um trabalho protegido.
- Ignorar licenças, origem ou direitos de uso de modelos, imagens, fontes, áudio e vídeos.

### 2.3 Relação com outras áreas

As responsabilidades devem se complementar, sem duplicação:

| Área ou Skill | Responsabilidade principal | Colaboração com Creative Development |
|---|---|---|
| Frontend Engineering | Estrutura, componentes, estado, lógica e arquitetura do frontend | Integra a experiência à aplicação e define padrões de implementação |
| UI/UX Design | Necessidades, fluxos, hierarquia, usabilidade e direção de interface | Define o propósito da interação e os critérios de experiência |
| Responsividade | Estratégias gerais para diferentes tamanhos, orientações e contextos de uso | Orienta como a experiência criativa deve se adaptar |
| Julgamento Crítico | Avaliação independente, identificação de problemas e vereditos fundamentados | Questiona decisões e cobra evidências |
| Segurança | Ameaças, confiança, validação e proteção de dados e recursos | Avalia arquivos, dependências, conteúdo externo e interações |
| Testes e Qualidade | Estratégia, execução e registro de testes | Define cenários e comprova o comportamento da experiência |
| Performance | Medição e otimização do sistema | Avalia custos de animação, mídia, CPU, GPU, memória e rede |
| Orquestrador | Seleção e coordenação das Skills necessárias | Recebe tarefas e informa dependências e resultados |

Se uma dessas Skills ainda não existir, o agente deve aplicar boas práticas conhecidas e registrar a lacuna. Não deve fingir que consultou uma Skill inexistente.

---

## 3. Regras obrigatórias de operação

Estas regras se aplicam a toda tarefa conduzida por esta Skill.

### Regra 1 — Analisar antes de alterar

Antes de editar arquivos, o agente deve:

1. Identificar a estrutura do projeto.
2. Localizar os pontos de entrada e os componentes envolvidos.
3. Identificar framework, bibliotecas, versões e ferramentas já utilizadas.
4. Ler os arquivos que controlam a área que será modificada.
5. Verificar padrões existentes de estilo, animação, carregamento e limpeza.
6. Identificar funcionalidades que não podem ser quebradas.
7. Determinar como executar e testar o projeto.

Não deve reescrever uma estrutura inteira quando uma alteração localizada for suficiente. Não deve presumir que o projeto usa uma tecnologia apenas porque ela é comum.

### Regra 2 — Definir o objetivo antes do efeito

Antes de escolher uma técnica, responder:

- O que a pessoa precisa perceber, compreender ou conseguir fazer?
- Qual informação ou ação a experiência deve destacar?
- O movimento ajuda a comunicar algo ou é apenas decorativo?
- O efeito pode atrasar ou dificultar o acesso ao conteúdo?
- Existe uma alternativa mais simples que entrega o mesmo resultado?

Se o objetivo não estiver claro e a decisão puder alterar significativamente o resultado, pedir esclarecimento em vez de inventar requisitos.

### Regra 3 — Justificar a tecnologia

Para cada tecnologia ou dependência nova, explicar:

- Qual problema resolve.
- Por que foi escolhida.
- Quais alternativas foram consideradas.
- Quais custos introduz.
- Como será testada.
- Como será removida ou substituída se deixar de ser necessária.

Não escolher GSAP, Three.js ou qualquer biblioteca apenas porque ela aparece em sites premiados.

### Regra 4 — Preferir a solução proporcional

Avaliar as alternativas em uma escala de complexidade:

1. HTML e CSS nativos.
2. JavaScript e APIs do navegador.
3. Biblioteca especializada de animação.
4. Renderização 2D ou canvas, quando apropriado.
5. WebGL e 3D em tempo real.
6. Vídeo ou sequência de imagens, quando a natureza do conteúdo justificar.

Essa ordem é um roteiro de avaliação, não uma hierarquia absoluta. A solução correta depende dos requisitos.

### Regra 5 — Não presumir sucesso

O agente deve distinguir:

- **Implementado:** o código foi escrito ou alterado.
- **Executado:** a aplicação ou o teste foi iniciado.
- **Verificado:** o comportamento foi observado por um método adequado.
- **Aprovado:** os critérios definidos foram atendidos.
- **Não verificado:** não houve ambiente, ferramenta ou evidência suficiente.

Nunca declarar "funcionando perfeitamente", "100% responsivo" ou "totalmente otimizado" sem evidências que sustentem essas afirmações.

### Regra 6 — Preservar o projeto

Não apagar, substituir ou simplificar funcionalidades existentes sem entender seu propósito e sem comunicar o impacto. Manter convenções, dependências e arquitetura do repositório, salvo justificativa técnica documentada.

### Regra 7 — Declarar incertezas

Quando a documentação for insuficiente, contraditória ou não tiver sido consultada, declarar a incerteza. Separar fatos documentados, observações do projeto, hipóteses e recomendações. Nunca inventar APIs, parâmetros, compatibilidade ou resultados de teste.

---


## 7. Three.js, WebGL e cenas 3D

### 7.1 Fundamentos que o agente precisa compreender

Uma cena Three.js normalmente envolve:

- **Scene:** contêiner lógico dos objetos, luzes e elementos da cena.
- **Camera:** define de onde e como a cena é observada.
- **Renderer:** transforma a cena em pixels usando a tecnologia de renderização disponível.
- **Geometry:** descreve a forma dos objetos.
- **Material:** define como a superfície reage à luz e é apresentada.
- **Texture:** fornece imagens ou dados usados por materiais.
- **Mesh:** combina geometria e material.
- **Render loop:** ciclo que atualiza e desenha a cena.

O agente deve entender como esses elementos se relacionam. Alterar a proporção da área de visualização, por exemplo, pode exigir atualizar a câmera e o renderer.

### 7.2 Redimensionamento correto

Quando o contêiner muda de tamanho:

1. Medir a largura e a altura disponíveis.
2. Confirmar que ambas são maiores que zero.
3. Atualizar o tamanho do renderer sem distorcer a cena.
4. Atualizar a proporção da câmera quando a câmera utilizada exigir isso.
5. Atualizar a matriz de projeção quando aplicável.
6. Verificar enquadramento, recorte e qualidade.

Não assumir que mudar apenas o CSS do canvas redimensiona corretamente a renderização interna.

### 7.3 Renderização e consumo

Avaliar:

- Quantidade de objetos e chamadas de desenho.
- Complexidade da geometria.
- Materiais e transparências.
- Resolução e quantidade de texturas.
- Iluminação e sombras.
- Pós-processamento.
- Resolução do canvas.
- Frequência de atualização.
- Dispositivos gráficos de menor capacidade.

Não aumentar a resolução de renderização sem necessidade. Uma tela com alta densidade de pixels pode multiplicar o número de pixels processados. Definir limites adequados e medir a qualidade resultante.

### 7.4 Ciclo de vida e liberação de recursos

Quando a cena deixa de ser utilizada, o agente deve encerrar o que criou:

- Cancelar loops de animação.
- Remover listeners.
- Desconectar observers.
- Liberar geometrias, materiais e texturas que não serão reutilizados.
- Encerrar controles e loaders quando aplicável.
- Remover elementos do DOM.
- Evitar manter referências que impeçam a coleta de lixo.

Remover um objeto da cena não significa necessariamente liberar os recursos gráficos associados.

### 7.5 Carregamento e falhas

Uma cena deve prever:

- Estado de carregamento.
- Progresso, quando disponível e útil.
- Falha ao buscar arquivos.
- Arquivo inválido ou incompatível.
- Falta de suporte gráfico.
- Cancelamento ou saída da seção.
- Alternativa sem 3D.

O conteúdo principal não deve depender de uma cena 3D carregar para se tornar acessível.

---

## 8. Blender e preparação de ativos 3D

O Blender é uma ferramenta de criação e preparação de conteúdo 3D. Um arquivo visualmente bonito no Blender pode ser inadequado para a web por excesso de polígonos, texturas grandes, materiais incompatíveis ou estrutura de cena desnecessária.

Antes de exportar, avaliar:

- Escala e orientação.
- Origem e pivô dos objetos.
- Aplicação de transformações quando necessária.
- Topologia e quantidade de polígonos.
- Materiais e número de materiais.
- UVs.
- Resolução e formato das texturas.
- Animações e esqueletos.
- Objetos ocultos ou não utilizados.
- Nomes e organização.
- Direitos de uso dos recursos.

### 8.1 Exportação

GLTF/GLB são formatos comuns para entrega de cenas e modelos 3D em aplicações web. O agente deve escolher as opções de exportação conforme o conteúdo e o destino, e verificar o resultado em um visualizador ou na aplicação real.

Não presumir que toda funcionalidade do Blender será preservada exatamente da mesma forma após exportação. Materiais, iluminação, modificadores e recursos específicos podem ter diferenças.

### 8.2 Compressão

Conhecer as finalidades e limitações de:

- Draco para compressão de geometria.
- Meshopt para otimização e compressão de dados de malha.
- KTX2/Basis para entrega eficiente de texturas, quando compatível.

Compressão pode reduzir transferência, mas também introduzir etapas de decodificação, dependências e diferenças de qualidade. Verificar suporte, custo e resultado no ambiente-alvo.

---

## 9. Vídeos e experiências audiovisuais

### 9.1 Escolher vídeo quando fizer sentido

Vídeo pode ser adequado para uma sequência visual previamente definida, especialmente quando não é necessário interagir com cada objeto individualmente.

Three.js pode ser mais adequado quando a pessoa precisa explorar, manipular ou visualizar o objeto em tempo real.

Image sequence pode ser útil quando o controle preciso por quadro é essencial, mas pode exigir muita memória e transferência.

A decisão deve considerar objetivo, qualidade, controle, peso, compatibilidade e desempenho.

### 9.2 Reprodução controlada pelo scroll

Ao sincronizar vídeo e scroll:

- Verificar suporte do navegador ao codec e ao formato.
- Considerar que busca por tempo pode não ser instantânea.
- Tratar `seek` e atualização de quadro sem presumir execução imediata.
- Não depender de autoplay com áudio.
- Considerar políticas de reprodução automática dos navegadores.
- Evitar downloads desnecessários de vídeos longos.
- Oferecer poster ou alternativa enquanto o vídeo carrega.
- Evitar que o scroll fique bloqueado esperando mídia.
- Testar em dispositivos reais e navegadores relevantes.

Não prometer sincronização perfeita quadro a quadro em todo dispositivo: decodificação, buffer e busca variam.

### 9.3 Entrega e formatos

Escolher formato, codec, resolução e bitrate com base nos navegadores e dispositivos-alvo. Considerar poster, preload, lazy loading e streaming quando aplicáveis.

Não baixar automaticamente vários arquivos grandes para escolher depois. A estratégia de seleção deve evitar transferência desnecessária.

---

## 10. Image Sequences

Uma image sequence é uma série ordenada de imagens que representam quadros sucessivos de uma animação.

Pode oferecer controle explícito sobre os quadros, mas o custo pode ser elevado: dezenas ou centenas de arquivos, transferência de rede, decodificação e memória.

Antes de escolher:

- Estimar quantidade de quadros.
- Medir dimensões e peso total.
- Escolher formatos apropriados.
- Definir estratégia de carregamento.
- Evitar carregar todos os quadros de uma vez quando isso não for necessário.
- Prever quadros ainda não carregados.
- Testar velocidade de busca e consumo de memória.
- Comparar com vídeo e 3D em tempo real.

A experiência deve continuar utilizável quando a sequência não estiver totalmente carregada.

---

## 11. Integração com frameworks e ciclo de vida

Ao integrar GSAP ou Three.js com React ou outro framework:

- Respeitar o ciclo de vida dos componentes.
- Criar recursos apenas quando o elemento necessário existir.
- Evitar criar uma instância nova a cada renderização sem necessidade.
- Limpar timelines, listeners, observers, render loops e recursos.
- Evitar manipular o mesmo elemento simultaneamente por múltiplos sistemas sem coordenação.
- Manter referências estáveis para recursos que precisam persistir.
- Prevenir atualizações de estado desnecessárias em cada quadro.
- Não acessar elementos do DOM antes de estarem disponíveis.

Em React, por exemplo, o agente deve compreender efeitos, referências e desmontagem de componentes. Não basta colocar toda a lógica de animação dentro de um efeito sem considerar dependências e limpeza.

A integração deve seguir a documentação da versão instalada e os padrões do projeto.

---

## 12. Performance: medir antes de otimizar

Performance não é uma impressão subjetiva. É necessário identificar o gargalo e medir o comportamento.

### 12.1 Dimensões de avaliação

- Tempo até o conteúdo principal aparecer.
- Peso transferido pela rede.
- Tempo de execução de JavaScript.
- Frequência e estabilidade de quadros.
- Uso de CPU e GPU.
- Memória da aplicação e memória gráfica, quando observável.
- Quantidade de recursos simultâneos.
- Comportamento em dispositivos de menor capacidade.
- Impacto no restante da página.

### 12.2 Estratégias possíveis

- Carregamento sob demanda.
- Lazy loading.
- Divisão de código.
- Redução de texturas.
- Compressão de modelos.
- Redução de resolução de renderização.
- Limitação de efeitos e sombras.
- Pausa quando fora da área visível.
- Uso de `requestAnimationFrame` de forma controlada.
- Redução de trabalho por quadro.
- Reutilização de recursos.
- Alternativas estáticas ou em vídeo.

Cada otimização deve preservar o objetivo e ser medida. Não aplicar uma técnica apenas porque aparece em uma lista de boas práticas.

### 12.3 Evitar trabalho desnecessário

Não manter uma cena renderizando continuamente se nada está mudando e não existe necessidade de atualização. Considerar renderização sob demanda quando adequada.

Evitar criar múltiplos loops de animação para a mesma cena. Coordenar atualizações de câmera, controles e renderização.

---

## 13. Acessibilidade e respeito às preferências

Experiências criativas precisam continuar acessíveis.

O agente deve:

- Respeitar `prefers-reduced-motion`.
- Oferecer uma alternativa quando movimento intenso puder causar desconforto.
- Não transmitir informação exclusivamente por animação, cor ou som.
- Não esconder conteúdo essencial atrás de uma interação impossível por teclado.
- Garantir foco visível e ordem de navegação coerente.
- Disponibilizar controles acessíveis para pausar ou interromper movimento quando necessário.
- Evitar animações que bloqueiem leitura ou interação.
- Garantir que textos e controles mantenham contraste e legibilidade.
- Fornecer alternativas textuais ou visuais para conteúdo audiovisual quando necessário.

A preferência por movimento reduzido deve mudar o comportamento da experiência, não apenas remover uma classe CSS sem avaliar o resultado.

---

## 14. Segurança, procedência e confiabilidade

Embora exista uma área própria de Segurança, esta Skill deve aplicar cuidados específicos:

- Verificar origem e confiança de modelos, texturas, vídeos, fontes e bibliotecas.
- Avaliar licenças e permissões de uso.
- Não executar scripts ou arquivos desconhecidos sem avaliação.
- Não inserir credenciais em código do frontend.
- Não confiar em nomes, extensões ou metadados de arquivos como prova de segurança.
- Tratar arquivos enviados por usuários como entrada não confiável.
- Evitar dependências desnecessárias e verificar vulnerabilidades conforme o processo do projeto.
- Não carregar conteúdo remoto arbitrário sem avaliar origem, política de segurança e impacto.
- Prever falhas de rede e arquivos corrompidos.

A otimização nunca deve remover verificações de segurança necessárias.

---

## 15. Critérios de escolha: qual tecnologia usar?

O agente deve comparar as opções, não escolher automaticamente a tecnologia mais complexa.

| Necessidade | Opções a avaliar |
|---|---|
| Transição simples de interface | CSS |
| Sequência de movimentos coordenados | CSS ou GSAP |
| Animação ligada ao scroll | CSS ou GSAP/ScrollTrigger |
| Objeto 3D explorável | Three.js ou solução equivalente |
| Cena 3D previamente renderizada | Vídeo ou image sequence |
| Produto com interação em tempo real | Three.js, conforme a necessidade |
| Movimento decorativo leve | CSS, SVG ou JavaScript |
| Conteúdo audiovisual linear | Vídeo |
| Controle explícito de quadros | Image sequence ou vídeo, conforme o teste |

Essa tabela é um ponto de partida. O agente deve justificar a decisão com os requisitos concretos do projeto.

---

## 16. Testes e validação

A validação deve corresponder ao que foi implementado.

### 16.1 Testes funcionais

Verificar:

- A experiência inicia corretamente.
- Os controles respondem.
- O movimento termina ou pode ser interrompido conforme planejado.
- Não há interação bloqueada.
- A navegação continua funcionando.
- Falhas de carregamento são tratadas.
- A experiência pode ser reiniciada quando necessário.

### 16.2 Testes responsivos

Testar diferentes larguras e alturas, proporções, orientações e mudanças de dimensão do contêiner. Incluir, quando fizer parte do público, celulares, tablets, desktops e dispositivos dobráveis.

Não limitar os testes a três larguras fixas. Verificar também larguras intermediárias e situações em que o conteúdo muda de forma.

### 16.3 Testes de acessibilidade

Verificar:

- Navegação por teclado.
- Foco visível.
- Ordem de leitura.
- Movimento reduzido.
- Controles de pausa.
- Conteúdo alternativo.
- Contraste e legibilidade.

### 16.4 Testes de desempenho

Medir o comportamento em condições representativas. Registrar dispositivo, navegador, versão, conexão e método quando esses dados estiverem disponíveis.

Não afirmar que o site funciona em todos os aparelhos com base em uma única máquina.

### 16.5 Testes de integração

Verificar se a experiência:

- Não conflita com outras animações.
- Não quebra o layout.
- Não duplica listeners ou render loops.
- Não deixa recursos ativos após desmontagem.
- Não interfere no funcionamento de outros componentes.

### 16.6 Registro de evidências

Para cada afirmação relevante, registrar evidência compatível:

| Afirmação | Evidência esperada |
|---|---|
| "A animação funciona" | Execução observada no cenário descrito |
| "É responsiva" | Testes em dimensões e condições representativas |
| "Respeita movimento reduzido" | Verificação com a preferência ativada |
| "O modelo foi otimizado" | Comparação de peso, recursos e comportamento |
| "Não há erro de console" | Console observado durante os fluxos testados |
| "Está pronta para produção" | Critérios de aceite, testes e revisão concluídos |

Se a ferramenta de teste não estiver disponível, registrar a limitação e indicar o teste pendente.

---

## 17. Documentação técnica e padrão de ensino

A documentação produzida ou consultada por esta Skill deve ser compreensível para uma pessoa iniciante e operacional para um agente de programação.

Para cada assunto técnico relevante, explicar, conforme aplicável:

1. **Definição:** o que é.
2. **Problema:** qual necessidade resolve.
3. **Fundamento:** como funciona.
4. **Contexto:** quando é adequado utilizar.
5. **Pré-requisitos:** o que precisa existir.
6. **Implementação:** como fazer corretamente.
7. **Código:** exemplo funcional e comentado.
8. **Integração:** como se conecta ao restante do projeto.
9. **Erros comuns:** o que pode dar errado e por quê.
10. **Diagnóstico:** como localizar a causa.
11. **Correção:** como resolver sem criar novos problemas.
12. **Desempenho:** quais recursos consome.
13. **Responsividade:** como reage a diferentes contextos.
14. **Acessibilidade e segurança:** quais cuidados são necessários.
15. **Validação:** como provar que funciona.
16. **Alternativas:** quais outras soluções existem.
17. **Limitações:** o que não resolve.
18. **Referências:** quais fontes sustentam as informações.

Não preencher tópicos artificialmente quando não forem relevantes. Explicar por que determinado aspecto não se aplica quando isso for importante para a decisão.

### 17.1 Exemplos de código

Todo exemplo deve:

- Ter objetivo explícito.
- Informar as dependências necessárias.
- Indicar onde o código deve ser colocado.
- Usar nomes compreensíveis.
- Explicar as partes importantes.
- Tratar limpeza e erros quando aplicável.
- Evitar APIs inventadas.
- Ser compatível com a versão declarada ou identificar que é pseudocódigo.

Não apresentar pseudocódigo como se fosse código pronto para produção.

### 17.2 Fontes e atualização

Priorizar documentação oficial da tecnologia e especificações relevantes. Usar artigos de terceiros como complemento, não como substituto automático da fonte primária.

Registrar, quando possível:

- Título da fonte.
- URL.
- Tecnologia e versão a que se refere.
- Data de consulta ou verificação.
- Afirmação sustentada.
- Limitações conhecidas.

Se a documentação consultada for de outra versão, declarar isso. Não afirmar que uma API está atualizada sem verificar.

---

## 18. Organização futura do conhecimento

O `SKILL.md` é a porta de entrada e o contrato operacional. Documentos especializados podem aprofundar tecnologias e procedimentos sem tornar a entrada confusa.

Estrutura sugerida para expansão:

```text
creative-development/
├── SKILL.md
├── conhecimento/
│   ├── gsap/
│   │   ├── fundamentos.md
│   │   ├── timelines.md
│   │   └── scroll-trigger.md
│   ├── threejs/
│   │   ├── fundamentos.md
│   │   ├── cameras-e-renderer.md
│   │   ├── materiais-e-texturas.md
│   │   └── performance-e-memoria.md
│   ├── blender/
│   │   ├── preparacao-de-modelos.md
│   │   └── exportacao-web.md
│   ├── modelos-3d/
│   │   ├── gltf-glb.md
│   │   └── compressao.md
│   ├── videos/
│   │   ├── formatos-e-codecs.md
│   │   ├── videos-responsivos.md
│   │   └── scroll-video.md
│   ├── image-sequences/
│   │   └── carregamento-e-sincronizacao.md
│   ├── integracoes/
│   │   ├── gsap-threejs.md
│   │   └── gsap-react.md
│   └── responsividade-criativa/
│       └── estrategias.md
├── exemplos/
│   ├── animacoes/
│   ├── experiencias-3d/
│   └── experiencias-audiovisuais/
└── referencias/
    └── fontes-oficiais.md
```

Esta árvore é uma proposta de expansão. Não presumir que os arquivos listados já existem. Ao criar novos documentos, manter links relativos corretos e evitar duplicar regras que pertencem a outras Skills.

---

## 19. Critérios de julgamento da própria implementação

Antes de considerar uma entrega concluída, avaliar:

### Objetivo e experiência

- A solução atende ao objetivo?
- O movimento tem finalidade?
- A experiência é compreensível?
- O conteúdo essencial permanece acessível?

### Qualidade técnica

- A implementação respeita a arquitetura existente?
- As dependências são justificadas?
- O ciclo de vida e a limpeza estão corretos?
- Os erros e estados alternativos foram tratados?

### Responsividade e acessibilidade

- O comportamento se adapta ao espaço disponível?
- Há testes em condições representativas?
- Movimento reduzido foi considerado?
- Teclado, toque e controles são utilizáveis?

### Desempenho e segurança

- Os custos foram avaliados?
- O carregamento é razoável?
- Recursos são liberados?
- Arquivos e dependências têm origem confiável?

### Evidências e documentação

- Os testes foram executados?
- Os resultados estão registrados?
- As limitações estão declaradas?
- As fontes técnicas são rastreáveis?

Uma resposta negativa em um requisito essencial impede a aprovação até que o problema seja resolvido ou formalmente aceito como limitação.

---

## 20. Formato recomendado de entrega do agente

Ao concluir uma tarefa, apresentar um resumo organizado:

```text
OBJETIVO
O que a experiência deveria alcançar.

ANÁLISE DO PROJETO
Arquivos, tecnologias e padrões relevantes encontrados.

DECISÃO TÉCNICA
Solução escolhida, alternativas consideradas e justificativa.

IMPLEMENTAÇÃO
Arquivos criados ou modificados e o que mudou.

RESPONSIVIDADE E ACESSIBILIDADE
Comportamentos implementados e cenários avaliados.

PERFORMANCE E SEGURANÇA
Custos, otimizações e riscos considerados.

TESTES E EVIDÊNCIAS
Comandos executados, ambientes, resultados e limitações.

PENDÊNCIAS
O que ainda precisa de validação ou decisão.
```

Não preencher esse relatório com afirmações genéricas. Cada item deve descrever o trabalho real.

---

## 21. Regras finais e inegociáveis

1. Não alterar o projeto sem analisá-lo primeiro.
2. Não escolher tecnologia sem justificar.
3. Não utilizar efeitos apenas para parecer sofisticado.
4. Não presumir que 3D, GSAP ou vídeo são sempre a melhor solução.
5. Não criar versões por resolução sem avaliar adaptação.
6. Não confundir responsividade com redução proporcional de tamanho.
7. Não ignorar mudanças de orientação ou dimensão do contêiner.
8. Não deixar recursos gráficos e listeners ativos sem necessidade.
9. Não sacrificar acessibilidade em nome de estética.
10. Não comprometer conteúdo ou navegação para manter uma animação.
11. Não confiar automaticamente em ativos gerados por IA ou obtidos de terceiros.
12. Não ignorar licenças e procedência.
13. Não declarar testes que não foram executados.
14. Não tratar hipótese como fato.
15. Não inventar APIs, parâmetros ou resultados.
16. Não duplicar responsabilidades de outras Skills.
17. Não adicionar dependências sem avaliar custo e manutenção.
18. Não esconder limitações técnicas.
19. Não considerar uma experiência pronta apenas porque funciona em um dispositivo.
20. Sempre justificar decisões relevantes e deixar evidências verificáveis.

---

## 22. Referências oficiais para consulta

Consultar a documentação correspondente à versão utilizada no projeto. Os links abaixo são pontos de partida, não prova de que uma funcionalidade específica é compatível com todos os ambientes.

- GSAP: https://gsap.com/docs/
- ScrollTrigger: https://gsap.com/docs/v3/Plugins/ScrollTrigger/
- Three.js: https://threejs.org/docs/
- MDN Web Docs: https://developer.mozilla.org/
- WebGL: https://developer.mozilla.org/en-US/docs/Web/API/WebGL_API
- Resize Observer API: https://developer.mozilla.org/en-US/docs/Web/API/Resize_Observer_API
- Web Content Accessibility Guidelines: https://www.w3.org/WAI/standards-guidelines/wcag/
- WAI-ARIA: https://www.w3.org/WAI/ARIA/
- Blender Manual: https://docs.blender.org/manual/
- glTF: https://www.khronos.org/gltf/
- React: https://react.dev/

---

**Fim do contrato operacional do Creative Development.**

Este documento define como a Skill deve pensar, planejar, implementar, avaliar e comunicar seu trabalho. Os guias especializados deverão aprofundar cada tecnologia sem contradizer estas regras.
