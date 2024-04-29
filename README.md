# Grande Hotel Budapeste

💡 A atividade abaixo foi proposta pelo Professor Gabriel Augusto durante o curso do Instituto PROA visando a aprendizagem de Lógica de Programação com JavaScript.


## Conceito da atividade 

Hora de pensar!
Hoje vamos desenvolver um programa feito com vários outros programas utilizando um conceito de software modulado, feito com partes independentes. 
O objetivo é desenvolver uma plataforma para funcionários de um hotel usarem, não os hóspedes. 

## Enunciado da atividade 

Antes de tudo: execute o código proposto e veja como ele se comporta.

Depois disso... De acordo com cada uma das solicitações abaixo, adapte o programa principal: 

    Invente um nome para o Hotel. 
    Ao acessar o sistema, exiba "Bem vindo ao {Hotel}".
    Ao acessar o sistema, pergunte o nome do usuário e uma senha. O nome do usuário não precisa de validação. A senha deve ser 2678.  
    Na função "inicio", utilize escolha/caso (switch/case) para validar a opção escolhida pelo do usuário.
    Sempre que o usuário acessar o sistema, diga "Bem vindo ao Hotel {Hotel}, {Nome}. É um imenso prazer ter você por aqui!".
    Substituir a expressão {Hotel} pelo nome do hotel informado pelo em todos os pontos do código.
    Sempre que o usuário sair do sistema, exiba a mensagem "Muito obrigado e até logo, {Nome}."
    Para cada escolha que o usuário fizer no menu principal, deve ser desenvolvido um programa seguindo as instruções abaixo. Esse programa deve ser criado utilizando uma função principal como chamada. Todo o restante é feito com sua liberdade.
    Atualize o menu de opções e a função inicio com todas as opções de programas abaixo. 
    Atualize a função "erro" com as novas opções do menu.
    Ao encerrar qualquer programa abaixo, sempre retorne ao menu inicial. 


Agora vamos para a parte que interessa! 

### 1) Quantos quartos são?

Todo hotel precisava reservar quartos. 
Então vamos começar por isso. 

Considere que o hotel possui 20 quartos e ao iniciar o programa todos estão livres. 

Desenvolva um programa que: 
1) Receba o valor de uma diária no hotel e a quantidade de dias de hospedagem. Valide as informações, ou seja, impeça que o usuário informe dados inválidos, de maneira que o valor da diária não seja negativo e que a quantidade de dias não seja nem negativa, nem maior que 30. 
Em caso de informação inválida escreva na tela “Valor Inválido” e volte ao inicio do programa. 

2) Em seguida, caso o usuário tenha informado um valor correto, pergunte o nome do hóspede. 

3) Agora será informado o número do quarto (de 1 a 20); A informação deve ser armazenada e se outro hóspede tentar ocupar um quarto já ocupado o sistema informará “Quarto já está ocupado”. No caso de um quarto ocupado, deve ser oferecido ao usuário a escolha de outro quarto. 

4) O próximo passo é perguntar se o usuário confirma a reserva. Caso não aceite, volte ao menu inicial. 

Exemplo 1:
Programa pergunta   =>  "Qual o valor padrão da diária?"
<br>Resposta do usuário =>  -12
<br>Programa exibe      =>   “Valor inválido, {Nome}”

Exemplo 2:
Programa pergunta   =>  "Qual o valor padrão da diária?"
<br>Resposta do usuário =>   55.0
<br>Programa pergunta   =>  "Quantas diárias serão necessárias?"
<br>Resposta do usuário =>  10
<br>Programa exibe      =>  "O valor de 10 dias de hospedagem é de R$550.0"
<br>Programa pergunta   =>  "Qual o nome do hóspede?"
<br>Resposta do usuário =>  Carlos Moreira
<br>Programa pergunta   =>  "Qual o quarto para reserva? (1 - 20)?"
<br>Resposta do usuário =>  7
<br>Programa exibe      =>  "Quarto Livre."
<br>Programa pergunta   =>  "{Nome}, você confirma a hospedagem para Carlos Moreira por 10 dias para o quarto 7 por R$550.0? S/N"
<br>Resposta do usuário =>  S
<br>Programa exibe      =>  "{Nome}, reserva efetuada para Carlos Moreira."

