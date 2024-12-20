- Construir una transacción con una entrada y una salida.
- Serializarla en formato hexadecimal.
  - **_Guía_**
    ### 1. **Conceptos Previos**
    **Transacciones Bitcoin:**
    - Una transacción contiene entradas (inputs) y salidas (outputs).
    - Una entrada gasta un UTXO (salida no gastada) previo, y una salida especifica un nuevo destinatario.
    **Proceso para Crear una Transacción:**
    1. Identificar el UTXO a gastar.
    2. Crear las salidas deseadas.
    3. Firmar la transacción.
    ***
    ### 2. **Objetivo del Ejercicio**
    Construir una transacción con una entrada y una salida utilizando Rust.
    ***
    ### 3. **Pasos Detallados**
    **Paso 1: Crear un contenedor de transacciones**
    - Usa `Transaction` para construir la estructura básica.
    **Paso 2: Añadir entradas**
    - Crea una entrada usando un hash de transacción previo.
    **Paso 3: Añadir salidas**
    - Especifica un destinatario y una cantidad.
    **Paso 4: Serializar la transacción**
    - Usa funciones de `rust-bitcoin` para convertir la transacción a formato hexadecimal.
    ***
    ### 4. **Código Base**
    ```rust
    rust
    Copy code
    extern crate bitcoin;

    use bitcoin::blockdata::transaction::{Transaction, TxIn, TxOut};
    use bitcoin::util::amount::Amount;

    fn main() {
        // Crear una nueva transacción vacía
        let mut tx = Transaction::default();

        // 1. Añadir entradas (completar)
        // tx.input.push(...);

        // 2. Añadir salidas (completar)
        // tx.output.push(...);

        // Serializar la transacción
        println!("Transacción: {:?}", tx);
    }

    ```
    ***
    ### 5. **Tareas para Resolver**
    1. Construye una transacción que gaste un UTXO ficticio.
    2. Añade una salida que transfiera bitcoins a una dirección dada.
    ***
    ### 6. **Validación**
    - Verifica la transacción utilizando un explorador de bloques.
    ***
    ### 7. **Reflexión Final**
    Este ejercicio introduce cómo funcionan las transacciones y prepara para firmarlas en ejercicios posteriores.
