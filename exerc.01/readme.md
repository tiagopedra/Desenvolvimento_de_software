1. Identificação simples
Leia os valores abaixo e identifique se cada um deles deve ser armazenado como string, int ou bool no C#:
• “João Pereira”
• 30
• true
• “Rua XV  de Novembro, 500”
• false
#RESPOSTA#
João Pereira” → string (texto – nome da pessoa
30 → int (número inteiro – idade)
true → bool (valor lógico – verdadeiro)
“Rua XV de Novembro, 500” → string (texto – endereço, mesmo contendo número)
false → bool (valor lógico – falso)


2. Classificação em contexto

Um sistema de cadastro precisa guardar as seguintes informações:
• Nome do cliente
• Idade
• CPF (documento numérico mas não usado em cálculos)
• Status se está ativo no sistema (sim ou não)
Classifique cada informação com o tipo de dado correto (string, int ou bool) e explique sua escolha.

#RESPOSTA#
Nome do cliente → string (é texto)
Idade → int (número inteiro usado em cálculos e comparações)
CPF → string (embora seja composto de números, não se faz cálculo com ele e pode começar com zeros)
Status ativo → bool (representa verdadeiro ou falso: ativo ou não ativo)
#JUSTIFICATIVA#
Strings armazenam textos ou dados que não precisam de cálculos.
Int armazena números inteiros para cálculos ou comparações.
Bool é ideal para valores binários (sim/não, ativo/inativo).

3. Corrigindo erros
Analise os exemplos abaixo e identifique onde estão os erros de tipo:
• Uma variável chamada idade recebeu o valor “vinte e cinco”.
• Uma variável chamada nome recebeu o valor 12345.
• Uma variável chamada ativo recebeu o valor “true” (como texto).
Explique por que o C# não aceita essas atribuições e qual seria a forma correta.

#RESPOSTA#
idade = "vinte e cinco"; → Erro: tipo incorreto (texto em vez de número). Correto seria idade = 25;
nome = 12345; → Erro: tipo incorreto (número em vez de texto). Correto seria nome = "12345"; (embora idealmente deva ser um nome real, não número).
ativo = "true"; → Erro: tipo incorreto (texto em vez de booleano). Correto seria ativo = true;
#Por que o C# não aceita?#
O C# é fortemente tipado, portanto cada variável aceita apenas valores do tipo declarado. Não permite atribuir texto a uma variável numérica nem vice-versa sem conversão explícita.


4. Escolha do tipo adequado
Você está criando um sistema para uma loja online e precisa armazenar as seguintes informações:
• Nome do produto
• Preço do produto (apenas número inteiro)
• Disponibilidade do produto (se está disponível ou não)
Defina o tipo de dado para cada informação e justifique sua escolha.
#RESPOSTA#:
Nome do produto → string (texto)
Preço do produto → int (número inteiro, pois não há centavos no enunciado; se houvesse, seria decimal)
Disponibilidade do produto → bool (representa se está disponível – verdadeiro ou falso)
#JUSTIFICATIVA#
Nome precisa armazenar texto.
Preço é um valor numérico para cálculos.
Disponibilidade é um estado binário.

5. Analisando fortemente tipada
Explique com suas palavras o que significa dizer que o C# é fortemente tipado e dê um exemplo simples
do que aconteceria se tentássemos colocar texto em uma variável numérica.

#RESPOSTA#:

Em C#, cada variável tem um tipo definido (string, int, bool etc.) e só pode armazenar valores compatíveis. Se você tentar atribuir um tipo diferente, o compilador gera erro antes de rodar o programa.

Exemplo:
int idade = 20;
idade = "vinte"; // ERRO: não pode atribuir string a uma variável int
