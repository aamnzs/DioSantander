# DioSantander

Projeto de Dashboard com excel demonstrando evoluções de vendas do XBox

# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 13/12/2025
Empresa: Abstergo Industries 
Responsável: Arildo Alves de Menezes

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa Abstergo Industries, realizado por Arildo Alves de Menezes. O objetivo do projeto foi elencar 3 serviços AWS, com a finalidade de realizar diminuição de custos imediatos.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos especí­ficos. A seguir, serão descritas as etapas do projeto:

Etapa 1: Diagnóstico e Eliminação de Desperdícios

Nome da ferramenta: AWS Trusted Advisor

Foco da ferramenta: Identificação automática de recursos subutilizados ou ociosos para eliminação imediata de gastos desnecessários-1.

Descrição de caso de uso: Após a implantação, o Trusted Advisor pode gerar um relatório que mostra, por exemplo: instâncias EC2 com utilização de CPU abaixo de 10% nos últimos 14 dias (sugerindo redimensionamento ou desligamento)-1; volumes de armazenamento (EBS) com atividade quase nula (que podem ser excluídos após um snapshot)-1; e balanceadores de carga sem tráfego-1. Para uma fábrica, isso pode corresponder a servidores de um projeto piloto concluído, volumes de backup antigos não gerenciados ou recursos de testing ligados continuamente. A ação direta sobre essas recomendações gera economia a partir do primeiro ciclo de faturamento.

Etapa 2: Automação do Ciclo de Vida de Recursos

Nome da ferramenta: AWS Instance Scheduler

Foco da ferramenta: Agendamento automático para iniciar e parar instâncias de computação (EC2) e bancos de dados (RDS) conforme a necessidade operacional-6.

Descrição de caso de uso: Muitos ambientes não produtivos, como desenvolvimento, testes e homologação, só são necessários em horário comercial. Manter esses recursos (servidores de aplicação e bancos de dados) executando 24/7 é um custo evitável. Com o Instance Scheduler, a empresa pode configurar que todos os recursos da conta marcados com a tag Ambiente: Dev sejam desligados automaticamente às 19h e reiniciados às 7h, de segunda a sexta. Para uma empresa industrial, isso também pode ser aplicado a servidores que dão suporte a turnos de produção específicos. Esta prática pode gerar economia de até 70% no custo desses recursos-6.

Etapa 3: Otimização Inteligente de Armazenamento

Nome da ferramenta: Amazon S3 Intelligent-Tiering

Foco da ferramenta: Redução automática do custo de armazenamento de dados ao movê-los entre camadas de acesso (frequente, infrequente, arquivo) com base em padrões de uso observados-6.

Descrição de caso de uso: Indústrias geram grandes volumes de dados de longo prazo, como telemetria de sensores, logs de máquinas, vídeos de inspeção e backups de sistemas. Muitos desses arquivos são acessados com frequência apenas nos primeiros meses e depois raramente consultados. Armazená-los todos em uma camada de alto custo é ineficiente. Ao habilitar o S3 Intelligent-Tiering nos buckets existentes, o serviço monitora o acesso e move automaticamente objetos não acessados por 30 dias para uma camada de custo inferior, e após 90 dias sem acesso para uma camada de arquivamento, sem risco de custos de recuperação de dados. A economia é contínua e progressiva.

## Conclusão
A implementação de ferramentas na empresa Abstergo Industries terá como benefícios tangíveis e imediatos:

Redução de Custos Imediata: A primeira etapa gera economia imediata ao eliminar recursos que já estão sendo cobrados sem agregar valor. A automação da segunda etapa cria uma economia recorrente e previsível. Juntas, elas atacam os dois principais vetores de desperdício em nuvem: recursos órfãos e recursos ociosos.

Otimização Contínua e Automática: A terceira etapa introduz uma otimização passiva e contínua para um dos principais custos em ambientes de dados industriais: o armazenamento. O S3 Intelligent-Tiering funciona sem necessidade de intervenção ou análise manual constante.

Cultura de Eficiência: O plano estabelece uma base prática para uma cultura de gestão financeira na nuvem (Cloud Financial Management). Ele começa com ferramentas nativas e de baixa complexidade, permitindo que as equipes de TI e engenharia ganhem visibilidade e controle sobre os custos, um princípio fundamental para a otimização de longo prazo.

Tais benefícios aumentarão a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.


Assinatura do Responsável pelo Projeto:

Arildo Alves de Menezes
