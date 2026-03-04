# ☁️ RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

<div align="center">

![AWS](https://img.shields.io/badge/Amazon_AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen?style=for-the-badge)
![Empresa](https://img.shields.io/badge/Empresa-Abstergo_Industries-blue?style=for-the-badge)

</div>

---

## 📋 Informações do Projeto

| Campo | Detalhes |
|-------|----------|
| 📅 **Data de Início** | 04 de Março de 2026 |
| 🏢 **Empresa** | Abstergo Industries |
| 👤 **Responsável** | John Mitchell — Arquiteto de Soluções Cloud |
| 🎯 **Objetivo** | Redução imediata de custos operacionais com migração para AWS |

---

## 📌 Introdução

Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **John Mitchell**. O objetivo do projeto foi elencar **3 serviços AWS estratégicos** com a finalidade de promover a **redução imediata de custos** operacionais, eliminando gastos com infraestrutura física desnecessária e otimizando o consumo de recursos de TI.

A iniciativa faz parte do plano de modernização tecnológica da empresa, alinhando-se às melhores práticas de arquitetura em nuvem e ao modelo de pagamento por uso (*pay-as-you-go*) da AWS.

---

## 🚀 Descrição do Projeto

O projeto de implementação foi dividido em **3 etapas sequenciais**, cada uma endereçando um ponto de alto custo identificado no diagnóstico inicial da infraestrutura da empresa.

---

### 🔹 Etapa 1 — Amazon EC2 com Auto Scaling

**Ferramenta:** Amazon EC2 (Elastic Compute Cloud)  
**Foco:** Substituição de servidores físicos e otimização de capacidade computacional  

**Caso de Uso:**  
A Abstergo Industries mantinha um conjunto de servidores físicos on-premises que operavam com baixa utilização média (~20% de capacidade), gerando custos fixos elevados com energia, refrigeração e manutenção de hardware.

A migração para instâncias EC2 com **Auto Scaling** permitiu que a empresa pagasse apenas pela capacidade computacional efetivamente utilizada. Nos períodos de baixa demanda, as instâncias são reduzidas automaticamente; nos picos, escalam horizontalmente sem intervenção manual.

> 💰 **Economia estimada:** Redução de até **65% nos custos** de infraestrutura computacional nos primeiros 3 meses.

---

### 🔹 Etapa 2 — Amazon S3 com Intelligent-Tiering

**Ferramenta:** Amazon S3 (Simple Storage Service)  
**Foco:** Substituição de storages físicos e repositórios de arquivos locais  

**Caso de Uso:**  
A empresa possuía múltiplos NAS (Network Attached Storage) físicos para armazenamento de arquivos corporativos, backups e documentos históricos. Esses dispositivos demandavam contratos de manutenção anuais e apresentavam riscos de falha de hardware.

A migração para o **Amazon S3 com Intelligent-Tiering** automatizou a movimentação de objetos entre classes de armazenamento (frequent access, infrequent access, archive) com base nos padrões reais de acesso. Arquivos raramente acessados, como registros históricos, foram automaticamente movidos para camadas mais baratas como o **S3 Glacier**.

> 💰 **Economia estimada:** Redução de **~70% no custo por GB** comparado ao armazenamento físico, com ganho adicional em durabilidade (99,999999999% — "11 noves").

---

### 🔹 Etapa 3 — AWS Lambda + Amazon RDS (Reserved Instances)

**Ferramenta:** AWS Lambda + Amazon RDS  
**Foco:** Modernização de processos batch e otimização do banco de dados  

**Caso de Uso:**  
Processos internos de relatórios, envio de notificações e integrações entre sistemas rodavam em servidores dedicados que ficavam ociosos a maior parte do tempo. Paralelamente, o banco de dados corporativo operava em hardware próprio com licença de software cara.

A adoção do **AWS Lambda** (computação serverless) eliminou completamente a necessidade de servidores para tarefas eventuais — a empresa paga apenas pelos milissegundos de execução de cada função. O banco de dados foi migrado para o **Amazon RDS** com **Reserved Instances** de 1 ano, garantindo desconto de até 40% frente ao preço sob demanda.

> 💰 **Economia estimada:** Eliminação de 100% dos custos de servidores ociosos e desconto de **40% no RDS** com o plano reservado.

---

## 📊 Resumo de Benefícios

```
┌────────────────────────────────────────────────────────────────────┐
│                     IMPACTO FINANCEIRO ESTIMADO                    │
├─────────────────────┬──────────────────────┬───────────────────────┤
│ Serviço AWS         │ Área de Impacto       │ Redução de Custo      │
├─────────────────────┼──────────────────────┼───────────────────────┤
│ EC2 + Auto Scaling  │ Servidores físicos    │ ~65%                  │
│ S3 Intelligent-Tier │ Storage local/NAS     │ ~70%                  │
│ Lambda + RDS        │ Processos e banco     │ ~40–100%              │
├─────────────────────┼──────────────────────┼───────────────────────┤
│ TOTAL GERAL         │ Infraestrutura TI     │ ≈ 55–65% do custo     │
└─────────────────────┴──────────────────────┴───────────────────────┘
```

---

## ✅ Conclusão

A implementação das ferramentas AWS na empresa **Abstergo Industries** tem como resultado esperado:

- ✔️ **Redução significativa de custos operacionais** com eliminação de hardware físico
- ✔️ **Maior escalabilidade e flexibilidade** para crescimento sem investimento antecipado em infraestrutura
- ✔️ **Alta disponibilidade e resiliência** com SLAs garantidos pela AWS
- ✔️ **Segurança aprimorada** com recursos nativos de criptografia, IAM e monitoramento via CloudWatch
- ✔️ **Liberação da equipe de TI** para focar em iniciativas estratégicas, reduzindo o tempo gasto em manutenção de hardware

Recomenda-se a **continuidade da utilização das ferramentas implementadas** e a busca por novas oportunidades de otimização, como o uso de **AWS Cost Explorer** para monitoramento contínuo de gastos, **AWS Trusted Advisor** para recomendações automáticas, e a avaliação de serviços como **Amazon CloudFront** e **AWS Organizations** para uma governança ainda mais robusta.

---

## 📎 Anexos

| # | Documento | Descrição |
|---|-----------|-----------|
| 1 | `diagnostico_infraestrutura_atual.pdf` | Levantamento da infraestrutura on-premises antes da migração |
| 2 | `planilha_comparativo_custos.xlsx` | Comparativo de custos antes e depois da migração AWS |
| 3 | `arquitetura_aws_abstergo.drawio` | Diagrama da arquitetura de nuvem implementada |
| 4 | `manual_ec2_autoscaling.pdf` | Guia de operação do EC2 com Auto Scaling |
| 5 | `politica_backup_s3.pdf` | Política de backup e retenção de dados no S3 |
| 6 | `sla_aws_contratos.pdf` | Contratos de nível de serviço e termos AWS |

---

## ✍️ Assinatura

<br>

_______________________________________________  
**John Mitchell**  
Arquiteto de Soluções Cloud  
Responsável pelo Projeto de Implementação AWS  
Abstergo Industries — Março/2026

---

<div align="center">

*Documento gerado em 04/03/2026 · Abstergo Industries · Confidencial*

</div>