#!/usr/bin/env python3
import subprocess

# Usando input para pegar o alvo
alvo = input("Digite o alvo para fazer o scanning [+] ")

print("\n!!!! ATENÇÃO: esse scan pode ser bem intrusivo !!!!")
print("1 = Scan simples")
print("2 = Scan agressivo (Todos os ports + Versões)")

opcao = input("\nDigite a opção: ")

# Em Python, precisamos de ":" no final do if/elif
if opcao == "1":
    print(f"Rodando o processo simples em {alvo}...")
    # As variáveis dentro do subprocess.run não levam chaves {}, passamos a variável direto
    subprocess.run(["sudo", "nmap", alvo])

elif opcao == "2":
    print(f"Rodando o processo agressivo em {alvo}...")
    # Adicionei a vírgula que faltava entre os argumentos
    subprocess.run(["sudo", "nmap", "-p-", "-sV", alvo])

else:
    print("Opção inválida!")
