# Jacccobi-xd
Codigo Jaccobi pibe 



    a = float(input("Ingrese Ax: "))
    b = float(input("Ingrese By: "))
    r1 = float(input("Ingrese el resultado de la Ecuación 1: "))
    c = float(input("Ingrese A_1x: "))
    d = float(input("Ingrese B_1y: "))
    r2 = float(input("Ingrese el resultado de la Ecuación 2: "))
    if abs(a) > abs(b) and abs(d) > abs(c):
    print("\n La matriz es diagonalmente dominante. Jacobi")
    x_viejo = 0.0
    y_viejo = 0.0

    tolerancia = 1e-5
    max_iteraciones = 20


    for k in range(max_iteraciones):

        x_nuevo = (r1 - b * y_viejo) / a
        y_nuevo = (r2 - c * x_viejo) / d

        print(f"Iteración {k+1}: x = {round(x_nuevo, 5)}, y = {round(y_nuevo, 5)}")


        # Comparamos qué tanto cambió lo NUEVO respecto a lo VIEJO
        if abs(x_nuevo - x_viejo) < tolerancia and abs(y_nuevo - y_viejo) < tolerancia:
            print(f|"-> Convergió con éxito en la iteración {k+1}.")
            break

        # AL FINAL DEL PASO: Actualizamos los valores viejos para la siguiente iteración
        x_viejo = x_nuevo
        y_viejo = y_nuevo
        else: 
          print("\nERROR: La matriz NO es diagonalmente dominante.")
          
