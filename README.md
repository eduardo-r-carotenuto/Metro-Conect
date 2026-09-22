# MetrôBot SP 2.0

**Integrantes:** Daniel Santiago, Eduardo Carotenuto, Everton Tiburcio, Fauzer Ribeiro e Matheus Diorio.

O MetrôBot SP 2.0 foi desenvolvido para a disciplina de Inteligência Artificial e Machine Learning e reúne os principais conceitos trabalhados na Aula Prática 01, como BFS, DFS, lógica proposicional e de primeira ordem, motor de inferência e uso de modelo de linguagem. Nesta versão, o projeto foi ampliado para considerar as Linhas 1-Azul, 2-Verde e 3-Vermelha do Metrô de São Paulo, permitindo trabalhar com rotas entre 52 estações, baldeações, integrações, estações bloqueadas, acessibilidade e paralisação de linhas.

O sistema encontra rotas utilizando BFS ou DFS e também compara o esforço de cada algoritmo pelo número de estações visitadas. As integrações entre linhas são identificadas automaticamente pelo motor de inferência através da regra R6, sem serem cadastradas manualmente. Também foi criada uma nova regra, R7, para representar a paralisação de uma linha e bloquear as estações pertencentes a ela durante a busca.

Além da parte de busca e lógica, o notebook possui um intérprete e um narrador. Quando o Llama está habilitado, o intérprete transforma o pedido escrito pelo usuário em dados estruturados e o narrador apresenta a rota de forma mais natural, incluindo as baldeações. A escolha da rota, porém, continua sendo feita pelos algoritmos e pelas regras implementadas no sistema. Também foi criada uma interface com `ipywidgets`, na qual é possível selecionar origem, destino, algoritmo, acessibilidade, estações fechadas, elevadores em manutenção e linhas paralisadas.

Para executar o projeto, basta abrir o arquivo `Desafio_MetroBot_SP_2.0.ipynb` no Google Colab e rodar as células em ordem, de cima para baixo, ou utilizar a opção **Executar tudo / Run All**. Por padrão, `PROVEDOR = "offline"` na célula 2, então o notebook funciona sem internet e sem chave de API.

Caso seja desejado utilizar o Llama pelo Groq, basta alterar para `PROVEDOR = "groq"` e configurar a variável `GROQ_API_KEY` nos Secrets do Colab ou em um arquivo `.env`. Também é possível utilizar `PROVEDOR = "ollama"` para execução com um modelo local.

Ao final do notebook está disponível a função `rodar_testes()`, que executa os 6 casos obrigatórios do desafio e mais 4 casos adicionais criados pelo grupo. Os testes verificam situações como quantidade de paradas, baldeações, estações bloqueadas e possibilidade de desvios na rede. O notebook também conta com um painel interativo desenvolvido com `ipywidgets`, permitindo testar diferentes cenários diretamente pela interface.

Este notebook reaproveita tudo que foi construído na Aula Prática 01, incluindo BFS, DFS, lógica proposicional e de primeira ordem, motor de inferência, intérprete e narrador com Llama e modo offline, e estende essas funcionalidades para as três linhas do metrô, com baldeações, integrações deduzidas automaticamente pela R6 e uma nova regra criada pelo grupo na R7.

O projeto foi desenvolvido para fins acadêmicos. Informações como tempo de viagem, manutenção de elevadores, estações fechadas e paralisações são utilizadas como cenários simulados para demonstrar o funcionamento dos algoritmos e das regras implementadas.
