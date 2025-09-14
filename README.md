Desafio de Projeto DIO: Orquestrando Fluxos de Trabalho com AWS Step Functions
Este repositório documenta a conclusão do desafio de projeto da DIO, que tem como objetivo aprofundar o conhecimento em AWS Step Functions.

O projeto prático consistiu na construção de um fluxo de trabalho automatizado para simular o processo de um pedido, utilizando os serviços da AWS para orquestrar as etapas de validação, processamento de pagamento e confirmação.

🚀 Arquitetura do Projeto
O fluxo de trabalho foi construído usando o AWS Step Functions para orquestrar a execução de três funções AWS Lambda distintas. Cada função representa uma etapa específica no processamento do pedido:

ValidateOrderFunction: Responsável por validar os dados de entrada do pedido.

ProcessPaymentFunction: Simula o processamento do pagamento.

ConfirmOrderFunction: Confirma o pedido após o pagamento ser concluído com sucesso.

A imagem abaixo ilustra a arquitetura visual do fluxo de trabalho conforme configurado no console da AWS:

🛠️ Passo a Passo da Implementação
A seguir, estão os passos detalhados para a criação deste fluxo de trabalho:

Criação das Funções Lambda:

Três funções foram criadas no console da AWS Lambda: ValidateOrderFunction, ProcessPaymentFunction e ConfirmOrderFunction.

Para cada função, foi utilizado o runtime Python 3.9.

O código Python para cada etapa foi inserido e salvo com sucesso.

Configuração da Máquina de Estados (Step Functions):

No console do AWS Step Functions, foi criada uma nova máquina de estados com o nome OrderProcessingStateMachine.

O design visual foi usado para arrastar e conectar as três ações "Lambda Invoke" na ordem correta.

Cada ação foi configurada para chamar uma das funções Lambda criadas.

Execução e Validação:

A máquina de estados foi executada, fornecendo um JSON de entrada para simular um novo pedido ({"orderId": "12345"}).

O fluxo de trabalho foi monitorado e todas as etapas foram concluídas com êxito, confirmando o sucesso da orquestração.

💡 Anotações e Insights
Durante a realização deste desafio, adquiri os seguintes conhecimentos e insights:

Orquestração vs. Funções Avulsas: A principal vantagem do AWS Step Functions é a capacidade de orquestrar múltiplos serviços da AWS. Isso simplifica a gestão de fluxos de trabalho complexos, em oposição a encadear chamadas de função manualmente, o que pode levar a erros e dificultar o monitoramento.

Monitoramento e Visualização: A interface visual do Step Functions é extremamente útil. Ela permite acompanhar o progresso de cada etapa em tempo real, facilitando a identificação de gargalos ou falhas no fluxo.

Tratamento de Erros: O Step Functions oferece recursos robustos para tratamento de erros, novas tentativas e escolhas condicionais, tornando os fluxos de trabalho mais resilientes.

Valor na Prática: A aplicação deste conceito em um cenário real, como o processamento de um pedido, demonstra o poder de automatização e como essa ferramenta pode ser usada para construir sistemas mais eficientes e confiáveis.

![Descrição da imagem](images/trabalhoooo.png)

Feito por
Bruna Macedo
