# formas_de_pagamento
ESSE PROGRAMA DE ESTUDO CALCULA AS FORMAS DE PAGAMENTO DE UM CLIENTE EM DETERMINADA LOJA.

import emoji
print ('{:=^50}'.format('\033[1;33mLOJAS LUCAS IMPORTS\033[m'))
produto = float(input('\033[1mDigite o valor das compras:\033[m'))
print(emoji.emojize('\n\033[1mQual seria a melhor opção para você? :winking_face:'))
print('''\n[1] À VISTA NO DINHEIRO OU CHEQUE
[2] À VISTA NO CARTÃO
[3] EM 2X NO CARTÃO
[4] EM 3X OU MAIS NO CARTÃO\033[m''')
opção = int(input('\n\033[1mQual opção você deseja:\033[m'))
if opção == 1:
    print(emoji.emojize('''\n\033[1mPAGANDO À VISTA VOCÊ TEM 10% DE DESCONTO! :smirking_face:
VALOR TOTAL: R$ {:.2f}'''.format(produto-(produto * 0.10))))
elif opção == 2:
    print(emoji.emojize('''\n\033[1mPAGANDO À VISTA NO CARTÃO VOCÊ TEM 5% DE DESCONTO! :face_savoring_food:
VALOR TOTAL: R$ {:.2f}'''.format(produto-(produto * 0.15))))
elif opção == 3:
    print(emoji.emojize('''\n\033[1mDA PRA DIVIDIR EM 2X SEM JUROS! :money_mouth_face:
    VALOR TOTAL: R$ {:.2f}'''))
else:
    total = produto + (produto * 0.20)
    parc = int(input('\033[1mQuantas parcelas?\033[m'))
    juros = total / parc
    jurost = parc * juros
    print(emoji.emojize('''\n\033[1mCOM JUROS NO CARTÃO EM 3X OU MAIS!\033[m :index_pointing_up:
\033[0;31mconsulte um de nossos atendentes para maiores informações!\033[m
\n\033[1mVALOR TOTAL DAS COMPRAS: R$ {:.2f}
PARCELANDO EM {}x VOCÊ PAGARÁ R$: {:.2f} CADA PARCELA!
UM TOTAL DE R$: {:.2f} COM JUROS\033[m'''.format(produto, parc, juros, jurost )))