Exemplo 3:
Programa pergunta   =>  "Qual o valor padrão da diária?"
<br>Resposta do usuário =>  55.0
<br>Programa pergunta   =>  "Quantas diárias serão necessárias?"
<br>Resposta do usuário =>  10
<br>Programa exibe      =>  "O valor de 10 dias de hospedagem é de R$550.0"
<br>Programa pergunta   =>  "Qual o nome do hóspede?"
<br>Resposta do usuário =>  Carlos Moreira
<br>Programa pergunta   =>  "Qual o quarto para reserva? (1 - 20)?"
<br>Resposta do usuário =>  2
<br>Programa exibe      =>  "Quarto está ocupado. Escolha outro."
<br>Programa pergunta   =>  "Qual o quarto para reserva? (1 - 20)?"
<br>Resposta do usuário =>  7
<br>Programa exibe      =>  "Quarto Livre."
<br>Programa pergunta   =>  "{Nome}, você confirma a hospedagem para Carlos Moreira por 10 dias para o quarto 7 por R$550.0 ? S/N"
<br>Resposta do usuário =>  S
<br>Programa exibe      =>  "{Nome}, reserva efetuada para Carlos Moreira.."


### 2) Como soletra?

Aqui vamos tratar do cadastro de hóspedes. 
Imagine que uma família acaba de chegar ao balcão do hotel e quer se hospedar. 

Primeiro diremos ao programa o valor padrão da diária e só então cadastraremos todos os hóspedes. 
O programa receberá vários nomes de hóspedes e suas idades, sem limites. 

Caso o hóspede tenha menos de 6 anos, ela ou ele não paga a diária – nesses casos mostre na tela “[Nome do hóspede] possui gratuidade”.
Caso o hóspede tenha mais de 60, ela ou ele paga metade da diária – mostre na tela “[Nome do hóspede] paga meia”.

O usuário informará hóspedes até digitar a palavra “PARE”, que interrompe a entrada de dados. 

Ao fim, mostre a quantidade de gratuidades, a quantidade de meias hospedagens e o valor total, considerando todos os hóspedes informados.

Exemplo:
Programa pergunta   => "Qual o valor padrão da diária?"
<br>Resposta do usuário => 100

<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário => Rosani Albuquerque
<br>Programa pergunta   => "Qual a idade do Hóspede?"
<br>Resposta do usuário => 25
<br>Programa exibe      => "Rosani Albuquerque cadastrada(o) com sucesso."

<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário => Jailson Albuquerque
<br>Programa pergunta   => "Qual a idade do Hóspede?"
<br>Resposta do usuário => 6
<br>Programa exibe      => "Jailson Albuquerque cadastrada(o) com sucesso. Jailson possui gratuidade"

<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário => Gabriel Albuquerque
<br>Programa pergunta   => "Qual a idade do Hóspede?"
<br>Resposta do usuário => 19
<br>Programa exibe      => "Gabriel Albuquerque cadastrada(o) com sucesso."

<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário => Wesley Albuquerque
<br>Programa pergunta   => "Qual a idade do Hóspede?"
<br>Resposta do usuário => 82
<br>Programa exibe	    => "Wesley Albuquerque cadastrada(o) com sucesso. Wesley paga meia"

<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário => PARE
<br>Programa exibe      => "{Nome}, o valor total das hospedagens é: R$250; 1 gratuidade(s); 1 meia(s)"

### 3) Com "S" ou com "Z"?

Aqui vamos tratar do cadastro de hóspedes, mas de uma forma diferente. 
Como no programa anterior, imagine que uma família acaba de chegar ao balcão do hotel e quer se hospedar. 

Monte um programa em que o usuário poderá cadastrar e pesquisar hóspedes. 

O programa deve oferecer um menu com algumas opções ao usuário: 1- cadastrar; 2- pesquisar; 3-listar; 4- sair. 

A opção “cadastrar” deve permitir que o usuário informe um nome de hóspede, gravando-o em memória (máximo de 15 cadastros; caso atinja essa quantidade, mostre “Máximo de cadastros atingido”). 

A opção “pesquisar” deve permitir que o usuário informe um nome e, caso seja encontrado um nome exatamente igual, mostre a mensagem “Hospede (nome) foi encontrado". Se o nome não foi encontrado mostre “Hóspede não encontrado”. 

A opção “listar” exibe todos os hóspedes do hotel um a um. 

O programa deve permitir que o usuário realize essas operações repetidas várias vezes, até que use a opção “4”, que retorna ao menu principal.   

Exemplo 1:
Programa pergunta   =>  "Selecione uma opção: 1. Cadastrar - 2. Pesquisar - 3. Sair"
<br>Resposta do usuário => 1
<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário => Rosani Albuquerque
<br>Programa exibe      => "Hóspede " + nome_hospede + " foi cadastrada(o) com sucesso!"
<br>Programa pergunta   => "Selecione uma opção: 1. Cadastrar - 2. Pesquisar - 3. Sair"

