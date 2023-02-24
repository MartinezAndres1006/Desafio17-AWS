
Como primera consigna me pidieron una comparacion con el middleware compression para verificar cuanto puede comprimir la ruta "/info"

Los resultados me dieron:

💥Sin el compression: 693 B

💥Con el compression: 717 B



Manejo de loggers:

💥Con info lo utilice en la ruta "/info"

💥Con warm lo use con cualquier ruta que no exista en la pagina

💥El ERROR lo utilice en el apartado del login ya que si no acepta algun dato te lo regrese 

Artillery:

Primero hay que tener en cuenta que inicio hay que hacer para cada caso:

💥Para fork utilizamos el comando comun para iniciar el servidor:

npm run start || nodemon app.js


💥Y para cluster utilizamos el siguiente:

node app.js inicio --puerto=1006 --mode=cluster

Para acceder en Artillery utiliza el siguiente comando:

artillery quick --count 30 -n 20 http://localhost:1006 > result_cluster.txt

Y para fork utiliza:

artillery quick --count 30 -n 20 http://localhost:1006 > result_fork.txt





