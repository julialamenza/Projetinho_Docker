# Proketinho_Docker

Como vocês podem ver existem 2 arquivinhos ai o nginx e o mysql, cada um com seu dockerfile.

Então vou ensinar como você sobe cada um ok?

NGINX:

Na pasta do nginx além do Dockerfile temos a pasta web aonde contém um site html
Então para iniciar o container com esse volume você primeiro fará o build para criar a imagem:

docker build -t nginx_ju .

Aonde está ngixin_ju você pode escolher o nome que você quiser e ai a imagem vai subir com esse nome

Depois da imagem criada você vai subir o container:

 docker run -d -p 80:80 -v $('pwd')/web:/var/www/html/ nome_da_imagem
 
 Em nome_da_imagem colocar o nome da imagem criada
 
 Depois você vai no seu navegador e digita 0.0.0.0 e veja se visualiza a página do nginx e posteriormente o 0.0.0.0/seudoc.html para ver se visualiza o documento html que está na pasta web
 
 Vamos para o MYSQL
 
 Primeiro vamos buildar a imagem igual no nginx
 
 docker build -t mysql_ju . 
 
 depois você vai subir o ocntainer lembrando que colocamos uma apste chamada datadir na pasta do mysql e queremos que seus dados do banco fiquem nela
 
  docker run -d -p 3306 -v $('pwd')/datadir:/var/lib/mysql nome_da_imagem
  
   Em nome_da_imagem colocar o nome da imagem criada

  
  PRONTO =)
 
