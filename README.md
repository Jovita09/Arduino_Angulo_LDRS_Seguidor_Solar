# Arduino_Angulo_LDRS_Seguidor_Solar
Este código para ESP32 controla un actuador lineal basado en la lectura de sensores LDR, ajustando su posición en función de la intensidad de luz detectada. También mide un ángulo con un potenciómetro y envía los datos por serial en formato CSV.

Inicialización:
1.-Se configuran los pines del actuador lineal y los sensores LDR.
2.-Se inicializa la comunicación serial a 115200 baudios.

Lectura de sensores:
3.-Se lee el valor del potenciómetro (pin 25) y se convierte a grados (0-180°).
4.-Se leen los valores de los LDRs (pin 34 y 35), invirtiendo los valores para que valores altos correspondan a más luz.

Control del actuador:
5.-Si la luz en el LDR izquierdo es mayor, el actuador sube.
6.-Si la luz en el LDR derecho es mayor, el actuador baja.
7.-Si no hay una diferencia significativa, el actuador se detiene.

Envío de datos por serial:
8.-Se envían los valores de ángulo, LDR izquierdo y LDR derecho en formato CSV, lo que permite monitorear el sistema en MATLAB o cualquier software serial.
