## Como enviar email com Python
Bibliotecas utilizadas: <b>smtplib</b> e **email**

## Procedimentos
- Configurar o servidor SMTP e fazer o login;
- Criar o objeto MimeMultipart carregar os valores corretos de headers;
- Adicionar a mensagem;
- Envio da mensagem usando o servidor;

--------------------------------------------------

## Configurando Servidor
É feito a configuração do servidor (para envio de e-mails), configuração dos dados de login, realizado a importação e configuração dos objetos necessários.

      import smtplib
      from email.mime.multipart import MIMEMultipart
      from email.mime.text import MIMEText
      host = '<HOST_URL'>
      port = 587
      user = '<USUARIO>'
      password = '<SENHA>'
      server = smtplib.SMTP(host, port)
      
**Configuração do servidor**: A configuração do servidor vai depender do servidor de e-mail que estiver utilizando. Dependendo de qual servidor estiver utilizando, a confogiração será diferente.
 
- *NOTA: Não é interessante deixar os dados de login e senhas salvas direto do código fonte. Se possível, deixar salvo em um arquivo ou banco de dados por exemplo. Assim evita-se que compartilhe informações confidenciais acidentalmente.*
    
Feito a criação do objeto e os dados de login, é preciso estabelecer uma conexão. No caso do servidor, será feito uma conexão TSL, portanto é preciso indicar na biblioteca.

      server.ehlo()
      server.starttls()
      server.login(user, password)
    
--------------------------------------------------


    


## Referências
Como enviar email com python. Souza, Fernando.                                                                                                                            
Disponível em: <https://medium.com/vacatronics/como-enviar-email-com-python-e43a9af7f672>. Acessado 21/07/2021 às 08:42.


