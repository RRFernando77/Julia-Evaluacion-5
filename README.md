# Función para calcular el n-ésimo número de Fibonacci usando programación dinámica
function fibonacci_dinamica(n)
    if n < 0
        throw(ArgumentError("n debe ser un número no negativo"))
    end

    # Array para almacenar los resultados intermedios
    fib = Vector{Int64}(undef, n + 1)
    
    # Casos base
    fib[1] = 0
    if n > 0
        fib[2] = 1
    end

    # Calcular los valores de Fibonacci para 2 hasta n
    for i in 3:n+1
        fib[i] = fib[i - 1] + fib[i - 2]
    end

    return fib[n+1]
end

# Imprimir los primeros 10 números de la secuencia de Fibonacci
for i in 0:9
    println("Fibonacci($i) = ", fibonacci_dinamica(i))
end

COMO EJECUTARLO:
-Entrar en la cuenta de drive y crear una copia

-Cuando se haya copiado en el drive hay que darle a ejecutar a ese bloque de código. 
es decir al símbolo de play. Eso es para instalar Julia en la maquina de Google Colabs, y aceptas los permisos

-Y cuando se termine de ejecutar que ya no salga el cuadrado se pide reiniciar la página para que cargue Julia. 
O sea refrescar la página

-Ir a la parte de "Checking the installation" para verificar si tiene Julia instalado, Le das al play en versioninfo(). 
y debería dar una salida algo así:

Julia Version 1.8.2
Commit 36034abf260 (2022-09-29 15:21 UTC)
Platform Info:
  OS: Linux (x86_64-linux-gnu)
  CPU: 2 × Intel(R) Xeon(R) CPU @ 2.20GHz
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-13.0.1 (ORCJIT, broadwell)
  Threads: 2 on 2 virtual cores
Environment:
  LD_LIBRARY_PATH = /usr/local/nvidia/lib:/usr/local/nvidia/lib64
  JULIA_NUM_THREADS = 2

-Si sale asi y no da error es porque Julia ya esta instalado

-Para programar en Julia vas a bajar donde dice "Julia"

-Debajo de Julia se va a dar en Código para agregar código de ejecución, osea el codigo de Fibonacci en Julia

-Colocas el código ahí y listo!! Ahí tienes el Fibonacci en Julia.
