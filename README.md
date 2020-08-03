- 4 tipos de produtos podem ser vendidos por preços que variam de $1 a $6.
- a máquina suporta 15 itens de cada produto.
- o dono carrega a máquina com os produtos, informando qual o tipo e preço.
- o usuário pode colocar notas de $1, $2, $5 e $10 na máquina, sendo possível carregar um saldo de até $15.
- o usuário seleciona o produto que quer comprar e adquire o item caso seu saldo seja suficiente e o produto esteja disponível.

----------

o projeto foi feito com esquemático do circuito (Quartus II), mas planejo fazer a versão em Verilog ou VHDL em breve.

----------

no imagem 

Caso I:
Proprietário carrega os preços e as quantidades.
Notar que, quando são colocados os valores 0 e 7, são carregados os valores default de 1 e 6, respectivamente.
11 itens do produto 0 a 2 reais.
14 itens do produto 1 a 1 real (default).
1 item do produto 2 a 3 reais.
11 itens do produto 3 a 6 reais (default).

Caso II:
Usuário carrega nota de 5 reais (opção 10).

Caso III:
Usuário compra o produto 2 (custo: 3 reais). Seu saldo cai para 2 reais. A quantidade disponível do produto 2 vai para zero.

Caso IV: 
Usuário tenta comprar novamente o produto 2, que está indisponível. Seu saldo se mantém em 2 reais.

Caso V:
Proprietário tenta inserir 10 itens do produto 3 na máquina. Antes havia 11, agora há 15 (quantidade máxima) - pois não há como guardar 21 itens.

Caso VI:
Usuário tenta comprar o produto 3 (custo: 6 reais), porém não possui saldo suficiente. A quantidade do produto 3 se mantém em 15, bem como seu saldo também permanece em 2 reais.

Caso VII:
Usuário carrega nota de 10 reais (opção 11). Seu saldo vai para 12 reais.

Caso VIII:
Usuário carrega nota de 2 reais (opção 01). Seu saldo vai para 14 reais.

Caso IX:
Usuário tenta carregar nota de 10 reais (opção 11) - que resultaria num saldo de 24 reais -, porém a nota é rejeitada, já que isso estouraria o valor máximo possível para o saldo (15 reais). Seu saldo permanece em 14 reais.

Caso X:
Usuário carrega nota de 1 real (opção 00). Seu saldo vai para 15 reais.

Caso XI:
Usuário compra produto 0 (custo: 2 reais); seu saldo diminui para 13 reais; a quantidade disponível do produto 0 cai para 10.
Usuário compra produto 1 (custo: 1 real); seu saldo diminui para 12 reais; a quantidade disponível do produto 1 cai para 13.
Usuário tenta comprar produto 2 (custo: 3 reais), mas este se encontra indisponível. Seu saldo se mantém em 12 reais.
Usuário compra produto 3 (custo: 6 reais); seu saldo diminui para 6 reais; a quantidade disponível do produto 3 cai para 14.
Usuário compra produto 0 (custo: 2 reais); seu saldo diminui para 4 reais; a quantidade disponível do produto 0 cai para 9.

Caso XII:
Usuário tenta comprar produto 3 (custo: 6 reais), porém seu saldo é insuficiente. Saldo se mantém em 4 reais; quantidade disponível do produto 3 se mantém em 14.
