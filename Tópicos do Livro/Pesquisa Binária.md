- A Busca Binária é um [[Algoritmo]] que tem como entrada uma lista ordenada de elementos.
- Se o elemento está na lista, essa busca retorna sua posição.
	- Caso contrário, não retornará.
- Pesquisa Estupida: Indo do menor para o maior, ou do inicio da lista até o fim.
	- Complexidade O(n)
- A pesquisa binária tem complexidade log(n)

```python
def pesquisa_binaria(lista, item):
    baixo = 0
    alto = len(lista) - 1
    
    while baixo <= alto:
        meio = (baixo + alto) // 2
        chute = lista[meio]
        if chute == item:
            return meio
        if chute > item:
            alto = meio - 1
        else:
            baixo = meio + 1
    return None

minha_lista = [1, 3, 5, 7, 9]
print(pesquisa_binaria(minha_lista, 3)) 
print(pesquisa_binaria(minha_lista, -1))
```

# Exercícios 
1.1 - Suponha que você tenha uma lista com 128 nomes e esteja fazendo uma pesquisa binária. Qual seria o número máximo de etapas que você levaria para encontrar o nome desejado?
$$
	log_2(128) = 7
$$
1.2 - Suponha que você duplique o tamanho da lista. Qual seria o número máximo de etapas agora?
$$
	2^7 = 2*2*2*2*2*2*2 = 128
$$$$
	2^8 = 2^7 * 2 = 256
$$
