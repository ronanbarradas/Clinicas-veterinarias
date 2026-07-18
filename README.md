# Soluções em Python

Este repositório reúne notebooks desenvolvidos em Python para automatizar atividades, tratar dados e apoiar processos analíticos utilizados durante minha atuação como Analista de Dados. Todos os dados sensíveis foram modificados com a biblioteca _Faker_ do python objetivando preservar a identidade dos envolvidos. O único objetivo aqui é didático.

Os projetos contemplam diferentes desafios do dia a dia, como limpeza e transformação de dados, integração de informações provenientes de múltiplas fontes, geração de bases para análise, automatização de tarefas repetitivas e otimização de processos. Sempre que necessário, dados sensíveis e informações confidenciais foram removidos ou anonimizados, preservando apenas a estrutura e a lógica das soluções.

O objetivo deste repositório é documentar parte da minha experiência prática com Python, demonstrando a aplicação da linguagem na resolução de problemas reais e na criação de soluções que aumentam a eficiência operacional e apoiam a tomada de decisões baseada em dados.
____

Levando em conta que tenho o _baseclientes.xlsx_ com toda a base de clientes do plano de saúde, em _Relatório_SAC.ipynb_ temos três códigos python que eu utilizava no Google Collab. A seguir eu explico todo o procedimento:
- Pego o _basesac.xlsx_, esse arquivo vem com todos os clientes atendidos no dia anterior pelo plano de saúde.
- Subo _basesac.xlsx_ e _baseclientes.xlsx_ no notebook do Collab onde estão os códigos.
- Executo o primeiro código, este vai cruzar os dois arquivos upados usando a função merge do pandas vai gerar o _Atendimentos_do_dia.xlsx_, que é um relatório detalhado dos atendimentos do dia anterior dividido por clientes, com os seus dados, quantos e quais os procedimentos utilizados além do número total de procedimentos. Esse código é necessário pois em nenhuma database tem todos os dados do cliente.
- Agora se executa o segundo código, este totalmente baseado em _Atendimentos_do_dia.xlsx_ e é basicamente um resumo desse. Esse extrai apenas o nome do cliente, do animal e o número de telefone e gera o arquivo _clientes.xlsx_. Esse serve apenas para simplificar e auxiliar a visualização dos clientes e de seus contatos.
- Por fim, executa-se o terceiro código que lê o recém criado _clientes.xlsx_ para criar as mensagens que serão enviadas aos tutores dos pets atendidos, também lê o _baseclientes.xlsx_ para definir o gênero do artigo utilizado antes do nome do pet. É gerado o _mensagens_automatizadas.txt_ que são as mensagens prontas para o envio para o tutor correspondente
