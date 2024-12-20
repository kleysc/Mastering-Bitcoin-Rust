## **Scripts de Bitcoin:**

   - Crear y ejecutar un script simple (e.g., `OP_CHECKSIG`).
   - Analizar scripts de transacción de ejemplo.
   
  **_Guía_**
       
       ### 1. **Conceptos Previos**
       
       **Bitcoin Script:**
       - Es un lenguaje de programación simple usado en transacciones Bitcoin.
       - Se utiliza para definir condiciones para gastar UTXOs.
       
       ***
       
       ### 2. **Objetivo del Ejercicio**
       Crear y ejecutar un script simple (e.g., `OP_CHECKSIG`).
       
       ***
       
       ### 3. **Pasos Detallados**
       
       **Paso 1: Crear un script**
       - Define un script utilizando opcodes básicos.
       **Paso 2: Ejecutar el script**
       - Usa una herramienta para simular la ejecución.
       
       ***
       
       ### 4. **Código Base**
       ```rust
       extern crate bitcoin;

       use bitcoin::blockdata::script::Builder;

       fn main() {
           // 1. Crear un script (completar)
           let script = Builder::new()
               .push_opcode(bitcoin::blockdata::opcodes::OP_DUP)
               .push_opcode(bitcoin::blockdata::opcodes::OP_HASH160)
               // Agregar datos y más opcodes
               .into_script();

           println!("Script creado: {:?}", script);
       }

       ```
       
       ***
       
       ### 5. **Tareas para Resolver**
       1. Crea un script que verifique una firma (`OP_CHECKSIG`).
       2. Analiza su resultado.
       
       ***
       
       ### 6. **Validación**
       - Asegúrate de que el script sea válido y funcione como se espera.
       
       ***
       
       ### 7. **Reflexión Final**
       Este ejercicio introduce los fundamentos de Bitcoin Script, la base de las condiciones para gastar UTXOs.
