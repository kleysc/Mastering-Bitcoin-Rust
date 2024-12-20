## **Explorar UTXOs:**
   
   - Consultar UTXOs asociados a una dirección.
   - Crear una transacción que gaste estos UTXOs.
   
   - **_Guía_**
   
       ### 1. **Conceptos Previos**
       **UTXOs (Unspent Transaction Outputs):**
       - Son salidas de transacciones anteriores que no han sido gastadas.
       - Representan la "moneda" que se puede usar en nuevas transacciones.
       **Proceso para Consultar y Gastar UTXOs:**
       1. Identificar la dirección para la que deseas consultar UTXOs.
       2. Usar una herramienta o API para recuperar los UTXOs asociados.
       3. Crear una transacción que gaste estos UTXOs.
   
       ***
   
       ### 2. **Objetivo del Ejercicio**
       Consultar los UTXOs de una dirección Bitcoin y usarlos para construir una nueva transacción.
   
       ***
   
       ### 3. **Pasos Detallados**
       **Paso 1: Consultar los UTXOs**
       - Usa una API (como Blockstream o una instancia de Bitcoin Core).
       - Recupera los detalles de los UTXOs, incluyendo txid, índice, y cantidad.
       **Paso 2: Construir la transacción**
       - Usa los UTXOs como entradas.
       - Define las salidas (destinatarios y cantidades).
       **Paso 3: Firmar y serializar la transacción**
   
       - Firma cada entrada con la clave privada correspondiente.
   
       ***
   
       ### 4. **Código Base**
       ```rust
       extern crate bitcoin;

       use bitcoin::blockdata::transaction::{Transaction, TxIn, TxOut};
       use bitcoin::util::amount::Amount;

       fn main() {
           // Consultar UTXOs de una dirección (simulado)
           let utxos = vec![("txid1", 0, 50000)]; // txid, índice, cantidad en satoshis

           // Crear una transacción que gaste estos UTXOs
           let mut tx = Transaction::default();

           // 1. Agregar entradas (completar)
           // tx.input.push(...);

           // 2. Agregar salidas (completar)
           // tx.output.push(...);

           println!("Transacción construida: {:?}", tx);
       }

       ```

       ***
       
       ### 5. **Tareas para Resolver**
       1. Usa una API para consultar UTXOs reales.
       2. Construye y firma una transacción que gaste esos UTXOs.
       
       ***
       
       ### 6. **Validación**
       - Verifica que la transacción sea válida utilizando un explorador de bloques.
       
       ***
       
       ### 7. **Reflexión Final**
       Este ejercicio conecta los conceptos de UTXOs con la creación de transacciones prácticas.
