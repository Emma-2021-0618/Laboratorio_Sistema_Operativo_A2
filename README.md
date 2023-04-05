# UCATECI
- Sistemas operativo 2
- Lizandro jose Ramirez
- Encuentro 7 Teoria

# Tema
- Semaforo Python

# Autores
- Enmanuel Sanchez Rodriguez 2021-0618
- Albert Francisco Hernandez Sanchez 2019-0126

# Desarrollo
Librerias las cuales usamos para pdoer correr el codigo de manera correcta y sin fallos desde la librerias de hilos a la de tiempo.
~~~
import threading
from time import sleep
semaforo = threading.Semaphore(2)
n=0
~~~

Declaramos la clase hilos con un argumento de hilo, ademas de al momento de llamarla se inicio una instacia la cual se declara asi mismo con sus propiedades ademas de agregar un metodo run el cual hace la funcion del semaforo y pueda agregar a la lista sus instacias.
~~~
class Hilo(threading.Thread):
    def __init__(self, id):
        threading.Thread.__init__(self)
        self.id = id

    def run(self):
        semaforo.acquire()
        sleep(3-self.id)
        d.append(self.id)
        semaforo.release()
~~~


Se declara los hilos a procesar y el arrays donde se almacenaran.
~~~
d=[]
hilos = [Hilo(1),
Hilo(2),
Hilo(3)]
~~~

Bucle en el cual pasa hilo por hilo y iniciamos cada instacia de lo mismo, luego esperamos paara obtener el semaforo imprimos el estado y lo retiramos.
~~~
for h in hilos:
    h.start()

    sleep(4)
    semaforo.acquire()
    print(d)
    semaforo.release()
~~~


Video explicandolo: 
