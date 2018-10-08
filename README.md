# Derivative-Calculator
This is a calculator for new entry learners on the field of Calculus. You will be able to differentiate various expressions to the first level with this program.

from sympy import Symbol, Derivative, sympify, pprint
from sympy.core.sympify import SympifyError

def derivative(f, var):
  var = Symbol(var)
  d = Derivative(f, var).doit()
  pprint(d)
  
if __name__=='__main__':

  f = input('Enter a function: ')
  var = input('Enter the variable to differentiate with respect to: ')
  try:
     f = sympify(f)
  except SympifyError:
     print('Invalid input')
  else:
     derivative(f, var)
