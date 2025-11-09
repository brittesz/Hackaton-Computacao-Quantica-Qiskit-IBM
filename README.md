#  Hackathon Qiskit IBM – Fall Fest 2025  
### Grupo 3 – Quantum para Todos  

**Integrantes:**  
- Denise Sagbo — denise.sagbo@ufabc.edu.br  
- Luiza Brittes Barros — luiza.brittes@aluno.ufabc.edu.br  
- Victor Emanuel Guimarães — victoremanuelguima@gmail.com  
- Nícolas Amaral Ferreira Pinho — nicolas.pinho@usp.br  

---

## Projeto: Encontrar números gerados aleatoriamente utilizando o Algoritmo de Grover  

### Objetivo  
Nosso projeto tem como objetivo utilizar o princípio do Algorítmo de Grover para encontrar, de forma mais rápida e precisa que um algorítmo clássico, um número gerado aleatoriamente utlizando o conceito de superposição de estados quânticos de um qubit.

---

## Conceitos Quânticos Utilizados  

1. **Interferência Quântica:** os qubits operam a partir do princípio da dualidade da onda-partícula. Graças a isso, utilizaremos a propriedade de onda dos qubits para fazer uma interferência de ondas.
2. **Algoritmo de Grover:** é um algoritmo de busca quântica que reduz o número de tentativas necessárias para encontrar um item específico em um conjunto não ordenado.
---

##  Metodologia  

O projeto foi dividido em duas abordagens:

- **Busca Quântica (Grover):** usa o simulador `AerSimulator` do Qiskit para preparar o circuito, aplicar o oráculo e o difusor, e medir o resultado.
- **Busca Clássica:** o algoritmo percorre todas as combinações possíveis até encontrar a senha correta.  

Em ambos os casos, comparamos o número de tentativas e a probabilidade de sucesso.

---

## Resultados  

- A busca clássica exige em média metade das combinações possíveis (\(N/2\)).  
- O Algoritmo de Grover encontra o resultado com apenas cerca de \(\sqrt{N}\) iterações.  
- Nos testes com 10 qubits (\(N=1024\)), o Grover obteve a senha correta com probabilidade superior a 90% com uma quantidade significativamente menor de de iterações quânticas quando comparada com as tentativas clássicas.

Visualmente, os resultados podem ser observados no **histograma de medições** gerado pelo Qiskit.

---

## Conclusões e Limitações  

O projeto demonstra a eficiência dos algoritmos quânticos para tarefas de busca, utiliazndo-se dos conceitos de **superposição**, **interferência**, uso da propriedade onda-partícula e **amplificação de amplitude**.

**Limitações:**  
- O tempo de simulação cresce exponencialmente de acordo o número de qubits e a simulação do algoritmo quântico demora mais em computador clássico do que a pesquisa clássica.  
- Em hardware clássico, o ruído pode reduzir a precisão.
- O tamanho da simulação é limitado fisicamente à capacidade de memória do sistema

**Melhorias futuras:**  
- Implementar um sistema de senha quântica que aceite qualquer tipo de caractere, incluindo números, letras e símbolos especiais, ampliando o espaço de busca e tornando o experimento mais próximo de um cenário real de segurança digital.  
- Buscar o menor números de iterações e mantendo uma alta porcentagem de acerto

---

## Execução  

Para executar o notebook:

1. Instale as dependências:  
   ```bash
   pip install qiskit qiskit-aer matplotlib
