# Flow-4
Aquí se encuentra el ejercicio corespondiente al flow 4

El ejercicio consiste en utilizar el protocolo de comunicación MQTT para mandar datos de la temperatura del lugar donde me encuentro, para posteriormente graficarla mediante Node-Red

Se utilizaran un nodo mqtt in para recibir un mensaje enviado desde terminal, este mensaje contendrá un json con 2 valores, un id y un valor de temperatura. 
Estos pasaran a un nodo json para que se convierta en un objeto de javaScript y posteriormente con un nodo de función asignar el id a el topic del mensaje, y el payload sea la temperatura.

Posteriormente estos valores entraran en un dashboard que contiene una grafica donde se graficaran todas las temperaturas enviadas a ese topic.

Por ultimo se agregara un nodo inject y un nodo mqtt out para automatizar el envío de la temperatura, el nodo injecte mandara un string que contiene el comando en json cada 15 segundos, el mqtt out lo recibirá y lo publicara en el topic.