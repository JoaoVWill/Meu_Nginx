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

  *Anotação: [^2]*

  - Editar seu arquivo [Arquivo em .txt](https://github.com/jvwill/Meu_Nginx/blob/main/Arquivo-Site_Novo.txt)
  <div align="left">
    <img align="center" alt="configs_utilizadas" src="https://cdn.discordapp.com/attachments/759062113808809994/957274048621064282/unknown.png">
  </div>
  
  ___LEGENDA:___
    - server: começo da configuração a ser lida
      - listen: porta ser ouvida (no caso 81)
      - server_name: como será o nome do server
      - location: será onde procurar o arquivo quando houver requisição 
        - root: será a raiz dos arquivos, a partir da onde os arquivos começam a ser procurados
        - index: será o nome a procurar do nosso arquivo **Index**

  5. Copiar arquivo para o diretório `sites-enabled`
```ruby
  cp /etc/nginx/sites-available/[NOME_DO_ARQUIVO] /etc/nginx/sites-enabled
```
  <div align="left">
    <img align="center" alt="copia_para_sites-enabled" src="https://cdn.discordapp.com/attachments/759062113808809994/957352222935613560/unknown.png">
  </div>

  6. Criar arquivo ___Index___ para o site novo
```ruby
  vim /var/www/html/[NOVO_ARQ_INDEX]
```
  <div align="left">
    <img align="center" alt="comando_novo_arquivo" src="https://cdn.discordapp.com/attachments/759062113808809994/957355336782712902/unknown.png">
    <img align="center" alt="arquivo_vim_novo" src="https://cdn.discordapp.com/attachments/759062113808809994/957369463303462962/unknown.png">
  </div>

  7. Reiniciar Nginx e conferir status
```ruby
  systemctl restart nginx
```
  <div align="left">
    <img align="center" alt="restart_nginx" src="https://cdn.discordapp.com/attachments/759062113808809994/957370267850645504/unknown.png">
  </div>

```ruby
  systemctl status nginx
```
  <div align="left">
    <img align="center" alt="status_nginx" src="https://cdn.discordapp.com/attachments/759062113808809994/957370500244467772/unknown.png">
  </div>

  8. Por fim, teste a sua config e veja os sites com seu novo __INDEX__
  - Porta 80
  <div align="left">
    <img align="center" alt="Index_porta-80" src="https://cdn.discordapp.com/attachments/759062113808809994/957371689572905071/unknown.png">
  </div>
   
  - Porta 81
  <div align="left">
    <img align="center" alt="Index_porta-81" src="https://cdn.discordapp.com/attachments/759062113808809994/957371768656506920/unknown.png">
  </div>

##

### EXTRAS
___Config de Página de ERRO___
  
##

### RESULTADO FINAL(APÓS ÚLTIMAS ALTERAÇÕES)

- Porta 80
  <div align="left">
    <img align="center" alt="Index_porta-80" src="">
  </div>
   
- Porta 81
  <div align="left">
    <img align="center" alt="Index_porta-81" src="">
  </div>

- Página de Erro
  <div align="left">
    <img align="center" alt="Index_pag_de_erro" src="">
  </div>







[^1]:`*.*.*.*` = Ip da sua máquina
[^2]: `site_novo` = Nome do meu arquivo, pode ser alterado
