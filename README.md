Projeto do Desafio de Projeto da DIO: uso de IA como ferramenta de aprendizagem ativa:

🔗 [Caderno no NotebookLM](https://notebook.google.com/notebook/b08b7f95-dd49-4266-8aa1-9a96139289a4)

## 🎯 Contexto e Objetivos

O tema escolhido foi **Ada Lovelace**, matemática britânica do século XIX considerada uma das pioneiras da programação. Como estudante de Análise e Desenvolvimento de Sistemas, quis entender as origens da computação e o papel dela na história da tecnologia.

**Objetivos de estudo:**
- Entender quem foi Ada Lovelace e em que contexto histórico viveu
- Compreender a relação dela com Charles Babbage e a Máquina Analítica
- Entender por que a Nota G é considerada o primeiro programa de computador publicado
- Praticar curadoria de fontes e uso crítico de IA (conferir as respostas nas fontes)

## 📚 Curadoria de Fontes

O caderno reúne 28 fontes. As 5 principais, todas abertas e em texto:

1. [Charles Babbage, Ada Lovelace, and the Bernoulli Numbers](https://coe.psu.ac.th/ad/cabbage/cabbage.pdf): artigo acadêmico (arXiv) sobre o algoritmo da Nota G.
2. [Sketch of the Analytical Engine Invented by Charles Babbage](https://www.fourmilab.ch/babbage/sketch.html): tradução de Ada com as Notas originais.
3. [Menabrea (1842)](https://www.christies.com/en/lot/lot-4443501): o texto original que Ada traduziu.
4. [Untangling the Tale of Ada Lovelace](https://writings.stephenwolfram.com/2015/12/untangling-the-tale-of-ada-lovelace/): análise histórica de Stephen Wolfram.
5. [Note G](https://en.wikipedia.org/wiki/Note_G): visão geral da Nota G (Wikipedia).

## 🧪 Engenharia de Prompts e "Cicatrizes"

### Prompt 1: O algoritmo da Nota G
- **Pergunta:** `Explique o algoritmo da Nota G passo a passo, citando de qual fonte vem cada afirmação.`
- **Resposta obtida (resumo):** O NotebookLM explicou que o algoritmo calcula números de Bernoulli (o exemplo da Nota G calcula o B7, com n = 4). Descreveu como Ada organizou o Depósito da máquina em constantes, entrada, variáveis de trabalho e resultados, e detalhou a tabela de 25 operações em 4 fases: inicialização, primeiro termo, laço de repetição e encerramento. Também apontou o erro tipográfico da operação 4 na publicação de 1843.

- **Dificuldade / ajuste:** A resposta veio com fórmulas em LaTeX, que aparecem como texto cru no GitHub, então precisei convertê-las ou resumi-las.

### Prompt 2: Glossário dos termos principais
- **Pergunta:** `Crie um glossário com os 15 termos técnicos mais importantes das fontes.`
- **Resposta obtida (resumo):** O NotebookLM devolveu 15 termos com definição, entre eles Moinho (The Mill), Depósito (The Store), Engenho Analítico, Engenho de Diferenças, Ciência Poética, cartões perfurados (de operação e de variáveis), Nota G, números de Bernoulli, laços de repetição, desvio condicional, manipulação de símbolos, a notação de Ada para o histórico da memória e a Objeção de Lovelace.

- **Dificuldade / ajuste:** A resposta veio com alguns problemas que precisei revisar manualmente: (1) erros de palavra, como "Infração teórica" no lugar de algo como "intuição teórica" e "polinomials" em vez de "polinomiais"; (2) notação em LaTeX (como `\\(V_n\\)`), que aparece como texto cru no GitHub, então troquei por `V_n` simples; (3) o pedido de "15 termos" trouxe termos muito específicos, então selecionei os mais úteis para o glossário final. Isso reforçou que a resposta da IA precisa ser lida e corrigida antes de ser usada.

### Troubleshooting das fontes
Ao montar o caderno, algumas fontes (como ResearchGate, Scribd e Cantor's Paradise) falharam na importação, provavelmente por bloqueio de acesso ou paywall. Substituí por fontes abertas, como o arXiv. Também usei o Deep Research para encontrar fontes adicionais.

## 📖 Miniguia de Estudo

### Resumo estruturado

**1. Vida e formação**
- Nasceu Augusta Ada Byron em 10 de dezembro de 1815, em Londres, filha do poeta Lord Byron e de Annabella Milbanke.
- Recebeu forte educação em matemática e ciências, com tutores como Mary Somerville e Augustus De Morgan.
- Casou-se com William King, depois Conde de Lovelace, e passou a ser a Condessa de Lovelace.
- Morreu em 27 de novembro de 1852, aos 36 anos.

**2. Parceria com Charles Babbage**
- Conheceu Babbage em 1833 e se interessou por suas máquinas de calcular.
- Babbage projetou a Máquina Diferencial e depois a Máquina Analítica, um projeto de computador mecânico de uso geral (nunca concluído na época).

**3. As Notas e o primeiro programa publicado**
- Entre 1842 e 1843, traduziu para o inglês um artigo do matemático italiano Luigi Menabrea sobre a Máquina Analítica.
- Acrescentou suas próprias Notas (A a G), maiores que o texto original.
- Na Nota G, descreveu passo a passo o cálculo de números de Bernoulli, considerado o primeiro programa de computador publicado.

**4. Visão à frente do seu tempo**
- Percebeu que a máquina poderia manipular símbolos em geral, não só números (por exemplo, compor música).
- Defendeu que a máquina só executa o que for programado, ponto depois discutido por Alan Turing como a "objeção de Lady Lovelace".

**5. Legado**
- A linguagem de programação **Ada**, criada para o Departamento de Defesa dos EUA, foi batizada em sua homenagem.
- O **Ada Lovelace Day** celebra mulheres na ciência e na tecnologia, na segunda terça-feira de outubro.
### Prompts reutilizáveis

1. `Resuma o tema [TEMA] em 5 tópicos, citando as fontes de cada um.`
2. `Crie 10 perguntas de revisão sobre [TEMA], com gabarito e a fonte de cada resposta.`
3. `Explique [CONCEITO] como se eu fosse iniciante, e depois em nível técnico.`
4. `Monte uma linha do tempo com os principais eventos de [TEMA], com datas e fontes.`
5. `Compare [ITEM A] e [ITEM B] em uma tabela, indicando as fontes.`
6. `Quais pontos as minhas fontes contradizem ou deixam em aberto sobre [TEMA]?`
7. `Gere um glossário com os 15 termos mais importantes das minhas fontes.`
8. `Responda apenas com base nas fontes e diga "não consta nas fontes" quando não houver informação.`

## ✅ Aprendizados

## ✅ Aprendizados

Foi uma experiência diferente do que estou habituado: usar a Inteligência Artificial como ferramenta de estudo, e não só para pedir respostas prontas. Conheci a história de Ada Lovelace e suas contribuições para o avanço da tecnologia. Quando pensamos na área de TI, costumamos imaginar homens, mas uma das pioneiras da programação foi uma mulher, e a cada ano as mulheres vêm transformando esse mercado. Também aprendi que a IA erra e precisa ser conferida: encontrei erros de palavra e fórmulas quebradas nas respostas que precisei corrigir.

---
Feito por [Kauã Fernandes](https://github.com/kfernandws)
