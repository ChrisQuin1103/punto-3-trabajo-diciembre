# punto-3-trabajo-diciembre
def obtener_estado_salud(imc):
    # Determinar el estado de salud según el IMC
    if imc < 18.5:
        return "peso ideal"
    elif 18.5 <= imc < 24.9:
        return "Peso ideal"
    elif 25 <= imc < 29.9:
        return "Sobrepeso"
    elif 30 <= imc < 34.9:
        return "Obesidad grado I"
    elif 35 <= imc < 39.9:
        return "Obesidad grado II"
    else:
        return "Obesidad grado III"

def main():
    # Inicializar contadores
    peso_ideal = 0
    obesidad_grado_I = 0
    obesidad_grado_II = 0
    obesidad_grado_III = 0
    sobrepeso = 0

    # Registrar información de 20 estudiantes
    for i in range(20):
        print(f"\nEstudiante {i + 1}:")
        peso = float(input("Ingrese el peso en kilogramos: "))
        altura = float(input("Ingrese la altura en metros: "))

        # Calcular el índice de masa corporal (IMC)
        imc = peso / (altura ** 2)

        # Obtener el estado de salud del estudiante
        estado_salud = obtener_estado_salud(imc)

        # Actualizar contadores según el estado de salud
        if estado_salud == "Peso ideal":
            peso_ideal += 1
        elif estado_salud == "Sobrepeso":
            sobrepeso += 1
        elif estado_salud == "Obesidad grado I":
            obesidad_grado_I += 1
        elif estado_salud == "Obesidad grado II":
            obesidad_grado_II += 1
        elif estado_salud == "Obesidad grado III":
            obesidad_grado_III += 1

    # Mostrar el reporte
    print("\nReporte de Salud:")
    print(f"a. Estudiantes en peso ideal: {peso_ideal}")
    print(f"b. Estudiantes en obesidad grado I: {obesidad_grado_I}")
    print(f"c. Estudiantes en obesidad grado II: {obesidad_grado_II}")
    print(f"d. Estudiantes en obesidad grado III: {obesidad_grado_III}")
    print(f"e. Estudiantes en sobrepeso: {sobrepeso}")

if __name__ == "__main__":
    main()
