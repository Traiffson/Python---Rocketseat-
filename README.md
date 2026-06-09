# Python---Rocketseat-
Exercício- Projeto 

1. Adivinhe o Número (Truque de Mágica)
print("🎩 Pense em um número de 1 a 10...")
input("Pronto? Aperte Enter para continuar... ")

print("Estou lendo sua mente... 🔮✨")
input("Concentre-se... Aperte Enter novamente... ")

print("O número que você pensou foi... 7! 😱✨")
print("Uau! Acertei? 😄")


2. Pense em uma Cor

print("🎨 Pense em uma cor bem bonita...")
input("Pronto? Aperte Enter para continuar... ")

print("Estou analisando sua energia cromática... 🌈✨")
input("Quase lá... Aperte Enter de novo... ")

print("A cor que você pensou foi... 💙 AZUL! 😄")


3. Criando uma História Maluca

lugar = input("Digite um lugar: ")
pessoa = input("Digite uma pessoa famosa: ")
objeto = input("Digite um objeto: ")
cor = input("Digite uma cor: ")
verbo = input("Digite um verbo: ")
numero = input("Digite um número: ")

print("\n📖 Sua história maluca:")
print(f"Um dia, no(a) {lugar}, encontrei o(a) {pessoa} segurando um(a) {objeto} {cor}.")
print(f"Ele(a) começou a {verbo} sem parar, e isso durou por {numero} horas! 😂")


4. Meu Crachá de Programador(a)

nome = input("Nome: ")
idade = input("Idade: ")
linguagem = input("Linguagem favorita: ")
emoji = input("Emoji que te representa: ")

print("\n-----------------------------")
print("👩‍💻")
print("Crachá do Dev\n")
print(f"Nome: {nome}")
print(f"Idade: {idade}")
print(f"Linguagem favorita: {linguagem}")
print(f"Emoji: {emoji}")
print("-----------------------------")


5. Oráculo da Sabedoria Python

tema = input("Pergunte sobre um assunto da programação: ").lower()

print("\n🔮 Oráculo diz:")

match tema:
    case "python":
        print("Python é poderoso, simples e domina o mundo da automação! 🐍")
    case "variáveis":
        print("Variáveis guardam valores — trate-as com carinho. 💾")
    case "funções":
        print("Funções tornam seu código organizado como um templo zen. 🧘‍♂️")
    case "listas":
        print("Listas são como mochilas: você guarda tudo nelas. 🎒")
    case _:
        print("Ainda estou aprendendo sobre esse tema... 🤔📚")


6. Quiz de Perguntas e Respostas

perguntas = [
    ["Qual a capital da França?", "paris"],
    ["Quanto é 5 + 7?", "12"],
    ["Qual linguagem estamos estudando?", "python"]
]

acertos = 0

for pergunta, resposta in perguntas:
    print(pergunta)
    chute = input("Resposta: ").lower()

    if chute == resposta:
        acertos += 1
        print("✔️ Acertou!\n")
    else:
        print("❌ Errou!\n")

print(f"Você acertou {acertos} de {len(perguntas)} perguntas!")


7. Número Secreto

secreto = 8
tentativas = 0

print("Tente adivinhar o número secreto! (0 a 10)")

while True:
    chute = int(input("Seu palpite: "))
    tentativas += 1

    if chute == secreto:
        print(f"🎉 Parabéns! Você acertou em {tentativas} tentativas!")
        break
    else:
        print("❌ Errado! Tente novamente.\n")


8. Caça ao Tesouro Espacial

tabuleiro = [[" " for _ in range(3)] for _ in range(3)]
tesouro_linha = 1
tesouro_coluna = 2

def mostrar_tabuleiro():
    for linha in tabuleiro:
        print(linha)

tentativas = 5

print("🪐 Caça ao Tesouro Espacial!")
print("Encontre o tesouro escondido (linha e coluna de 0 a 2).")

for tentativa in range(tentativas):
    print(f"\nTentativa {tentativa + 1} de {tentativas}")
    mostrar_tabuleiro()

    linha = int(input("Linha: "))
    coluna = int(input("Coluna: "))

    if linha not in range(3) or coluna not in range(3):
        print("⚠️ Posição inválida!")
        continue

    if tabuleiro[linha][coluna] != " ":
        print("⚠️ Você já tentou esse espaço!")
        continue

    if linha == tesouro_linha and coluna == tesouro_coluna:
        tabuleiro[linha][coluna] = "💎"
        print("🎉 Você encontrou o tesouro!")
        break
    else:
        tabuleiro[linha][coluna] = "X"
        print("❌ Nada aqui...")

else:
    print("\n⛔ Fim das tentativas!")
    print(f"O tesouro estava em ({tesouro_linha}, {tesouro_coluna}).")

print("\nTabuleiro final:")
mostrar_tabuleiro()
