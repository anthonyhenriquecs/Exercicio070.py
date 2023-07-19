# Exercicio070.py

total = totm = menor = cont = 0
while True:
    produto = str(input('Produto:'))
    preco = float(input('Preço:'))
    cont += 1
    total += preco
    if preco < 1000:
        totm += 1
    if cont == 1:
        menor = preco
    else:
        if preco < menor:
            menor = preco
    resp = ' '
    while resp not in 'SN':
        resp = str(input('quer continuar? [S/N]')).strip().upper()[0]
    if resp == 'N':
        break
print('{:-^40}'.format('Fim do programa'))
print(f'O total da compra foi: {total:10.2f}')
print(f'{totm} produtos custaram mais de 1000 reais.')
print(f'O produto mais barato custa:{menor}')

