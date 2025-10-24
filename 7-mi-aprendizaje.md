# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  
Si solucionó un problema presentado al realizar la práctica también se debe documentar.

# Reflexión Profesional sobre la Evolución de Competencias en Docker 
La realización de esta práctica ha marcado un salto significativo desde un conocimiento básico y superficial de Docker hacia una competencia avanzada y práctica, fundamental para mi desarrollo profesional en el ámbito de la infraestructura y DevOps.

El principal cambio radica en pasar de simplemente ejecutar contenedores a poder diseñar, asegurar y mantener aplicaciones contenterizadas que cumplen con estándares de rendimiento y disponibilidad en entornos de producción.
Obstáculos Superados y Aprendizaje Derivado
Durante el ejercicio, enfrenté desafíos prácticos que reforzaron la comprensión de los mecanismos internos de Docker:

Fallo de Comandos de Instalación (Ej. yum -y update):

Problema: La instrucción RUN para actualizar el sistema base fallaba sin una causa clara.

Solución y Aprendizaje: Se aprendió a usar flags de depuración como --progress=plain para ver el log detallado, identificando y resolviendo el problema con cambios en la imagen base o forzando la reconstrucción (--no-cache). Esto subraya la necesidad de depurar capas durante la construcción.

Rutas Absolutas en COPY no Funcionaban:

Problema: El comando COPY ./web... no encontraba los archivos fuente.

Solución y Aprendizaje: Se comprendió que Docker utiliza el Contexto de Build (el directorio donde se ejecuta docker build) como punto de referencia para todas las operaciones de copia. La solución fue simple: asegurar la correcta ubicación de ejecución (Set-Location), reforzando un concepto básico pero vital de la herramienta.

Mapeo de Puertos Incompleto con -P:

Problema: A pesar de usar -P (publicación automática), los puertos no se abrían externamente.

Solución y Aprendizaje: Se descubrió que -P solo publica los puertos que han sido declarados explícitamente con EXPOSE dentro del Dockerfile. Esto clarificó la diferencia entre la declaración interna (EXPOSE) y el mapeo externo (-P o -p).
