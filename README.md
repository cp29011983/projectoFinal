class receta(object):

    def __init__(self, a, b, c, d, e, f):
        self.huevomarca = a
        self.huevocantidad = b
        self.jamonmarca = c
        self.jamoncantidad = d
        self.salmarca = e
        self.salcantidad = f


def cantidad(n):
    return n * 2


if __name__ == "__main__":
    i = []

    while True:
        print("1********HAGAMOS OMELET**")
        print("2.NO quiero hacer omelet")
        q = 0
        choice = input("A cocinar? ")
        if choice == '2':
            t = len(i)
            if t > 0:
                print("Preparastes " + str(t) + " omelet")
            exit()
        elif choice == '1':
            while True:
                print("******************Que marca? ")
                print("1 Fidanque")
                print("2 Toledano")
                print("3 Salir")
                choicehuevo = input("Cual marca usaras? ")
                if choicehuevo == '3':
                    q = 1
                    break
                elif choicehuevo == '1':
                    marcahuevo = "Fidanque"
                    break
                elif choicehuevo == '2':
                    marcahuevo = "Toledano"
                    break
                else:
                    print("Solo es valido 1, 2, o 3")
            if q == 1:
                break
            while True:
                try:
                    testcanthuevo = 1
                    choicecanthuevo = int(input("Cuantos huevos son? "))
                except ValueError:
                    testcanthuevo = testcanthuevo - 1
                    print("Numero entero por favor" )
                if testcanthuevo == 1:
                    break
            while True:
                print("******************Que Sal? ")
                print("1 Sal Solar")
                print("2 Cristalina")
                print("3 Salir")
                choicesal = input("Cual marca usaras? ")
                if choicesal == '3':
                    q = 1
                    break
                elif choicesal == '1':
                    marcasal = "Sal Solar"
                    break
                elif choicesal == '2':
                    marcasal = "Cristalina"
                    break
                else:
                    print("Solo es valido 1, 2, o 3")
            if q == 1:
                break
            while True:
                try:
                    testcantsal = 1
                    choicecantsal = int(input("Cuantas pizcas de sal hay? "))
                except ValueError:
                    testcantsal = testcantsal - 1
                    print("Numero entero por favor")
                if testcantsal == 1:
                    break
            while True:
                print("******************Que Jamon? ")
                print("1 Kienner")
                print("2 Blue Ribbon")
                print("3 Salir")
                choicejamon = input("Cual marca usaras? ")
                if choicejamon == '3':
                    q = 1
                    break
                elif choicejamon == '1':
                    marcajamon = "Fidanque"
                    break
                elif choicejamon == '2':
                    marcajamon = "Toledano"
                    break
                else:
                    print("Solo es valido 1, 2, o 3 ")
            if q == 1:
                break
            while True:
                try:
                    testcantjamon = 1
                    choicecantjamon = int(input("Cuantos jamones son? "))
                except ValueError:
                    testcantjamon = testcantjamon - 1
                    print("Numero entero por favor")
                if testcantjamon == 1:
                    break
            preparado = receta(marcahuevo, choicecanthuevo, marcasal, choicecantsal, marcajamon, choicecantjamon)
            i.append(preparado)
            final = cantidad(preparado.huevocantidad)
            print("****************************Alcanza para " + str(final))
            print("")
        else:
            print("")




