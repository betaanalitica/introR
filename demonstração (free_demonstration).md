# R - Estruturas de controle - ifelse 

A função ifelse(): Os comandos if() e if() else não são vetorizados, ou seja eles avaliam somente 
um valor por vez. Ou seja para um vetor com n elementos o comado if tem que ser executado n vezes, 
através de um loop for. Uma alternativa para casos como esses é utilizar a função ifelse().

A função ifelse() tem a seguinte estrutura básica:

ifelse(vetor_de_condições, valor_se_TRUE, valor_se_FALSE)

o primeiro argumento é um vetor (ou uma expressão que retorna um vetor) com vários TRUE e FALSE;

o segundo argumento é o valor que sera retornado quando o elemento do vetor_de_condições for TRUE;

o terceiro argumento é o valor que sera retornado quando o elemento do vetor_de_condições for FALSE.
vamos criar o vetor com os números de 1 a 5 e testar se são pares ou ímpares

v = 1:10
vpi = ifelse(((v %% 2) == 0), 0,1)
vrp = ifelse(vpi == 0,"par","impar")
print(paste(v,' = ',vrp))

Vamos testar agora com o pH do solo e mostrar que podemos colocar ifelse dentro de ifelse

 vph = c(7.2,5,7,7.9,4.2,7.01)
 vr = ifelse(vph < 7, "ácido", ifelse(vph == 7, "neutro", "alcalino"))
 print(paste(vph , '=', vr))

