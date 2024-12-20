## **Decodificar una transacción Bitcoin:**

   - Parsear una transacción codificada en hexadecimal.
   - Extraer sus entradas, salidas y otros detalles.

  ## **_Guía_**

    ### 1. **Conceptos Previos**
    **Transacciones Bitcoin:**
    - Las transacciones están serializadas en un formato binario compacto.
    - Decodificar una transacción implica interpretar sus entradas y salidas.
    **Estructura de una Transacción:**
    - Incluye un identificador de versión, inputs, outputs, y un locktime.
    ***
    ### 2. **Objetivo del Ejercicio**
    Decodificar una transacción Bitcoin en formato hexadecimal y extraer sus entradas, salidas, y demás información.
    ***
    ### 3. **Pasos Detallados**
    **Paso 1: Proveer la transacción hex**
    - Usa una transacción hexadecimal de ejemplo.
    **Paso 2: Parsear la transacción**
    - Usa la función `deserialize` para convertirla a una estructura de Rust.
    **Paso 3: Extraer datos**
    - Itera por las entradas y salidas para obtener detalles como direcciones y cantidades.
    ***
    ### 4. **Código Base**
    ```rust
    rust
    Copy code
    extern crate bitcoin;

    use bitcoin::consensus::deserialize;
    use bitcoin::blockdata::transaction::Transaction;

    fn main() {
        // Hexadecimal de una transacción (reemplazar con un valor real)
        let tx_hex = "0200000001...";

        // 1. Decodificar la transacción (completar)
        let tx: Transaction = deserialize(&hex::decode(tx_hex).unwrap()).unwrap();

        // 2. Imprimir detalles de la transacción
        println!("Transacción decodificada: {:?}", tx);
    }

    ```
    ***
    ### 5. **Tareas para Resolver**
    1. Usa una transacción real en formato hexadecimal.
    2. Extrae y muestra información como las direcciones de salida y los valores.
    ***
    ### 6. **Validación**
    - Compara los datos extraídos con un explorador de bloques.
    ***
    ### 7. **Reflexión Final**
    Este ejercicio te enseña cómo interpretar datos en crudo, una habilidad esencial para trabajar con la blockchain.
