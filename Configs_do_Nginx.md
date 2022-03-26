# __Projeto de__ <img align="center" alt="Jv-Nginx" height="90" width="90" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nginx/nginx-original.svg"> 
 ### Aqui as etapas para meu projeto e desafio do Nginx na Certsys


  1. Instalação do Nginx
```ruby
apt install nginx
```
  2. Testar site default do Nginx
      - Abrir navegador (Edge será a melhor alternativa)
      - Na guia de pesquisa: `http://*.*.*.*`[^1].
      - Exemplo: 
       <img align="center" alt="Exemplo_de_site" src="https://cdn.discordapp.com/attachments/764827072652247090/956562460951842936/MicrosoftTeams-image_1.png">
   
  3. Alteração do Texto do site Default (porta 80)
```ruby
vim /var/www/html/index.nginx-debian.html
```
  <div align="left">
  <img align="center" alt="Arquivo_Index" height="450" width="300" src="https://cdn.discordapp.com/attachments/764827072652247090/956568917717946378/unknown.png">
  <img align="center" alt="Exemplo_de_site" height="350" width="600" src="https://cdn.discordapp.com/attachments/764827072652247090/956569263114715186/unknown.png">
  </div>
  
  *Anotação: Não usar acentos por que pode dar erro (nesse projeto pelo menos)*
  
  4. Criação do arquivo do novo site
```ruby
cd /etc/nginx/sites-available
```
  <div align="left">
  <img align="center" alt="Caminho_sites-available" src="https://cdn.discordapp.com/attachments/759062113808809994/957266219923300382/unknown.png">
  </div>
  
  - Criar arquivo texto de configuração do site
  ```ruby
  vim [NOME_DO_ARQUIVO]
  ```

<div align="left">
  <img align="center" alt="arquivo_de_conf" src="https://cdn.discordapp.com/attachments/759062113808809994/957269119487574076/unknown.png">
  </div>

*`site_novo` pode ser alterado por um de sua escolha*

  - Editar seu arquivo
<div align="left">
  <img align="center" alt="arquivo_de_conf" src="https://cdn.discordapp.com/attachments/759062113808809994/957274048621064282/unknown.png">
  </div>





















[^1]:`*.*.*.*` = Ip da sua máquina
