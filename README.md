<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Otimização de Performance de Compressores Centrífugos

#### Aluno: [Thiago César Emrich](https://github.com/thiagoemrich00)
#### Orientadora: [Prof. Ana Carolina Abreu](https://github.com/acarolina1612?tab=overview&from=2024-12-01&to=2024-12-31)
<!-- Co-orientador(/a/es/as): [Nome Sobrenome](https://github.com/link_do_github). <!-- caso não aplicável, remover esta linha -->

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código de variação da Pressão de Sucção na 1ª Seção](https://github.com/thiagoemrich00/bi-master-final-project/blob/main/otimizacao_pressao_intersecao.ipynb). <!-- caso não aplicável, remover esta linha -->
- [Link para o código de variação da Temperatura do Interseção (Sucção na 2ª Seção)](https://github.com/thiagoemrich00/bi-master-final-project/blob/main/otimizacao_pressao_intersecao_Ts_2_45_C.ipynb).

---

### Resumo

Em sistemas que utilizam controle de capacidade por válvula de estrangulamento, a variação da pressão de sucção resulta em novas distribuições de pressão ao longo das diferentes seções do compressor. Nessa configuração, a definição adequada da pressão entre seções torna-se essencial não apenas para assegurar a integridade operacional do equipamento, mas também para o correto estabelecimento dos limites de alarme e disparo (trip) dos vasos associados ao estágio intermediário.

Embora os fabricantes sejam os responsáveis pela definição dos pontos operacionais dos compressores, é comum que, ao longo da operação dessas máquinas, ocorram variações nas condições de processo. Nesse contexto, a otimização dos parâmetros operacionais torna-se fundamental para garantir a confiabilidade, a segurança e a eficiência do sistema de compressão.

O presente estudo propõe uma abordagem de otimização voltada à determinação da pressão intermediária entre as seções de compressão em compressores de gás úmido, utilizados em unidades de processamento de petróleo. A metodologia adotada permite a flexibilização de variáveis operacionais, como rotação, temperatura na seção intermediária e composição do gás, entre outras, visando a adaptação dinâmica do sistema às diferentes condições de operação.

![image](https://github.com/user-attachments/assets/3efad77c-f34a-4bfb-a0fd-89f99d91a229)


### 1. Introdução

Os cálculos de desempenho de compressores centrífugos estão intrinsecamente relacionados às suas curvas características de performance. A Figura a seguir apresenta as curvas de desempenho correspondentes ao modelo analisado:

![image](https://github.com/user-attachments/assets/4bc51195-e6b7-4c40-bae4-b963c0e39351)

Essas curvas representam a relação entre o estado termodinâmico do gás na sucção (caracterizado por variáveis como pressão, temperatura, entalpia, entropia e massa específica) e seu estado termodinâmico após a compressão, ou seja, na descarga do compressor.

Em compressores de gás úmido, é comum a presença de duas seções de compressão integradas em uma mesma carcaça. Essas seções são interdependentes, uma vez que as condições de sucção da segunda seção são diretamente influenciadas pelas condições de descarga da primeira. Essa interdependência deve ser cuidadosamente considerada nas análises de desempenho, de modo a garantir a operação segura e eficiente do equipamento.

### 2. Modelagem

Para a modelagem do problema foi utilizado a biblioteca do python [CCP](https://ccp-centrifugal-compressor-performance.readthedocs.io/en/latest/index.html)  que realiza cálculos de performance para compressores centrífugos. O código utiliza CoolProp / REFPROP para realizar os cálculos de propriedades dos gases e misturas.

Para a otimização utilizamos a função [differential evolution](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.differential_evolution.html) do SciPy.

Esta função encontra o mínimo global de uma função multivariada utilizando o método de evolução diferencial. O algoritmo é estocástico, ou seja, utiliza abordagens probabilísticas em vez de métodos baseados em gradientes. Isso o torna adequado para explorar grandes espaços de soluções, mesmo em problemas complexos e com múltiplos mínimos locais. Por outro lado, tende a exigir um número maior de avaliações da função quando comparado a métodos tradicionais baseados em gradiente.

A otimização realizada possui as seguintes restrições: Presssão de Sucção da 1ª Seção, Pressão de descarga na 2ª Seção, Temperatura de sucção na 2ª seção e perda de carga no trocador de calor inter-seção, porém podemos ter outros, como rotação, temperatura ou delta de temperatura no trocador de calor, torque, potência por seção. As possibilidades de otimização são bem abrangentes.

A função objetivo construída para o nosso caso em questão foi a minimização da subtração pressão de descarga na 2ª seção imposta pela pressão de descarga na 2ª seção calculada através do CCP.

### 3. Resultados

A tabela a seguir mostra os resultados das otimizações realizadas, onde foram variadas as pressões de entrada da primeira seção:

![image](https://github.com/user-attachments/assets/e0c53baa-6dea-483f-a4f8-7dfd012b86ac)


### 4. Conclusões

Do ponto de vista de processamento do gás, à medida que se reduz o estrangulamento na válvula de controle de vazão — ou seja, quando a pressão de sucção da primeira seção é diminuída — observa-se uma redução nas vazões mássicas processadas por ambas as seções do compressor, bem como uma diminuição na pressão na região inter-seções.

Já do ponto de vista do processo de otimização, este trabalho apresenta significativa relevância nas etapas de projeto conceitual e básico, ao proporcionar estimativas mais precisas e aproximações realistas das condições operacionais de compressores centrífugos de dupla seção.

---

Matrícula: 222.100.476

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
