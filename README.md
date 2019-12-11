#-------------------------------------------------#
#Script metodo Bissecção com Python
#Aluno Edilson Tarcio Braga da Silva
#Discplina de Cálculo Númerico Computacional
#Faculdade IBRATEC
#-------------------------------------------------#
#
#importando biblioteca matemática

import math

#definindo intervalo (a,b) e um erro E

a = 1
b = 8
E = 0.01

#definindo uma função com parametro x

def f(x): 
  return x**2 - 5 #equivalente a(X² -5)

#teorema de bissecção

if f(a)*f(b) < 0:
    
  while (math.fabs(b-a)/2 > E): #loop para encontrar a raiz
    raiz = (a+b)/2
    if f(raiz) == 0:
      print("A raiz é: ", raiz)
      break
    else:
      if f(a)*f(raiz) < 0: #verificando qual lado está a raiz
        b = raiz
      else:
        a = raiz
        
  #após passar por todos os loops encontra a raiz      
  print("valor da raiz é: ", raiz) 

else:
  print(" Não existe raiz neste intervalo!")
