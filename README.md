## 🚀 Relatório de Implementação de Serviços AWS: Otimização de Custos Imediata 
> desafio - Bootcamp Ciências de Dados com Python - DIO Santander 2025

### 📋 Detalhes do Projeto

| Item | Descrição |
| :--- | :--- |
| **Data de Início** | **06/12/25** |
| **Empresa Cliente** | **Abstergo Industries** |
| **Responsável** | **Lincoln Hernandes** |

---

## 💡 Introdução e Objetivo

Este relatório documenta a implementação de **três serviços AWS** estratégicos na Abstergo Industries, visando uma **redução de custos imediata** através da otimização de recursos de Custo, Armazenamento e Rede.

---

## 🌐 Descrição Detalhada da Otimização (3 Pilares)

O projeto de otimização foi estruturado em três pilares para atacar os maiores ofensores de custo da infraestrutura AWS. 

### 1️⃣ Etapa 1: Otimização de Capacidade de Computação

| Detalhe | Serviço AWS | Foco da Otimização |
| :--- | :--- | :--- |
| **Nome da Ferramenta** | **AWS Compute Optimizer** | Dimensionamento Correto (*Right-Sizing*) e eliminação de recursos de CPU/Memória ociosos. |
| **Foco** | **EC2** | Garantir que as instâncias EC2 e volumes EBS provisionados estejam alinhados com a demanda real da carga de trabalho. |
| **Caso de Uso** | Análise de métricas de uso e redimensionamento de instâncias **EC2** subutilizadas de planos maiores para menores (ex: de `m5.large` para `m5.medium`), gerando economia no custo horário de computação. |

### 2️⃣ Etapa 2: Gerenciamento Inteligente de Armazenamento

| Detalhe | Serviço AWS | Foco da Otimização |
| :--- | :--- | :--- |
| **Nome da Ferramenta** | **Amazon S3 Intelligent-Tiering** | Movimentação automática e inteligente de objetos entre classes de armazenamento. |
| **Foco** | **S3** | Mudar o custo de armazenamento de quente para frio, de forma automatizada, conforme o padrão de acesso aos dados. |
| **Caso de Uso** | Implementação em *buckets* de *logs* e *backups*. Objetos que não são acessados por 30 dias são movidos para a camada **Standard-IA (Infrequent Access)**, reduzindo o custo de armazenamento sem a necessidade de definir políticas de ciclo de vida manuais. |

### 3️⃣ Etapa 3: Redução de Custos de Rede e Distribuição

| Detalhe | Serviço AWS | Foco da Otimização |
| :--- | :--- | :--- |
| **Nome da Ferramenta** | **Amazon CloudFront** | Utilização como Content Delivery Network (CDN) para cache global. |
| **Foco** | **Transferência de Dados de Saída (DTO)** | Reduzir os custos de DTO, pois o custo por GB do CloudFront é menor que o custo de DTO direto do S3 ou EC2. |
| **Caso de Uso** | Configuração do CloudFront como *front-end* para o S3. O conteúdo estático é **armazenado em cache** nos *edge locations* da AWS, diminuindo a carga na origem (S3) e, mais importante, reduzindo a quantidade de dados que o S3 precisa transferir para o público, economizando significativamente nos custos de rede. |

---

## 🎯 Conclusão

A implementação estratégica das ferramentas **AWS Compute Optimizer (EC2/EBS)**, **Amazon S3 Intelligent-Tiering** e **Amazon CloudFront** na Abstergo Industries tem como esperado **maximizar o uso dos recursos e reduzir os custos de transferência de dados**, impactando positivamente a linha de custos da infraestrutura.

Recomenda-se a continuidade da utilização das ferramentas implementadas para manter o controle da **eficiência e produtividade** e explorar novas oportunidades de otimização contínua.

---

## 📎 Referências

* AMAZON WEB SERVICES. Guia do Usuário do AWS Compute Optimizer. [S. l.: AWS], 2024. Disponível em: [https://docs.aws.amazon.com/pt_br/compute-optimizer/latest/ug/whats-it-do.html]. Acesso em: 6 dez. 2025.
* AMAZON WEB SERVICES. Classes de armazenamento do Amazon S3: S3 Intelligent-Tiering. [S. l.: AWS], 2024. Disponível em: [https://aws.amazon.com/pt/s3/storage-classes/intelligent-tiering/]. Acesso em: 6 dez. 2025.
* AMAZON WEB SERVICES. O que é o Amazon CloudFront?. [S. l.: AWS], 2024. Disponível em: [https://docs.aws.amazon.com/pt_br/AmazonCloudFront/latest/DeveloperGuide/Introduction.html]. Acesso em: 6 dez. 2025.

---

### Assinatura do Responsável pelo Projeto

___________________________________________________
**Lincoln Hernandes**
