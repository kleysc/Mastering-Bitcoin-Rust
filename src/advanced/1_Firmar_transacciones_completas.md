## **Firmar transacciones completas:**
   - Crear una transacción sin firmar (raw transaction).
   - Firmarla usando una clave privada.
 
   - **_Guía_**
 
       ### 1. **Conceptos Previos**
       **Raw Transactions:**
       - Son transacciones no firmadas, listas para ser completadas.
       **Firma:**
       - Involucra firmar cada entrada con la clave privada correspondiente.
 
       ***
 
       ### 2. **Objetivo del Ejercicio**
       Construir una transacción sin firmar y completarla añadiendo las firmas necesarias.
 
       ***
 
       ### 3. **Pasos Detallados**
       **Paso 1: Crear una transacción sin firmar**
       - Define inputs y outputs.
       **Paso 2: Calcular el hash de la transacción**
       - Usa un algoritmo de hash doble.
       **Paso 3: Firmar cada entrada**
       - Usa la clave privada para firmar las entradas.
 
       ***
 
       ### 4. **Código Base**
       ```rust
       extern crate bitcoin;

       use bitcoin::blockdata::transaction::{Transaction, TxIn, TxOut};
       use bitcoin::util::key::PrivateKey;
       use bitcoin::secp256k1::Secp256k1;

       fn main() {
           let secp = Secp256k1::new();

           // Crear una transacción sin firmar (completar)
           let mut tx = Transaction::default();

           // Agregar entradas y salidas
           // tx.input.push(...);
           // tx.output.push(...);

           // Firmar la transacción (completar)
           println!("Transacción firmada: {:?}", tx);
       }

       ```

       ***

       ### 5. **Tareas para Resolver**
       1. Define una transacción sin firmar con entradas y salidas.
       2. Firma cada entrada con la clave privada correspondiente.

       ***

       ### 6. **Validación**
       - Usa herramientas externas para verificar la transacción firmada.

       ***

       ### 7. **Reflexión Final**
       Este ejercicio te prepara para trabajar con transacciones completas, el núcleo de cualquier aplicación de Bitcoin.
