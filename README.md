# Ordenador Universal
![Feito em C++](https://img.shields.io/badge/C%2B%2B-Feito%20em-blue)

![Badge Concluído](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)


**Trabalho Prático 1 – Estrutura de Dados**  
Departamento de Ciência da Computação – Universidade Federal de Minas Gerais (UFMG)  
Autor: Matheus Soares dos Santos de Freitas  
E-mail: masanfreitas@outlook.com

## 🧩 Descrição

Este projeto implementa o **Ordenador Universal**, um Tipo Abstrato de Dados (TAD) que seleciona dinamicamente o algoritmo de ordenação mais eficiente com base nas características do vetor de entrada.

A escolha entre **Insertion Sort** e **Quick Sort** é feita automaticamente, considerando:

- O **grau de ordenação** do vetor (número de quebras)
- O **tamanho do vetor**
- O uso de **mediana de três** para otimizar o Quick Sort

O TAD visa otimizar o desempenho da ordenação, sendo especialmente eficaz em vetores parcialmente ordenados.

## 📁 Estrutura do Projeto

```
TP1/
├── include/           # Arquivos de cabeçalho e templates (.hpp e .tpp)
│   ├── estatisticas.hpp
│   ├── funcoes.hpp
│   ├── funcoes.tpp
│   ├── ordenador.hpp
│   └── ordenador.tpp
├── src/               # Arquivos-fonte (.cpp)
│   ├── estatisticas.cpp
│   └── main.cpp
├── bin/               # Executável final (tp1.out)
├── .obj/              # Arquivos objeto (.o)
├── .vscode/           # Configurações do Visual Studio Code
├── Makefile           # Script de compilação
└── README.md          # Este arquivo
```

## ⚙️ Compilação e Execução

1. Navegue até o diretório do projeto:
   ```bash
   cd ~/TP1
   ```

2. Compile todos os arquivos com `make`:
   ```bash
   make all
   ```

3. Execute o programa:
   ```bash
   ./bin/tp1.out testes/arquivo.txt
   ```

> **Nota:** O projeto foi desenvolvido em C++ usando o compilador G++ via WSL (Windows Subsystem for Linux).

## 🧠 Funcionalidades

- Determinação empírica dos limiares ótimos de:
  - Tamanho da partição (`determinaLimiarParticao`)
  - Número de quebras (`determinaLimiarQuebra`)
- Ordenação adaptativa com `OrdenadorUniversal<T>`
- Estatísticas detalhadas de chamadas, comparações e movimentações
- Análise experimental com geração de dados em `.csv`

## 📈 Análise Experimental

- Correlações estudadas:
  - **Payload** vs Tempo de execução
  - **Tamanho das chaves** vs Tempo de execução
  - **Número de quebras** vs Tempo de execução
- Comparação de desempenho entre:
  - **Ordenador Universal**
  - **QuickSort**
  - **InsertionSort**

> Resultados indicam que o TAD supera os algoritmos puros em vetores quase ordenados e se mantém competitivo com QuickSort em vetores desordenados.

## 📊 Complexidade

- **InsertionSort**:  
  - Tempo: O(n²) | Espaço: O(1)
- **QuickSort** (mediana de três, com fallback):  
  - Tempo: O(n log n) médio, O(n²) pior caso | Espaço: O(log n)
- **determinadores de limiares**:  
  - Tempo: O(k·n log n) | Espaço: O(n)

## 🧪 Ambiente de Testes

- Processador: Intel Core (6 núcleos, 6 threads, 2.90GHz)
- RAM: 9,2 GB em uso, 2,7 GB livres
- SO: Windows via WSL

## 📚 Referências

- Wikipedia: [Insertion Sort](https://pt.wikipedia.org/wiki/Insertion_sort) | [QuickSort](https://pt.wikipedia.org/wiki/Quicksort)  
- Slides da disciplina DCC205 - UFMG  
- Especificação oficial do TP1

---

Desenvolvido para a disciplina de **Estruturas de Dados - DCC/UFMG**.
