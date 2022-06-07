# Integer e Float

Como você já deve ter lido anteriormente, "integer" é o nome dado às variáveis que são tratadas como números inteiros, assim como "float" para números com casas decimais. Basicamente, podemos efetuar diversos tipos de cálculos utilizando qualquer linguagem de programação, e a linguagem Crystal oferece suporte à diversas funções que facilitam o nosso dia-a-dia como desenvolvedor! Abaixo estão alguns exemplos:
```cr
numero = 42

puts 42.gcd(35) # Retornará 7, pois este é o método para encontrar o maior divisor comum de 42 e 35!

numeroFloat = -5.2

!p numeroFloat.abs # Retornará 5.2! Basicamente este método transforma um número negativo em positivo!
!p numeroFloat.round # Retornará -5.0! Este método será utilizado para "arredondar" um número!
```
