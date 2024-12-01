# -usr-bin-python3-home-usuario-Calculador_massa-calculador.py
Calculador_IMC
def calcular_imc(peso, altura):
    # Calcula o IMC usando a fórmula
    imc = peso / (altura ** 2)
    return imc

def classificar_imc(imc):
    # Classifica o IMC de acordo com as categorias padrão
    if imc < 18.5:
        return "Abaixo do peso"
    elif 18.5 <= imc < 24.9:
        return "Peso normal"
    elif 25 <= imc < 29.9:
        return "Sobrepeso"
    elif 30 <= imc < 34.9:
        return "Obesidade Grau I"
    elif 35 <= imc < 39.9:
        return "Obesidade Grau II"
    else:
        return "Obesidade Grau III"

# Solicita os dados ao usuário
peso = float(input("Digite seu peso em kg: "))
altura = float(input("Digite sua altura em metros: "))

# Calcula o IMC e exibe o resultado com a classificação
imc = calcular_imc(peso, altura)
classificacao = classificar_imc(imc)

print(f"Seu IMC é: {imc:.2f}")
print(f"Classificação: {classificacao}")
