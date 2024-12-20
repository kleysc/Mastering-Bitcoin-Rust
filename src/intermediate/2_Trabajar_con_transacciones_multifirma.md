## **Trabajar con transacciones multifirma:**
   
   - Crear una transacción P2SH (Pay-to-Script-Hash).
   - Generar una dirección multifirma.
  
  **_Guía_**

       ### 1. **Conceptos Previos**
       
       **Multifirma:**
       - Una transacción multifirma requiere que varias partes firmen para gastar un UTXO.
       - Esto se logra utilizando un script que combina claves públicas y condiciones.
       **Pay-to-Script-Hash (P2SH):**
       - Las direcciones P2SH son más prácticas para scripts avanzados, como multifirma.
       
       ***
       
       ### 2. **Objetivo del Ejercicio**
       Crear una dirección multifirma y construir una transacción que use esa dirección como entrada.
       
       ***
       
       ### 3. **Pasos Detallados**
       **Paso 1: Crear claves públicas**
       - Genera múltiples claves públicas.
       **Paso 2: Crear un script multifirma**
       - Define las condiciones para gastar (e.g., 2 de 3 firmas).
       **Paso 3: Crear una dirección P2SH**
       - Usa el script para generar una dirección P2SH.
       **Paso 4: Construir y firmar la transacción**
       - Crea una transacción que gaste el UTXO asociado.
       
       ***
       
       ### 4. **Código Base**
       
       ```rust
       extern crate bitcoin;

       use bitcoin::blockdata::script::Builder;
       use bitcoin::blockdata::transaction::Transaction;
       use bitcoin::util::address::Address;
       use bitcoin::Network;

       fn main() {
           // Generar claves públicas
           // let keys = vec![...];

           // Crear un script multifirma
           let script = Builder::new()
               .push_int(2) // 2 firmas requeridas
               .push_key(&keys[0])
               .push_key(&keys[1])
               .push_key(&keys[2])
               .push_int(3) // Total de claves
               .push_opcode(bitcoin::blockdata::opcodes::OP_CHECKMULTISIG)
               .into_script();

           // Crear una dirección P2SH
           let address = Address::p2sh(&script, Network::Bitcoin);

           println!("Dirección P2SH: {}", address);
       }

       ```

       ***
       
       ### 5. **Tareas para Resolver**
       1. Genera tres claves públicas.
       2. Crea un script multifirma que requiera dos de tres firmas.
       3. Construye una transacción que gaste este UTXO.
       
       ***
       
       ### 6. **Validación**
       - Usa un explorador de bloques para verificar que el script y la transacción sean válidos.
       
       ***
       
       ### 7. **Reflexión Final**
       Este ejercicio introduce cómo se implementan las transacciones multifirma, fundamentales para aplicaciones como billeteras compartidas.