Exemplo 2:  
Programa pergunta   =>  "Selecione uma opção: 1. Cadastrar - 2. Pesquisar - 3. Sair"
<br>Resposta do usuário => 2
<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário => Rosani Albuquerque
<br>Programa exibe      => "Hóspede Rosani Albuquerque foi encontrada(o)!"
<br>Programa pergunta   => "Selecione uma opção: 1. Cadastrar - 2. Pesquisar - 3. Sair"

Exemplo 3:  
Programa pergunta   =>  "Selecione uma opção: 1. Cadastrar - 2. Pesquisar - 3. Sair"
<br>Resposta do usuário => 2
<br>Programa pergunta   => "Qual o nome do Hóspede?"
<br>Resposta do usuário =>  Eleanor Fernandes
<br>Programa exibe      => "Hóspede Eleanor Fernandes não foi encontrada(o)!"
<br>Programa pergunta   => "Selecione uma opção: 1. Cadastrar - 2. Pesquisar - 3. Sair"

### 4) Que horas você pode?
Neste cenário, o hotel receberá não hóspedes, mas eventos. 
Eventos são grandes e complexos, por isso precisamos pensar em diversas situações.
Leia atentamente tudo o que é solicitado.

Importante: as quatro partes abaixo constituem um único programa. 

<h3>Parte 1: Onde será o evento?</h3>

O auditório Laranja conta com 150 lugares e espaço para até 70 cadeiras adicionais. 
O auditório Colorado conta com 350 lugares, sem espaço para mais cadeiras. 

Desenvolva um programa que receba o número de convidados do evento e faça uma verificação sobre a quantidade: se for maior que 350 ou se for menor que zero, mostre a mensagem “Número de convidados inválido”. Se o valor informado é válido, mostre na tela qual dos auditórios é o mais adequado, dando prioridade ao Auditório Laranja.

No caso do auditório Laranja, ainda, calcule quantas cadeiras adicionais serão necessárias, observando o limite citado acima.

Exemplo 1:
Programa pergunta      => "Qual o número de convidados para o seu evento?"
<br>Resposta do usuário    =>  192
<br>Programa exibe         => "Use o auditório Laranja (inclua mais 42 cadeiras)"
<br>Programa exibe         => "Agora vamos ver a agenda do evento." 

Exemplo 2:
Resposta do usuário    => "Qual o número de convidados para o seu evento?"
<br>Resposta do usuário    => 300
<br>Programa exibe         => "Use o auditório Colorado"
<br>Programa exibe         => "Agora vamos ver a agenda do evento."

<h3>Parte 2: Quando será o evento?</h3>

O hotel oferece reserva de seu auditório caso o contratante necessite. O auditório está disponível para reservas de segunda a sexta das 7hs às 23hs; sábados e domingos apenas das 7hs às 15hs. 

1) Monte um programa que receba o dia da semana em texto.
Importante: na entrada de dados para dia da semana, desconsidere acentos e use letra minúscula. Não é necessário validação para isso no código.
2) Também receba a hora (número inteiro, desprezando minutos e segundos)
3) Diga se o auditório está disponível ou  não de acordo com as regras especificadas acima. 
4) Quando o auditório estiver disponível, receba ainda o nome da empresa e mostre na tela a mensagem “Auditório reservado para (nome da empresa): (dia da semana) às (horas)hs”.

Exemplo 1:
Programa pergunta       => "Qual o dia do seu evento?"
<br>Resposta do usuário     => sabado
<br>Programa pergunta       => "Qual a hora do seu evento?"
<br>Resposta do usuário     => 16
<br>Programa exibe          => Auditório indisponível"

Exemplo 2:
Programa pergunta     =>  "Qual o dia do evento?"
<br> Resposta do usuário  =>  segunda
<br>Programa pergunta     =>  "Qual é a hora do evento?"
<br>Resposta do usuário   =>  13
<br>Programa pergunta     =>  "Qual o nome da empresa?"
<br>Resposta do usuário   =>  Lojas Transilvânia
<br>Programa exibe        =>  "Auditório reservado para Lojas Transilvânia. Segunda às 13hs."

<h3>Parte 3: Quantos trabalharão no evento?</h3>

Quando uma empresa contrata o hotel para eventos, são oferecidos garçons para servir os convidados. Considerando que cada garçom custa R$ 10,50 por hora, escreva um programa que receba o número de garçons necessários e o total de horas do evento. Para cada 12 convidados é necessário um garçom, sempre arredondando para cima, e para cada duas horas de evento adicione mais um garçom.  

