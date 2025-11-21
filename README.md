# 📊 Análise de Engajamento e Colaboração em Repositórios Open Source do GitHub
**Uma Investigação Sobre Padrões de Contribuição e Interação Comunitária**

Este repositório documenta um estudo aprofundado sobre os fatores que influenciam o engajamento, a participação ativa e a dinâmica de interação em projetos open source hospedados no GitHub. A pesquisa analisa **1.000 repositórios ativos**, caracterizando como popularidade, colaboração e responsividade se relacionam no ecossistema GitHub.

---

## 📌 Objetivo Geral

Investigar sistematicamente **os padrões de engajamento e colaboração** presentes em repositórios open source, examinando como popularidade, volume de contribuições e interação via issues se combinam para formar comunidades sustentáveis.

---

## 🎯 Objetivos Específicos

1. **Q1 — Popularidade × Comunidade:**  
   Verificar se o número de estrelas de um projeto prediz o tamanho da comunidade de contribuidores.

2. **Q2 — Participação Ativa:**  
   Quantificar a atividade da comunidade por meio de pull requests e commits de contribuidores externos.

3. **Q3 — Interação Comunitária:**  
   Avaliar responsividade dos mantenedores e maturidade de processos através da análise de issues.

---

## 🧭 Fundamentação Teórica

A base teórica do estudo se apoia em pesquisas da área de Engenharia de Software Social, especialmente nos eixos:

### ⭐ Métricas de Popularidade
Trabalhos anteriores indicam que o número de estrelas de um repositório representa **visibilidade social**, não engajamento direto.

### 🔍 Repositórios Ativos
A seleção utiliza critérios robustos que distinguem projetos genuinamente ativos (ex.: ≥ 5 contribuidores, ≥ 50 issues fechadas, ≥ 100 estrelas, atividade recente).

### 🤝 Contribuições Externas
Pesquisas mostram que contribuidores externos têm papel fundamental, especialmente em correções de bugs e melhorias incrementais.

### 💬 Interação e Responsividade
Tempos menores de resposta são fortemente associados a maior retenção e participação dos contribuidores.

---

## 🧪 Metodologia

### 📂 Fonte dos Dados

A coleta utilizou:

- **GitHub REST API v3**
- **GitHub GraphQL API**

Todo o processo respeitou limites de requisição, políticas de uso e privacidade dos dados.

### 🔎 Critérios de Inclusão dos Repositórios

Um repositório foi incluído apenas se atendesse **todos** os critérios abaixo:

- Idade ≥ 365 dias  
- ≥ 5 contribuidores  
- > 1 issue aberta  
- > 50 issues fechadas  
- > 100 estrelas  
- > 10 forks  
- > 50 commits  
- Último commit nos últimos ≤ 180 dias  

Foram excluídos: repositórios privados, deletados, arquivados ou com dados incompletos.

---

## 🛠️ Pipeline da Coleta

O processo foi estruturado em módulos Python independentes:

1. **Busca inicial por faixa de estrelas**
2. **Extração de metadados**
3. **Coleta de contribuidores**
4. **Coleta de issues fechadas**
5. **Contagem de commits**
6. **Aplicação dos critérios de atividade**
7. **Consolidação da base final**
8. **Geração de relatórios textuais**

Cada módulo gera logs, checkpoints e salvamentos incrementais para garantir reprodutibilidade.

---

## 📏 Métricas Coletadas

### 🔹 Métricas Primárias (API)
- Nome, dono, descrição  
- Datas de criação, última atualização, último commit  
- Contagem de estrelas, forks e issues abertas  
- Linguagem principal  

### 🔹 Métricas Calculadas
- contributors_count  
- closed_issues_count  
- commits_count  
- days_since_last_commit  
- age_days  

---

## 📊 Procedimentos de Análise

A análise estatística empregou:

- Estatísticas descritivas  
- Correlações (Spearman)  
- Identificação de outliers  
- Análises comparativas entre estratos  
- Normalização das métricas  

Ferramentas utilizadas: `pandas`, `numpy`, `scipy`.

---

# 📈 Resultados Principais

## 🔹 Q1 — Popularidade vs. Número de Contribuidores

- Existe **correlação positiva, porém fraca**, entre estrelas e número de contribuidores.
- Algumas inconsistências aparecem: projetos com ~40k estrelas podem ter tanto <200 quanto >1000 contribuidores.
- Estrelas não são um bom preditor do tamanho da comunidade.

**Conclusão:** Popularidade mede visibilidade, não engajamento real.

---

## 🔹 Q2 — Participação Ativa da Comunidade

A análise de pull requests revelou:

- Alta **variabilidade** entre os repositórios.
- A mediana de PRs aceitos no último ano é de ~357.
- PRs rejeitados têm valores altos em alguns repositórios, indicando rigor ou desalinhamento.
- PRs abertos permanecem baixos, sinalizando triagem eficiente.

**Conclusão:**  
Os projetos analisados possuem participação ativa consistente, mas heterogênea — influenciada por documentação, governança e maturidade do projeto.

---

## 🔹 Q3 — Interação via Issues

- **75%** dos repositórios respondem a issues **em até 3 dias**.  
- Um número relevante responde em menos de 24 horas.  
- A mediana de issues fechadas é **11x maior** que a de issues abertas.
- Em projetos extremos, o alto número de issues abertas pode indicar desafios de escalabilidade.

**Conclusão:**  
Responsividade é alta entre os repositórios ativos, refletindo comunidades bem estruturadas e processos eficazes de resolução.

---

# 🧩 Conclusões Gerais

- Popularidade não significa engajamento.  
- Contribuição ativa depende de processos internos e clareza nas diretrizes.  
- Responsividade é um indicador-chave de saúde comunitária.  
- Comunidades sustentáveis utilizam práticas maduras de governança, triagem e integração de contribuições.

---

# ⚠️ Limitações

- Dependência da precisão da API do GitHub  
- Amostragem enviesada para projetos mais visíveis  
- Dificuldade em identificar contribuidores externos em repositórios muito grandes  
- Análise pontual (não longitudinal)

---

# 🔄 Reprodutibilidade

Este repositório inclui:

- Scripts em Python para coleta completa  
- Arquivos JSON consolidados  
- Logs e checkpoints  
- Documentação para reprodução do estudo  

---

# 📚 Referências

- Borges et al. (2016) – Popularidade no GitHub  
- Tov et al. (2018) – Significado das estrelas  
- Arachchi & Perera (2018) – Critérios de repositórios ativos  
- Padhye et al. (2014) – Contribuições externas  
- Yu et al. (2024) – Tempo de resposta e PRs  
- Rahman & Roy (2014) – Templates de issues

---

