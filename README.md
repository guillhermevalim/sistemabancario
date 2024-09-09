menu * """

[d] Depósito
[s] Saque
[e] Extrato 
[q] Saída 

=> """

saldo = 0 
limite = 500
extrato = ""
numero_saques = 0
LIMITE_SAQUES = 3 

while True 
opcao = input(menu)

if opcao == "d":
    valor = float(input("Informe o valor que deseja depositar: "))
    if valor > 0:
    saldo += valor 
    extrato += f"Depósito R${valor:.2f}\n"

   else: 
     print("Operação mal sucedida! O valor informado não corresponde.")

elif opcao == "s":
    valor = float(input("Informe o valor para realizar a operação de saque: "))


  valor_excedido_saldo = valor > saldo 
  valor_excedido_limite = valor > limite 
  valor_excedido_saque = numero_saques >= LIMITE_SAQUES

  if valor_excedido_saldo
        print("Falha na operação! Você não possui saldo suficiente em conta.")

  elif valor_excedido_limite
        print("Falha na operação! O valor da operação excedeu o limite.") 

  elif valor_excedido_saque
        print("Falha na operação! Número máximo de saques permitidos.")

  elif valor >0:
      saldo -= valor 
      extrato += f"Saque: R${valor:.2f}\n"
      numero_saques +=1 

  else
     print("Falha na operação! O valor infornado é inválido.")

  elif opcao == "e":
       print("\n================ EXTRATO DO CLIENTE===============")
       print("Não foram realizadas operações de movimentação." if not extrato else extrato)
       print(f"\nSaldo: R$ {saldo:.2f})
       print("==================================================")

elif opcao == "q":
    break 

else:
   print("Operação invalidada, por selecione novamente a operação desejada.")
     


     

   
