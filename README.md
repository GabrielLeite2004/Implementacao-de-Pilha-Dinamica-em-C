# Implementação de Pilha Dinâmica em C

## Descrição
Este projeto em C implementa uma estrutura de dados do tipo pilha utilizando alocação dinâmica. A pilha é composta por nodos que armazenam elementos, permitindo operações básicas como empilhar, desempilhar e obter o topo da pilha.

## Funcionalidades
- **Criação de Pilha**: Inicializa uma pilha vazia e pronta para uso.
- **Verificação de Pilha Vazia**: Verifica se a pilha está vazia.
- **Empilhar Elemento**: Adiciona um novo elemento no topo da pilha.
- **Desempilhar Elemento**: Remove o elemento do topo da pilha e retorna o valor.
- **Obter Topo da Pilha**: Acessa o elemento que está no topo da pilha sem removê-lo.

## Como Usar
1. Compile o código utilizando um compilador C. Exemplo:
   ```bash
   gcc -o pilha_dinamica pilha_dinamica.c
   ```
2. Execute o programa e utilize as funções para manipular a pilha conforme necessário:
   - Crie a pilha com `criarPilha(&p)`.
   - Empilhe elementos com `empilharElemento(&p, elemento)`.
   - Desempilhe elementos com `desempilharElemento(&p, &elemento)`.
   - Verifique o topo da pilha com `obterTopo(p, &elemento)`.

## Estrutura de Dados
O projeto utiliza uma estrutura de dados `nodo`, que representa cada elemento da pilha:
- **elem**: O elemento armazenado no nodo.
- **prox**: Ponteiro para o próximo nodo na pilha.

A pilha em si é representada pela estrutura `pilha`, que contém:
- **topo**: Ponteiro para o nodo que está no topo da pilha.
- **tamanho**: Inteiro que armazena o número de elementos na pilha.

## Funções Principais
- **criarPilha(pilha *p)**: Inicializa a pilha.
- **pilhaVazia(pilha p)**: Verifica se a pilha está vazia.
- **empilharElemento(pilha *p, elemento e)**: Adiciona um elemento no topo da pilha.
- **desempilharElemento(pilha *p, elemento *e)**: Remove e retorna o elemento no topo da pilha.
- **obterTopo(pilha p, elemento *e)**: Retorna o elemento no topo da pilha sem removê-lo.

## Exemplo de Uso
```c
pilha p;
criarPilha(&p);

elemento e1 = 10;
empilharElemento(&p, e1);

elemento topo;
if (obterTopo(p, &topo)) {
    printf("Elemento no topo: %d\n", topo);
}

elemento desempilhado;
if (desempilharElemento(&p, &desempilhado)) {
    printf("Elemento desempilhado: %d\n", desempilhado);
}
```

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença
Este projeto está licenciado sob a [MIT License](LICENSE).
