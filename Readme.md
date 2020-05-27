<h1>Docker_Crud</h1>
<p align="justify">O objetivo deste repositório é apresentar um exemplo simples de cadastro em que 
    os ambientes de produção foram construídos a partir de containers e imagem do Docker. Trata-se d eum repositório
    utilizado para o estudo do autor e assim podem haver alguns erros na implementação.
    A maior parte dos códigos foram retirados do curso da COD3R sobre Docker e assim os créditos devem ser dadas ao mesmo.
    Em especial, agradecimentos as aulas do professore Leonardo Moura Leitão.
</p>

<h3>Resultado Final</h3>
<p>Como resultado das aulas foi possível construir um cadastramento simples mas funcional e modularizado pelos containers de frontend, backend e banco de dados em mongodb.</p>
<img src="Crudexemplo.png"/>

<h3>Minhas anotações...</h3>
<p>Anotações sobre os comandos básicos do Docker, em especial ao instalar e usos iniciais:</p>

<p><b>1) Verificação de Instalação:</b></p>

<code>docker container run hello-world</code>

<p><b>2) Em caso de erro rodar:</b></p>

<p>sudo groupadd docker</p>
<p>sudo usermod -aG docker ${USER}</p>
<p>newgrp docker</p>
<p>docker run hello-world</p>

<p><b>3) Testando novamente:</b></p>

<p>docker container run hello-world</p>

<p><b>4) Verificando as versões:</b></p>

<p>bash --version</p>
<p>docker container run debian bash --version</p>

<p><b>5) Agora verificando container ativo:</b></p>

<p>docker container ps</p>

<p><b>6) Remover um container:</b></p>

<p>docker container run --rm debian bash --version</p>

<p><b>7) Para entrar no container (no terminal):</b></p>

<p>docker container run -it debian bash</p>

<p><b>8) Criação de arquivos dentro do container:</b></p>

<p>touch curso-docker.txt</p>
<p>ls curso-docker.txt</p>

<p><b>9) O run sempre cria um novo container então veja que:</b></p>

<p>docker container run --name mydeb -it debian bash</p>

<p><b>10) Para startar um container fazer o seguinte:</b></p>

<p>docker container start -ai mydeb</p>

<p><b>11) Para mapear as portas de um container:</b></p>

<p>docker container run -p 8080:80 nginx</p>

<p><b>12) Para rodar um servidor setando um diretório numa pasta do computador host basta fazer o seguinte:</b></p>

<p>docker container run -p 8080:80 -v $(pwd)/html:/usr/share/nginx/html nginx</p>

<p>Depois é só acessar o servidor local com localhost:8080 que vai estar lá o index.html.
    
<b>Observação:</b> É necessário colocar o diretório na pasta onde está situado o html, caso contrário não será possível visualizar a página que está sendo mandada para o servidor.
Para maiores informações basta olhar o html pelo localhost que possui outras dicas. Está localizado em ex-volume/html.
    </p>

