# Heredity - Análise de Hereditariedade com Inteligência Artificial  

Este projeto implementa um modelo probabilístico para analisar a hereditariedade de genes e calcular a probabilidade de um indivíduo herdar traços genéticos de seus pais. O código foi desenvolvido como parte do curso **CS50 - Introduction to Artificial Intelligence with Python**, oferecido por **Harvard University**.  
## Tecnologias Utilizadas  
- **Linguagem**: Python 3  
- **Bibliotecas**:  
  - `csv` (processamento de dados familiares)  
  - `itertools` (geração de combinações possíveis)  
- **Conceitos Chave**:  
  - Modelagem Bayesiana de probabilidades  
  - Cálculo de Probabilidade Conjunta  
  - Herança Genética com Mutação  
  - Normalização de Distribuições Probabilísticas  
  
## Estrutura do Projeto  

A pasta contém os seguintes arquivos:  

- **`heredity.py`**: Implementação do modelo probabilístico para análise genética.  
- **`data/`**: Contém arquivos CSV com informações sobre famílias e seus genes, fornecido pelo CS50.  
  - `family0.csv`  
  - `family1.csv`  
  - `family2.csv` 

## Features  
- **Modelo Genético Probabilístico**:  
  - Calcula a probabilidade de herança de genes considerando:  
    - Transmissão parental (pai e mãe)  
    - Taxa de mutação (1%)  
    - Expressão de traços baseada em dominância genética  
- **Sistema Flexível de Entrada**:  
  - Processa arquivos CSV com estrutura familiar complexa  
  - Aceita dados parciais (traços conhecidos/desconhecidos)  
- **Cálculos Avançados**:  
  - Gera todas combinações possíveis de genes/traços (powerset)  
  - Computa distribuições de probabilidade conjunta  
  - Normaliza resultados para soma total de 1  
- **Saída Detalhada**:  
  - Exibe probabilidades formatadas para:  
    - Número de cópias do gene (0/1/2)  
    - Expressão do traço (True/False)  
- **Otimizações**:  
  - Filtragem precoce de combinações inviáveis  
  - Atualização eficiente de distribuições acumuladas  
  
## Como funciona o modelo de hereditariedade  

O modelo utilizado neste projeto se baseia em redes bayesianas para calcular a probabilidade de um indivíduo herdar genes de seus pais. O processo funciona da seguinte maneira:  

1. Cada pessoa pode ter 0, 1 ou 2 cópias de um determinado gene.  
2. A herança genética segue probabilidades definidas:
   - Se os pais de um indivíduo são conhecidos, a probabilidade de herança do gene é calculada com base nos genes dos pais.  
   - Se os pais não são conhecidos, a probabilidade é baseada na frequência natural do gene na população.  
3. Além da transmissão genética, há uma probabilidade de mutação, ou seja, um gene pode surgir espontaneamente ou ser perdido na herança.  
4. O modelo calcula a probabilidade de cada pessoa no conjunto de dados possuir o gene e expressar determinado traço genético.  

## Minha Contribuição  

A implementação do modelo probabilístico foi desenvolvida no arquivo `heredity.py`, permitindo a análise da herança genética a partir de diferentes bases de dados contidas na pasta `data/`.  

## Como Rodar o Projeto  

1. Clone o repositório:  
   ```bash
   git clone https://github.com/Alvaro-Sena/heredity.git  
   ```
2. Navegue até a pasta do projeto:  
   ```bash  
   cd heredity   
   ```  
3. Execute a análise genética de uma determinada família, utilize o seguinte comando no terminal:  

  ```bash
  python3 heredity.py data/family0.csv
  ```  
No comando acima, data/family0.csv representa um conjunto de dados sobre uma família. Você é livre para substituir family0.csv por family1.csv ou family2.csv, para analisar diferentes amostras.

Certifique-se de que possui **Python 3** instalado no seu ambiente.


## Contato
Caso tenha dúvidas ou sugestões, entre em contato através do meu [LinkedIn](www.linkedin.com/in/alvaro-sena), [GitHub](https://github.com/Alvaro-Sena)ou [WhatsApp](https://wa.me/447356040385).
