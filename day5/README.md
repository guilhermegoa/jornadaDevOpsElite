# Day 4

## Prometheus - Grafana

### Resumo

**Métricas** são medidas quantitativas que servem para avaliar e medir determinado aspecto de um processo, sistema ou projeto. Elas podem ser usadas para avaliar o desempenho, a qualidade, a eficiência, a produtividade e outros aspectos. Algumas métricas comuns incluem o tempo de resposta, o número de erros, o número de usuários ativos, a taxa de conversão, o custo por unidade, entre outras. As métricas são úteis para identificar problemas, monitorar tendências, estabelecer metas e avaliar o sucesso de uma iniciativa.

**Prometheus** é uma plataforma de monitoramento de sistemas e aplicações de código aberto. Ele fornece uma linguagem de consulta (PromQL) para recuperar e analisar dados de métricas, armazenando-os em seu banco de dados de série temporal. Ele também oferece uma interface web para visualizar e alertar sobre esses dados. Prometheus é projetado para ser escalável e tolerante a falhas, e pode ser facilmente integrado a outras ferramentas de monitoramento e gerenciamento de infraestrutura. Além disso, ele permite a configuração de alertas baseados em regras, que são acionadas quando as métricas atingem determinados limiares, para que as equipes de operação possam tomar medidas preventivas.

**Prometheus arquitetura:**

- Prometheus Server: responsável por coletar métricas de aplicações e sistemas, armazenar essas métricas em um banco de dados e fornecer uma interface web para visualizar e alertar sobre esses dados.
  - Time Series Database: banco de dados de série temporal que armazena métricas.
  - Storage: armazena os dados coletados pelo Prometheus Server.
  - PromQL: linguagem de consulta para recuperar e analisar dados de métricas.
- Jobs: aplicações e sistemas que fornecem métricas para o Prometheus Server.
- Exporters: biblioteca que permite que aplicações e sistemas forneçam métricas.
- Push Gateway: servidor que permite que os jobs enviem métricas para o Prometheus Server.
- Service Discovery: mecanismo que permite que o Prometheus Server descubra os jobs automaticamente.
- Web UI: interface web para visualizar e alertar sobre os dados coletados.
- Alert Manager: servidor que permite a configuração de alertas baseados em regras.
