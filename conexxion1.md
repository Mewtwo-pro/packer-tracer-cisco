
    

#ejemplo de coneccion exitosa
    
### 1. Dispositivos de la Izquierda

* **PC2 (`PC-PT`):**
* **Dirección IPv4:** `192.168.1.2` (configurada en la sección Desktop > IP Configuration)
* **Máscara de subred:** `255.255.255.0`
* **Puerta de enlace predeterminada (Default Gateway):** `192.168.1.1`


* **Router2:**
* **Interfaz `FastEthernet0/0**` (Conectada hacia el Switch2 y la PC2):
* Estado: **Encendida (On)**

* Dirección IPv4: `192.168.1.1`

* Máscara de subred: `255.255.255.0`



* **Interfaz `FastEthernet0/1` o Serial** (Enlace hacia el Router3):
* Debe estar **Encendida (On)**.
* Dirección IPv4 de ejemplo: `10.0.0.1`
* Máscara de subred: `255.255.255.0` (recomendada para unificar con el Router3).


* **Ruta Estática configurada en Router2:**
* Red Destino: `192.168.2.0`
* Máscara: `255.255.255.0`
* Siguiente salto (Next Hop): `10.0.0.2` (IP del Router3)





---

### 2. Dispositivos de la Derecha

* **PC3 (`PC-PT`):**
* **Dirección IPv4:** `192.168.2.2` (asignada en su configuración de red)
* **Máscara de subred:** `255.255.255.0`
* **Puerta de enlace predeterminada (Default Gateway):** `192.168.2.1` (IP del puerto del Router3)


* **Router3:**
* **Interfaz `FastEthernet0/1**` (Conectada hacia el enlace del Router2):
* Estado: **Encendida (On)**

* Dirección IPv4: `10.0.0.2`

* Máscara de subred: Cambiar a `255.255.255.0` (en tu captura actual aparecía `255.0.0.0`, la cual debes corregir para que coincida con el Router2).


* **Interfaz `FastEthernet0/0**` (Conectada hacia el Switch3 y la PC3):
* Estado: **Encendida (On)**
* Dirección IPv4: `192.168.2.1`
* Máscara de subred: `255.255.255.0`


* **Ruta Estática configurada en Router3:**
* Red Destino: `192.168.1.0`

* Máscara: `255.255.255.0`

* Siguiente salto (Next Hop): `10.0.0.1` (IP del Router2)





![Conexión One](https://raw.githubusercontent.com/Mewtwo-pro/imagenes-info/main/conexionone.png)

