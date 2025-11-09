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
Demonstrar, por meio do **Algoritmo de Grover**, como a computação quântica pode acelerar a busca de um número (ou senha) aleatório em comparação com uma busca clássica.

---

## Conceitos Quânticos Utilizados  

O **Algoritmo de Grover** é um algoritmo de busca quântica que reduz o número de tentativas necessárias para encontrar um item específico em um conjunto não ordenado.

Etapas principais:
1. **Superposição:** todos os estados possíveis são preparados com igual probabilidade.  
2. **Oráculo:** marca o estado correto invertendo sua fase.  
3. **Difusor:** amplifica a probabilidade do estado marcado.  
4. **Medição:** colapsa o sistema para o resultado mais provável.

Enquanto a busca clássica tem complexidade **O(N)**, a busca quântica tem complexidade **O(√N)**.

---

##  Metodologia  

O projeto foi dividido em duas abordagens:

- **Busca Clássica:** o algoritmo percorre todas as combinações possíveis até encontrar a senha correta.  
- **Busca Quântica (Grover):** usa o simulador `AerSimulator` do Qiskit para preparar o circuito, aplicar o oráculo e o difusor, e medir o resultado.

Em ambos os casos, comparamos o número de tentativas e a probabilidade de sucesso.

---

## Resultados  

- A busca clássica exige em média metade das combinações possíveis (\(N/2\)).  
- O Algoritmo de Grover encontra o resultado com apenas cerca de \(\sqrt{N}\) iterações.  
- Nos testes com 10 qubits (\(N=1024\)), o Grover obteve a senha correta com probabilidade superior a 90%.

Visualmente, os resultados podem ser observados no **histograma de medições** gerado pelo Qiskit.

---

## Conclusões e Limitações  

O projeto demonstra a eficiência dos algoritmos quânticos para tarefas de busca, ilustrando conceitos como **superposição**, **interferência** e **amplificação de amplitude**.

**Limitações:**  
- O tempo de simulação cresce com o número de qubits.  
- Em hardware real, o ruído pode reduzir a precisão.  

**Melhorias futuras:**  
- Implementar um sistema de senha quântica que aceite qualquer tipo de caractere, incluindo números, letras e símbolos especiais, ampliando o espaço de busca e tornando o experimento mais próximo de um cenário real de segurança digital.  
- Ajustar o número de iterações conforme o tamanho do problema.  

---

## Execução  

Para executar o notebook:

1. Instale as dependências:  
   ```bash
   pip install qiskit qiskit-aer matplotlib
