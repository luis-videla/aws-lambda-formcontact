# aws-lambda-formcontact
Ejemplo de serverless framework en AWS para formulario de contacto

# Instalación requerida

- NodeJS
- Cuenta gratuita en AWS
- Configuración SES

# Instalación, configuración serverless y credenciales de AWS

```
npm i -g serverless
serverless config credentials --provider aws --key xxxxxxxxxxxxxx --secret xxxxxxxxxxxxxx
cat ~/.aws/credentials
```

# Crear proyecto serverless en AWS

```
serverless create --template aws-nodejs --path contact-form-api
```

# Desplegar desarrollo en la nube

```
serverless deploy
```

# Probar servicio serverless

```
curl --header "Content-Type: application/json" \
  --request POST \
  --data '{"email":"luis.videla@globant.com","name":"Luis Videla","content":"Hola!"}' https://d9s4pxo5jl.execute-api.us-east-1.amazonaws.com/dev/email/send
```
