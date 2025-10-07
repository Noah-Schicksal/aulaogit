# Aula de Python feita as pressas

# O que é o Python? 

Python é uma linguagem de programação de tipagem dinamica e forte

## principais características do Python

- sintaxe limpa
    - códigos em python são mais legiveis e fáceis de entender

-multiparadigma
    - suporta vários paradigmas de programação como POO, programação funcional e procedural

-versatilidade
    -Python é muito versátil. Pode ser usado para desenvolver aplicativos web, automação, análise de dados, inteligência artificial, machine learning, automação de tarefas, desenvolvimento de jogos e etc

## declaração de variaveis

por ser uma linguagem dinamica, declarar variaveis em python é muito fácil, pois a linguagem não pede que o tipo seja declarado, o próprio python identifica

## exemplo de declaração de variaveis

```python 
#valor inteiro : variável do tipo int
idade = 25

#texto : variável do tipo str
nome = "João"

#valor decimal: variável do tipo float
altura = 1.75

#valor booleano: variaável do tipo bool
is_student = True

#uma lista/array
notas = [8, 9, 7, 10]
```

## também se pode forçar o tipo de variável

```python
numero = int(1.20)
```
ou
```python
numero = float(1)
```

## comandos input e output

o comando input permanece igual na declaração de variáveis, por ex:

```python
variavel = input("digite aqui seu input: ")
```

por padrão tudo digitado em um input é definido como tipo _str_ caso o esperado seja um número, precisa ser convertido, um exmplo de como fazer isso é:

```python
variavel = int(input("Digite um número inteiro: "))
```

## comandos if e else

mesmo diferente do que aprendemos no simulador de javascript, os comandos if e else ainda são bem parecidos, dispensando o uso de "()" para condições e de "{}" para código executavel, usando apenas identação correta, ex: 

```python
num1 = 1
num2 = 2

if num1 > num2:
    print("num1 é maior que num2")
else:
    print("num2 é maior que num1")
```

## comando while

funciona da mesma forma que aprendemos no minicurso de javascript, porém, sem "()" para condições e sem "{}" para código executavel, ex:

```python
contador = 0

while contador < 10:
    contador +=  1
```

# E por ultimo, Try

try lida com excessões (erros), usando o try, podemos tratar um erro e evitar que o programa quebre ao encontrar esse erro,  try é uma estrutura em Python para "tentar" executar um pedaço de código que pode dar erro, e caso dê erro, você pode "capturar" e tratar esse erro para evitar que o programa pare de funcionar.

estrutura básica de um try:

```python
try:
    # código que pode gerar um erro
except TipoDeErro:
```

# E agora?

bora praticar

primeiro vamos fazer um pequeno sistema que pede uma senha númerica ao usuário, no entanto temos um problema, usar "var = int(input())", gera erro se o valor digitado não for um número inteiro, nossa missão é tratar esse erro


ex1:

```python
entrada = int(input("Digite um número inteiro: "))
```

ex2:

```python
entrada = input("Digite um número inteiro: ")
senha = int(entrada)
```

ex3:

```python
entrada = input("Insira sua senha: ")

while True:
    try:
        senha = int(entrada)
        break  # se conseguimos converter, encerramos o loop
    except ValueError:
        print("Erro: a senha digitada deve ser um número")
        entrada = input("Insira sua senha novamente: ")

print("Senha digitada:", senha)
```