## Descrição do problema.
O objetivo deste projeto é desenvolver um modelo de ciência de dados capaz de prever qual a intensidade de chuva de um dia, utilizando dados meteorológicos da cidade de Aracaju como base. 
Para essa classificação, considera-se a quantidade de precipitação acumulada em milímetros por hora ou por dia, categorizada da seguinte forma:

Chuva Fraca: abaixo de 25 mm/h.

Chuva Moderada: entre 25 mm/h e 50 mm/h.

Chuva Forte: entre 50 mm/h e 60 mm/h, ou até 100 mm/dia.

Chuva Extremamente Forte: acima de 60 mm/h ou 100 mm/dia, podendo ocasionar sérios impactos, como alagamentos, transbordamentos de rios e deslizamentos de terra.

A correta definição dos níveis de risco é essencial para antecipar e comunicar potenciais perigos à população. Essas informações, quando associadas às orientações das autoridades locais de defesa civil, 
tornam-se ferramentas fundamentais para apoiar a tomada de decisões preventivas e a mitigação de danos.

A cidade de Aracaju foi escolhida como objeto de estudo devido à recorrência de alagamentos durante o período chuvoso, 
o que a torna um cenário relevante para a análise de risco climático. O dataset utilizado neste projeto foi obtido a partir dos dados abertos do Instituto Nacional de Meteorologia (INMET), 
abrangendo registros dos últimos cinco anos, o que garante uma base histórica consistente para a construção e avaliação do modelo preditivo.

site: https://portal.inmet.gov.br/dadoshistoricos

## Roteiro 

O desenvolvimento deste projeto iniciou-se com a obtenção dos dados disponibilizados pelo INMET, abrangendo registros dos últimos 10 anos. Cada arquivo foi tratado e consolidado em um único dataset. Em seguida, realizou-se a análise exploratória, na qual foi identificado um grande volume de dados faltantes e valores negativos. Esses registros foram removidos por não apresentarem confiabilidade.

Após o tratamento inicial, os dados de precipitação total horária (mm) foram classificados de acordo com a intensidade da chuva e seu potencial de risco para a população. Contudo, essa etapa evidenciou um desbalanceamento entre as classes, o que tornou necessário aplicar técnicas de balanceamento para aproximar a quantidade de exemplos em cada categoria.

Na fase de modelagem, foram testados quatro algoritmos de classificação. O Dummy Classifier foi adotado como baseline de referência para avaliação da qualidade dos demais modelos, utilizando a precisão como métrica inicial de comparação. Os outros algoritmos avaliados foram Random Forest, SVM e Regressão Logística.

Os resultados mostraram que o Random Forest foi o modelo mais adequado para o problema, superando significativamente os demais. Para uma avaliação mais robusta, a métrica F1-Score foi utilizada, pois considera tanto a precisão quanto a revocação (recall), fornecendo uma visão mais completa do desempenho em dados desbalanceados, especialmente nas classes minoritárias.

Por fim, devido ao bom desempenho do Random Forest, foram realizados testes de otimização de parâmetros, buscando identificar a configuração mínima necessária para garantir um modelo mais eficiente, enxuto e confiável.

## Conclusão 
Em síntese, o projeto demonstrou que é possível utilizar dados meteorológicos históricos para construir um modelo preditivo confiável da intensidade da chuva na cidade de Aracaju. A aplicação do Random Forest, aliado ao balanceamento de classes e à otimização de parâmetros, mostrou-se a estratégia mais eficaz para lidar com o problema de desbalanceamento e garantir previsões mais robustas. Esse resultado reforça a importância da ciência de dados como ferramenta de apoio à gestão de riscos climáticos, oferecendo subsídios para ações preventivas da defesa civil e contribuindo para a redução dos impactos sociais e ambientais causados por eventos extremos de precipitação.



