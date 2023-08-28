# Leitor de Notícias via Email

O código utiliza a biblioteca `imaplib` para acessar uma caixa de entrada de email e ler os emails não lidos, convertendo o conteúdo do email em fala através da biblioteca `pyttsx3`.

## Funcionalidade

O código busca por emails não lidos em uma caixa de entrada de email específica, extrai o conteúdo dos emails, converte o conteúdo em texto e utiliza a biblioteca `pyttsx3` para transformar o texto em fala.

## Requisitos

- Python (versão compatível)
- Conta de email Gmail
- Acesso IMAP habilitado
- Senha de aplicativo gerada para o Gmail

## Uso

1. Ative o acesso IMAP na sua conta Gmail.
2. Crie uma senha de aplicativo para a sua conta Gmail (Conta Google > Segurança > Autenticação de 2 fatores > Criar senha de APP).
3. Insira seu email e a senha de aplicativo gerada no arquivo `credentials.py`.

## Como funciona

1. O código se conecta ao servidor IMAP do Gmail usando as credenciais fornecidas.
2. Ele seleciona a TAG "Deschamps".
3. Busca por emails não lidos na caixa de entrada.
4. Para cada email não lido:
   - Extrai o conteúdo do email.
   - Utiliza a biblioteca `BeautifulSoup` para parsear o HTML do email e extrair o texto relevante.
   - Decodifica o conteúdo codificado no formato quoted-printable.
   - Inicializa a biblioteca `pyttsx3` para transformar o texto em fala.
   - Executa a fala do texto.

## Observações

- O código está configurado para ler a caixa de entrada com a TAG "Deschamps". Você pode modificar o nome da TAG de acordo com suas necessidades.
- A biblioteca `pyttsx3` pode depender de dependências específicas do sistema para funcionar corretamente, como drivers de voz. Verifique a documentação do `pyttsx3` para obter mais informações sobre a configuração.

## Autoria e Créditos

- O código foi criado com base no vídeo do canal @Refatorando: [link do vídeo](https://youtu.be/wm82gDsKN0E).
- Créditos ao canal @FilipeDeschamps por compartilhar a ideia da aplicação.

## Contato

Caso você tenha alguma dúvida ou precise de assistência relacionada a este código, você pode entrar em contato com o autor original do código ou referir-se ao canal de origem mencionado.

