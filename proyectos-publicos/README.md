## PROYECTO CAMARA MADRID COMERCIO

### comando para instalar el nuevo chart

    # Instala el chart en el namespace "camara-madrid"
        helm install camara-madrid  -n camara-madrid .

    # Instala el chart en el namespace "camara-madrid-test" (importante cambiar el profile a "test")
        helm install --set profile=test camara-madrid-test -n camara-madrid-test .

### Comprobaciones

    # Comprueba que se ha creado el namespace con los pods y otros componentes
        kubectl -n camara-madrid-test get all

    #Comprueba recursos consumidos por los pods
        kubectl top node

        kubectl describe nodes 

### Actualizaciones

    # profile dev
        helm upgrade camara-madrid -n camara-madrid .
    # profile test
        helm upgrade --set profile=test camara-madrid-test -n camara-madrid-test .