## **Interacción con Lightning Network:**
   - Crear una conexión con un nodo Lightning.
   - Establecer un canal de pago básico.
  
   - **_Guía_**
       ### 1. **Conceptos Previos**
       **Lightning Network:**
       - Una red de segunda capa construida sobre Bitcoin para permitir transacciones rápidas y económicas.
       - Utiliza canales de pago para transferir fondos off-chain.
       **Elementos Clave:**
       - Canales de Pago: Conexiones entre pares que facilitan las transacciones.
       - Nodos Lightning: Participantes que mantienen canales y enrutamiento.
  
       ***
  
       ### 2. **Objetivo del Ejercicio**
       Conectar con un nodo Lightning y establecer un canal de pago básico.
  
       ***
  
       ### 3. **Pasos Detallados**
       **Paso 1: Configurar un nodo Lightning**
       - Usa `lnd`, `c-lightning` o `eclair` para ejecutar un nodo local.
       **Paso 2: Conectar al nodo**
       - Usa una biblioteca como `rust-lightning` para interactuar con el nodo.
       **Paso 3: Crear un canal de pago**
       - Abre un canal con otro nodo y realiza un pago básico.
  
       ***
  
       ### 4. **Código Base**
       ```rust
       extern crate lightning;

       use lightning::ln::peer_handler::PeerManager;

       fn main() {
           // Configurar un manejador de peers (simplificado)
           let peer_manager = PeerManager::new();

           // Conectar a un nodo Lightning (completar)
           // peer_manager.connect_peer(...);

           println!("Conexión Lightning establecida.");
       }

       ```
       
       ***
       
       ### 5. **Tareas para Resolver**
       1. Configura un nodo Lightning local.
       2. Establece una conexión con un nodo remoto.
       3. Abre un canal de pago.
       
       ***
       
       ### 6. **Validación**
       - Verifica que el canal se haya establecido y que el pago se haya realizado correctamente.
       
       ***
       
       ### 7. **Reflexión Final**
       Este ejercicio introduce conceptos avanzados de Lightning Network, conectando la teoría con la práctica.
