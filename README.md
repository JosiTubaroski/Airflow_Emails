# Airflow com Emails

### Enviar Email

- Notificação Automáticas de Sistema (error, retry)

- Notificação por task: erro, fim da execução etc. Configuradas na task

### Notificação de Sistema

- Automático, definição na Dag:
   - email_on_failure=True (Envia email em caso de falha)
   - email_on_retry=False 
   - retries=1: Isso define o número de vezes que uma tarefa será reprocessada antes de falhar definitivamente.
   - retry_delay=timedelta(minutes=5):
     Isso define o intervalo de tempo entre os reprocessamentos.

### Operador

- EmailOperator
   - Envia um email dentro do fluxo do airflow, como uma task

### O que é preciso

- Servidor SMTP (Serviço de envio de e-mail)
- Configurar o Airflow


# SMTP

- Você pode usar qualquer SMTP
- Vamos utilizar como exemplo o Gmail


### Configurando o gmail

- Ir em configurações de conta no gmail, security, habilitar a opção "2-Step Verification"

  exkz djff sskc gzzu

### Configurando o Airflow para envio de e-mails

- Incluir no arquivo docker-compose.yaml as configurações para envio de e-mail.
- As informações que devem ser adicionadas estão no arquivo config email
- Após realizar a inclusão das informações, é necessário reiniciar o docker compose

# Criando dag que envia e-mail


