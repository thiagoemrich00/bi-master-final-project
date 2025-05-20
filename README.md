<!-- antes de enviar a versão final, solicitamos que todos os comentários, colocados para orientação ao aluno, sejam removidos do arquivo -->
# Casos de otimização de Performance de Compressores Centrífugos

#### Aluno: [Thiago César Emrich](https://github.com/thiagoemrich00)
#### Orientadora: [Prof. Ana Carolina Abreu](https://github.com/acarolina1612?tab=overview&from=2024-12-01&to=2024-12-31).
<!-- Co-orientador(/a/es/as): [Nome Sobrenome](https://github.com/link_do_github). <!-- caso não aplicável, remover esta linha -->

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

<!-- para os links a seguir, caso os arquivos estejam no mesmo repositório que este README, não há necessidade de incluir o link completo: basta incluir o nome do arquivo, com extensão, que o GitHub completa o link corretamente -->
- [Link para o código](https://github.com/link_do_repositorio). <!-- caso não aplicável, remover esta linha -->

- [Link para a monografia](https://link_da_monografia.com). <!-- caso não aplicável, remover esta linha -->


---

### Resumo

<!-- trocar o texto abaixo pelo resumo do trabalho, em português -->

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pulvinar nisl vestibulum tortor fringilla, eget imperdiet neque condimentum. Proin vitae augue in nulla vehicula porttitor sit amet quis sapien. Nam rutrum mollis ligula, et semper justo maximus accumsan. Integer scelerisque egestas arcu, ac laoreet odio aliquet at. Sed sed bibendum dolor. Vestibulum commodo sodales erat, ut placerat nulla vulputate eu. In hac habitasse platea dictumst. Cras interdum bibendum sapien a vehicula.

### Abstract <!-- Opcional! Caso não aplicável, remover esta seção -->

<!-- trocar o texto abaixo pelo resumo do trabalho, em inglês -->

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pulvinar nisl vestibulum tortor fringilla, eget imperdiet neque condimentum. Proin vitae augue in nulla vehicula porttitor sit amet quis sapien. Nam rutrum mollis ligula, et semper justo maximus accumsan. Integer scelerisque egestas arcu, ac laoreet odio aliquet at. Sed sed bibendum dolor. Vestibulum commodo sodales erat, ut placerat nulla vulputate eu. In hac habitasse platea dictumst. Cras interdum bibendum sapien a vehicula.

Proin feugiat nulla sem. Phasellus consequat tellus a ex aliquet, quis convallis turpis blandit. Quisque auctor condimentum justo vitae pulvinar. Donec in dictum purus. Vivamus vitae aliquam ligula, at suscipit ipsum. Quisque in dolor auctor tortor facilisis maximus. Donec dapibus leo sed tincidunt aliquam.

Donec molestie, ante quis tempus consequat, mauris ante fringilla elit, euismod hendrerit leo erat et felis. Mauris faucibus odio est, non sagittis urna maximus ut. Suspendisse blandit ligula pellentesque tincidunt malesuada. Sed at ornare ligula, et aliquam dui. Cras a lectus id turpis accumsan pellentesque ut eget metus. Pellentesque rhoncus pellentesque est et viverra. Pellentesque non risus velit. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.

### 1. Introdução

Este estudo propõe uma abordagem de otimização para a determinação da pressão intermediária entre as seções de compressão em compressores de gás úmido, empregados em unidades de processamento de petróleo.

Em sistemas que utilizam controle de capacidade por válvula de estrangulamento, a variação da pressão de sucção resulta em novas distribuições de pressão ao longo das diferentes seções do compressor. Nessa configuração, a definição adequada da pressão entre seções torna-se essencial não apenas para assegurar a integridade operacional do equipamento, mas também para o correto estabelecimento dos limites de alarme e disparo (trip) dos vasos associados ao estágio intermediário.

A otimização desse parâmetro contribui diretamente para a confiabilidade, segurança e eficiência do sistema de compressão.

### 2. Modelagem

Para a modelagem do problema foi utilizado a biblioteca do python [CCP](https://ccp-centrifugal-compressor-performance.readthedocs.io/en/latest/index.html)  que realiza cálculos de performance para compressores centrífugos. O código utiliza CoolProp / REFPROP para realizar os cálculos de propriedades dos gases e misturas.

Para a otimização utilizamos a função [differential evolution](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.differential_evolution.html) do SciPy.

Esta função encontra o mínimo global de uma função multivariada utilizando o método de evolução diferencial. O algoritmo é estocástico, ou seja, utiliza abordagens probabilísticas em vez de métodos baseados em gradientes. Isso o torna adequado para explorar grandes espaços de soluções, mesmo em problemas complexos e com múltiplos mínimos locais. Por outro lado, tende a exigir um número maior de avaliações da função quando comparado a métodos tradicionais baseados em gradiente.

### 3. Resultados

Lorem ipsum dolor sit ame

![image](https://github.com/user-attachments/assets/e0c53baa-6dea-483f-a4f8-7dfd012b86ac)


### 4. Conclusões

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin pulvinar nisl vestibulum tortor fringilla, eget imperdiet neque condimentum. Proin vitae augue in nulla vehicula porttitor sit amet quis sapien. Nam rutrum mollis ligula, et semper justo maximus accumsan. Integer scelerisque egestas arcu, ac laoreet odio aliquet at. Sed sed bibendum dolor. Vestibulum commodo sodales erat, ut placerat nulla vulputate eu. In hac habitasse platea dictumst. Cras interdum bibendum sapien a vehicula.

Proin feugiat nulla sem. Phasellus consequat tellus a ex aliquet, quis convallis turpis blandit. Quisque auctor condimentum justo vitae pulvinar. Donec in dictum purus. Vivamus vitae aliquam ligula, at suscipit ipsum. Quisque in dolor auctor tortor facilisis maximus. Donec dapibus leo sed tincidunt aliquam.

---

Matrícula: 222.100.476

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
