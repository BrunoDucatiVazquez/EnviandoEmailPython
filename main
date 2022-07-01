import smtplib
import email.message

def enviar_email():  
    corpo_email = """
    <p style="font-weight: bold;">Template de formulario</p>
    <input type="submit" value></input>
    """

    msg = email.message.Message()
    msg['Subject'] = "Olá caro, eu estou testando o meu formulario"
    msg['From'] = 'brunoducati1001@gmail.com'
    msg['To'] = 'brunoducati1001@gmail.com'
    password = 'xxxxx' 
    msg.add_header('Content-Type', 'text/html')
    msg.set_payload(corpo_email )

    s = smtplib.SMTP('smtp.gmail.com: 587')
    s.starttls()
    # Login Credentials for sending the mail
    s.login(msg['From'], password)
    s.sendmail(msg['From'], [msg['To']], msg.as_string().encode('utf-8'))
    print('Email enviado')

enviar_email()
