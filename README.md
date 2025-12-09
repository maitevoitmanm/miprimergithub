def fn_calculadora(a, b, op_aritmetica):
    # Convertir operación a minúsculas
    op_aritmetica = str.lower(op_aritmetica)

    if op_aritmetica == 'suma':
        resultado = a + b

    elif op_aritmetica == 'resta':
        resultado = a - b

    elif op_aritmetica == 'division':
        try:
            resultado = a / b
        except ZeroDivisionError:
            resultado = 'La división por cero no es posible. Intenta nuevamente'

    elif op_aritmetica == 'multiplicacion':
        resultado = a * b

    else:
        resultado = 'Debe indicar una operación válida: suma, resta, division, multiplicacion'

    return resultado
