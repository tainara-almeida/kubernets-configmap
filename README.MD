Nginx + Config Map (CM)


Antes vamos ver sobre o configmap 
 Criar os seguintes recursos:
* Criar um namespace: web -> OK

* Criar um configmap com base no arquivo:
   * nome do arquivo: index.html
   * nome do configmap: indexsite
   * namespace: web

* Criar um deployment:   -> OK
   * Name: webserver-com-cm
   * namespace: web
   * image: nginx:latest
   * replicas: 2
   * o configmap deve ser montado no seguinte diretorio:  /usr/share/nginx/html com o nome de index.html

 * Criar um service para o deployment criado anteriormente  -> OK
    * Nome: webserver-service
    * Tipo: NodePort
