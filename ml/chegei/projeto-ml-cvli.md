
# **Descrição do projeto de machine learning na INT/SSPAL**
> Antes de escrever qualquer código, precisamos entender o problema que queremos resolver e fazer uma descrição eficiente do projeto, visando a comunicação simples e rápida do objetivo do projeto para técnicos, gestores e colaboradores.

### **1 - Descrição do problema ou tarefa:**
> Predições de possíveis locais de Crimes baseados nos dados de CVLIs do NEAC

### **2 - Descrição da solução de IA:**
> Treinamento supervisionado de modelo de regressão para predição com base nos dados das dimensões dos locais e tipo criminal que está relacionado com as CVLIs, com base em 7 atributos (características).
> São alguns locais possíveis: Via Pública, Imediações de Casa, Próximo de Casa, Porta de Casa, Dentro de Casa, Presídio, Residência, Vegetação, Bar, Estabelecimento Comercial, entre outros …

### **3 - Fonte de dados: (mudanças aqui)**

> Dados do NEAC/SSPAL (Núcleo de Estatística e Análise Criminais)

> - NEAC_CVLI_2023.csv - base de validação https://drive.google.com/file/d/1L7fHdQ5NSE8l22NV8xy-w4hHV9xMRktg/view?usp=sharing
>- NEAC_CVLI_2022.csv - base de testes https://drive.google.com/file/d/1l1WlIaNth_9il2OGCzWcCc1KrRyjM19r/view?usp=sharing
> - NEAC_CVLI.csv - Dados - base de treinamento (2012 ate 2022) https://drive.google.com/file/d/1pMOhYHnam6pCs8tt4yLMQDZGX_anK4LV/view?usp=sharing

### **4 - Variáveis independentes (preditoras ou "features"):**

> - Tipo ciminal - SUBJETIVIDADE_COMPLEMANTAR (str)
> - Instrumento - INSTRUMENTO (str)
> - Data do Fato - DATA_HORA_FATO (DateTime)
> - Turno do Fato - TURNO (str)
> - Cor ou Raça da Vítima - COR_RACA_VITIMA (str)
> - Sexo da Vítima - SEXO_VITIMA (str)
> - Dia da Semana - DIA_SEMANA (num)

### **5 - Variável dependente (resposta ou "target"):**

> Local do Fato - LOCAL_FATO (str)

### **6- Base de dados/estrutura de dados:**

|#|Description| Field|Non-Null Count| Data type|X ou y|Drop
|-|-----------|:-----|:---------|:--------|:-------|:---|
| 0 ||Unnamed: 0|63 non-null|int64|-|*| 
| 1 ||created_on|63 non-null|object|-|*|
| 2 ||operation|63 non-null|object|-|*|
| 3 ||property_type|63 non-null|object|-|*|
| 4 ||place_name|63 non-null|object|-|*| 
| 5 ||place_with_parent_names|63 non-null|object|-|*| 
| 6 ||geonames_id|0 non-null|float64|-|*|
| 7 ||lat_lon|41 non-null|object|-|*|
| 8 ||lat|41 non-null|float64|-|*|
| 9 ||lon|41 non-null|float64|-|*|
| 10 ||price|63 non-null|float64|y|*|
| 11 ||currency|63 non-null|object|-|*|
| 12 ||price_aprox_local_currency|63 non-null|float64|X|*|
| 13 ||price_aprox_usd|63 non-null|float64|X||
| 14 ||surface_total_in_m2|16 non-null|float64|X|*|
| 15 ||surface_covered_in_m2|57 non-null|float64|X|*|
| 16 ||price_usd_per_m2|56 non-null|float64|X||
| 17 ||price_per_m2|56 non-null|float64|X||
| 18 ||floor|7 non-null|float64|X||
| 19 ||rooms|22 non-null|float64|X||
| 20 ||expenses|11 non-null|float64|-|*||
| 21 ||properati_url|63 non-null|object|-|*|
| 22 ||description|63 non-null|object|-|*|
| 24 ||image_thumbnail|63 non-null|object|-|*|
| 25 ||location|41 non-null|object|-|*|

# Dados de CVLI2022
[Dados de CVLI2022 - link](https://drive.google.com/file/d/1UPDQ6V6ZQtwexk5f-mpROq_p1UvOUf2N/view?usp=sharing)
### ID: 1UPDQ6V6ZQtwexk5f-mpROq_p1UvOUf2N