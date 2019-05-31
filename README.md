# ¿Que es?

> Convex es un script de código abierto que te permite implementar en tu programa/script/snippet un proxy para obtener mayor protección a la hora de realizar conexiones en el exterior

# Requerimientos

* Python2.x (python >= 3 no probado)
* Módulo socks de python
* Librería de socket estándar (pre instalada)

# Instalación

```
[Linux y derivados] - No te asustes, lo puedes hacer en Windows descargando e instalando la librería socks
sudo apt-get install python-socks
git clone https://github.com/DtxdF/convex.git
```

# Uso

*Para usar este script sólo debes seguir dos pasos:*

1. Importar

`import convex`

2. Ejecutar la función encargada (rellenando la información al menos que se quiera dejar por defecto: (proxy_type=socks.PROXY_TYPE_SOCKS4, proxy_addr="127.0.0.1:9050", rdns=True, username=None, password=None)

`convex.transfor() # como ven ejecuto la función con la información por defecto, uso la dirección estándar de **Tor** para este ejemplo`

# Ejemplo

Para esta explicación usaré la librería **requests**:

```
import requests
import convex

convex.transfor()

data = requests.get("http://ip-api.com/json").json()

for key, value in data.items():

    print("℅s => ℅s" ℅ (str(key), str(value)))

# Si queremos volver a tener nuestra dirección IP

convex.restruct()
```