Depois calcule o custo total que o hotel terá com a contratação desses profissionais e exiba o resultado em tela.

Exemplo:
Programa pergunta      =>  "Qual a duração do evento em horas?"
<br>Resposta do usuário    =>  8 
<br>Programa exibe         =>  "São necessários 48 garçons." 
<br>Programa exibe         =>  "Custo: R$ 504.0"
<br>Programa exibe         =>  "Agora vamos calcular o custo do buffet do hotel para o evento." 

<h3>Parte 4: E quanto ao Buffet?</h3>

O hotel oferece café, água e salgados para cada um dos convidados de um evento alocado em seus salões. A quantidade de café, em litros, é calculada como 0,2 litro para cada convidado; a quantidade de água é calculada como 0,5 litro para cada convidado; são oferecidos 7 salgados por pessoa.

Com a quantidade de convidados informada na Parte 1, calcule a quantidade de água, café e salgados para o evento, mostrando em tela esses valores.
Sabendo que cada litro de café custa, 0,80 centavos, cada litro de água custa 0,40 centavos e o cento de salgados custa 34 reais, calcule o custo total com comida do evento. 

Exemplo:
Programa exibe =>  "O evento precisará de 20 litros de café, 50 litros de água, 700 salgados."

Agora, exiba o relatório com custos e pergunte se o usuário aceita todos os valores informados. 

Exemplo: 

Evento no Auditório Colorado.
<br>Nome da Empresa: Hotel Transivânia.
<br>Data: Segunda, 13H às 21h.
<br>Duração do evento: 8H.
<br>Quantidade de garçons: 48.
<br>Quantidade de Convidados: 192

Custo do garçons: R$504.00
<br>Custo do Buffet: R$274.00

Valor total do Evento: R$ 778.00

Programa pergunta   =>  "Gostaria de efetuar a reserva? S/N"
<br>Resposta do usuário =>  S
<br>Programa exibe          =>  "{Nome}, reserva efetuada com sucesso."

Se "SIM", exiba a mensagem "Reserva efetuada com sucesso". 
<br>Caso contrário, exiba a mensagem "Reserva não efetuada."
<br>Exemplo completo
<br>Programa exibe         => Parte 1: Quantidade de Convidados
<br>Programa pergunta      => "Qual o número de convidados para o seu evento?"
<br>Resposta do usuário    =>  192
<br>Programa exibe         => "Use o auditório Laranja (inclua mais 42 cadeiras)"
<br>Programa exibe         => "Agora vamos ver a agenda do evento."

Programa exibe            => Parte 2: Agenda
<br>Programa pergunta     =>  "Qual o dia do evento?"
<br>Resposta do usuário   =>  segunda
<br>Programa pergunta     =>  "Qual é a hora do evento?"
<br>Resposta do usuário   =>  13
<br>Programa pergunta     =>  "Qual o nome da empresa?"
<br>Resposta do usuário   =>  Lojas Transilvânia
<br>Programa exibe        =>  "Auditório reservado para Lojas Transilvânia. Segunda às 13hs."

Programa exibe           => Parte 3: Agenda
<br>Programa pergunta     =>  "Qual a duração do evento em horas?"
<br>Resposta do usuário   =>  8 
<br>Programa exibe        =>  "São necessários 48 garçons."
<br>Programa exibe        =>  "Custo: R$ 504.0"
<br>Programa exibe        =>  "Agora vamos calcular o buffet do hotel para o evento."

Programa exibe            => Parte 4: Buffet
<br>Programa exibe            =>  "O evento precisará de 20 litros de café, 50 litros de água, 700 salgados."

Programa exibe                => Parte 5: Conferência
<br>Programa exibe            => Evento no Auditório Colorado.
<br>Programa exibe            => Nome da Empresa: Hotel Transivânia.
<br>Programa exibe            => Data: Segunda, 13H às 21h.
<br>Programa exibe            => Duração do evento: 8H.
<br>Programa exibe            => Quantidade de garçons: 48.
<br>Programa exibe            => Quantidade de Convidados: 192
<br>Programa exibe            => Custo do garçons: R$504.00
<br>Programa exibe            => Custo do Buffet: R$274.00

Programa exibe            => Valor total do Evento: R$ 778.00

Programa pergunta    =>  "Gostaria de efetuar a reserva? S/N"
<br>Resposta do usuário  =>  S
<br>Programa exibe       =>  "{Nome}, reserva efetuada com sucesso."

### 5) Álcool ou gasolina?

