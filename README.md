# IntuitiveCare-ProcessoSeletivo

As aplicações e serviços desenvolvidos utilizando python possuem arquivo um arquivo de requiremento em suas respectivas pastas.

# Teste 1 
Ao final do script os anexos que foram baixados usando web scraping são compactos em um arquivo com o nome "Anexos.zip"

# Teste 2 
O script desse teste precisa que o arquivo de nome "Anexo_I_Rol_2021RN_465.2021_RN473_RN478_RN480_RN513_RN536_RN537_RN538_RN539_RN541_RN542_RN544_546_571_577.pdf" esteja presente no diretório atual.
Ao final da execução do script, um arquivo zip com o nome "Teste_(tales_oliveira_neves).zip" é gerado contendo a tabela extraída do arquivo pdf.
# Teste 4

 A infraestrutura da aplicação do teste 4 foi montadada seguinte maneira:
  Back-end: Servidor MySQL (Criado utilizando um servidor RDS da AWS)
  API Server: Servidor Flask-SQLAlchemy (Sendo executado em uma instância EC2 da AWS)
  Front-end: Aplicação em Vue.js (Também sendo executao em uma instância EC2 da AWS)
 
 O banco de dados back-end é composto de apenas uma tabela que possui as 19 colunas do anexo de relatório.
 A API possui duas rotas:
   http://endpoint/all
   http://endpoint/like/<lookforterm>
  
  A rota /all é utilizada para realizar um query de todas as entradas do presentes no banco de dados.
  A rota /like/<lookforterm> é uma query que busca todas as entradas que possuem a string de "lookforterm" no seu campo de razão social.
  
 O front-end apenas um cabeçalho para navegação e 
 
 # Detalhes e poréns
 A importação dos dados do anexo de relatório foi feita utilizando MySQL Worbench e exigiu que os acentos fossem removidos utilizando o script "fixencoding.py".
 A automatização dos serviços juntamente com um sistema CI/CD ainda não foram implementados.
