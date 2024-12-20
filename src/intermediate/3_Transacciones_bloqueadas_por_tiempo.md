## **Transacciones bloqueadas por tiempo:**
   - Construir una transacción que solo pueda gastarse después de un bloque específico (timelock).
   
   - **_Guía_**
   
       ### 1. **Conceptos Previos**
       **Timelock:**
       - Es una restricción que bloquea la transacción hasta un bloque o tiempo específico.
       **Tipos de Timelocks:**
       - `nLocktime`: Bloquea toda la transacción.
       - `OP_CHECKLOCKTIMEVERIFY`: Bloquea solo un script específico.
   
       ***
   
       ### 2. **Objetivo del Ejercicio**
       Construir una transacción que solo pueda gastarse después de un bloque o tiempo determinado.
       
       ***
       
       ### 3. **Pasos Detallados**
   
       **Paso 1: Crear un script con `OP_CHECKLOCKTIMEVERIFY`**
       - Define una condición de tiempo.
       **Paso 2: Crear la transacción**
       - Usa el script como una salida.
       **Paso 3: Gastar la transacción**
       - Intenta gastar la transacción antes y después del tiempo bloqueado.
   
       ***
   
       ### 4. **Código Base**
       ```rust
       extern crate bitcoin;

       use bitcoin::blockdata::script::Builder;
       use bitcoin::blockdata::transaction::Transaction;
       use bitcoin::Network;

       fn main() {
           // Crear un script con timelock
           let script = Builder::new()
               .push_int(500000) // Bloque 500,000
               .push_opcode(bitcoin::blockdata::opcodes::OP_CHECKLOCKTIMEVERIFY)
               .push_opcode(bitcoin::blockdata::opcodes::OP_DROP)
               .push_opcode(bitcoin::blockdata::opcodes::OP_DUP)
               .push_opcode(bitcoin::blockdata::opcodes::OP_HASH160)
               .into_script();

           println!("Script con timelock: {:?}", script);
       }

       ```
       ***

       ### 5. **Tareas para Resolver**
       1. Define un script con `OP_CHECKLOCKTIMEVERIFY`.
       2. Crea una transacción que lo utilice como salida.
       
       ***
       
       ### 6. **Validación**
       - Intenta gastar la transacción antes del tiempo especificado y verifica que sea rechazada.
       ***
       ### 7. **Reflexión Final**
       Este ejercicio te enseña cómo controlar cuándo una transacción puede gastarse, lo cual es útil para contratos inteligentes básicos.