O hotel tem um carro para levar seus hóspedes a passeios. O carro é sempre abastecido pelo hotel que tem convênios com dois postos de Gasolina: o Wayne Oil e o Stark Petrol. Os carros podem ser abastecidos tanto com álcool quanto gasolina, mas os preços têm flutuado bastante, então é necessário que que um funcionário cheque qual o posto mais em conta para abastecimento. 

Para isso, é necessário desenvolver um programa em que o usuário informe os valores de álcool e gasolina dos dois postos e depois calcule qual o combustível mais atraente e o posto mais barato. Considere que o tanque do carro comporta 42 litros de combústivel e esse sempre será o volume a ser abastecido. 
Considere que quando o álcool estiver 30% mais barato que a gasolina, é mais barato abastecer com álcool.
Dica: Regra de três. 

Exemplo:
Programa pergunta   =>  "Qual o valor do álcool no posto Wayne Oil?"
<br>Resposta do usuário =>  4.20
<br>Programa pergunta   =>  "Qual o valor da gasolina no posto Wayne Oil?"
<br>Resposta do usuário =>  5.82
<br>Programa pergunta   =>  "Qual o valor do álcool no posto Stark Petrol?"
<br>Resposta do usuário =>  4.35
<br>Programa pergunta   =>  "Qual o valor da gasolina no posto Stark Petrol?"
<br>Resposta do usuário =>  6.17
<br>Programa exibe      =>  "{Nome}, é mais barato abastecer com gasolina no posto Wayne Oil".

### 6) Ar puro, finalmente.

A manutenção dos ar-condicionados no hotel é realizada por empresas terceirizadas que, em alguns casos, oferecem desconto quando o serviço é realizado em uma quantidade determinada de aparelhos. 

Dentro desse contexto, crie um programa em que:

    O usuário informe o valor do serviço por aparelho, a quantidade de aparelhos em manutenção, o percentual de desconto (que pode ser zero) e a quantidade mínima de aparelhos para que o desconto seja dado.

    Calcule o valor total do serviço a partir do valor por aparelho e da quantidade de aparelhos. Aplique sobre esse valor o desconto, caso a quantidade de aparelhos seja maior que a mínima informada para que haja desconto. Ao fim mostre a mensagem “O serviço de [nome da empresa] custará R$ [total calculado]”.

    Permita que o usuário informe várias empresas e os outros dados necessários para o cálculo, usando a função/procedimento para mostrar o total orçado de cada empresa. Termine o algoritmo quando o usuário responder ‘N’ à mensagem “Deseja informar novos dados? (S/N)

    Seja possível obter os diferentes valores orçados e verificar o menor valor. Mostre ao final a mensagem “O orçamento de menor valor é o de (nome da empresa) por R$ (menor valor)".

Considere que sempre serão informados ao menos duas empresas. 

Exemplo:
Programa pergunta   =>  "Qual o nome da empresa?"
<br>Resposta do usuário =>  Empresa 1
<br>Programa pergunta   =>  "Qual o valor por aparelho?"
<br>Resposta do usuário =>  100
<br>Programa pergunta   =>  "Qual a quantidade de aparelhos?"
<br>Resposta do usuário =>  7
<br>Programa pergunta   =>  "Qual a porcentagem de desconto?"
<br>Resposta do usuário =>  12
<br>Programa pergunta   =>  "Qual o número mínimo de aparelhos para conseguir o desconto?"
<br>Resposta do usuário =>  3
<br>Programa exibe          =>  "O serviço de Empresa 1 custará R$ 1350.0"

Programa pergunta   =>  "Deseja informar novos dados, {Nome}? (S/N)"
<br>Resposta do usuário =>  S

Programa pergunta   =>  "Qual o nome da empresa?"
<br>Resposta do usuário =>  Empresa 2
<br>Programa pergunta   =>  "Qual o valor por aparelho?"
<br>Resposta do usuário =>  95
<br>Programa pergunta   =>  "Qual a quantidade de aparelhos?"
<br>Resposta do usuário =>  6
<br>Programa pergunta   =>  "Qual a porcentagem de desconto?" 
<br>Resposta do usuário =>  9
<br>Programa pergunta   =>  "Qual o número mínino de aparelhos para conseguir o desconto?"
<br>Resposta do usuário =>  10
<br>Programa exibe      =>  "O serviço de Empresa 2 custará R$1480.0"

Programa pergunta   =>  "Deseja informar novos dados, {Nome}? (S/N)"
<br>Resposta do usuário =>  N
<br>Programa exibe      =>  "O orçamento de menor valor é o [Empresa 1 por R$ 1200.0]"
