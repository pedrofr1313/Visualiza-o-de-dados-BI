# Relatório de Análise - Lab03

## Contexto

Este repositório contém o relatório de BI gerado a partir do *dataset do Lab03*, que analisa Pull Requests (PRs) de repositórios.  
O *dataset final* foi gerado no Lab03 e contém informações detalhadas sobre PRs, incluindo:

- repo_name: nome do repositório  
- pr_number: número do PR  
- state: estado do PR (open, closed, merged)  
- created_at, closed_at, merged_at: datas de criação, fechamento e merge  
- additions, deletions, changed_files: métricas de alterações  
- body_length: tamanho da descrição do PR  
- comments, review_comments, participants_count: interações no PR  

O relatório visa explorar e visualizar *tendências e métricas de PRs*, como:

- Percentual de PRs fechados (state = "closed")  
- Relação entre tamanho do PR e chance de merge  
- Tempo de revisão e interações  

---

## Relatório Power BI

O arquivo do relatório está localizado em:

/report/Relatório BI.pbix

Ao abrir no Power BI Desktop ou no Power BI Online, você encontrará todos os visuais, filtros e cards configurados para análise.  

*Seleção do Dataset:*  
O relatório utiliza o dataset gerado pelo *Lab03*, chamado final_dataset.  
Todos os gráficos, cards e visualizações do relatório estão conectados a este dataset, garantindo consistência com os dados processados no laboratório.

---

## Dashboard Online

Você também pode visualizar o dashboard diretamente no Power BI Online através deste link:

[Visualizar Dashboard](https://app.powerbi.com/groups/me/reports/d75060cc-a563-4ed7-8611-fbb9ed1059f3/dffc4584266dc2967bf8?experience=power-bi&clientSideAuth=0)

---

## Observações

- Para abrir o arquivo .pbix no Power BI Desktop, certifique-se de ter a versão mais recente do Power BI instalada.  
- Todas as medidas e visuais foram criados considerando a *estrutura do dataset do Lab03*.  
- Qualquer atualização no dataset requer reabertura e atualização do relatório para refletir novos dados.