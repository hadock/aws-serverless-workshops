## Serverless Web Application Workshop

En este workshop desplegarás una aplicación web simple que permite a los usuarios autenticar y agregar registros a una base de datos desde un formulario HTML con peticiones ajax a API Gateway.

La arquitectura de la aplicación usa [AWS Lambda][lambda], [Amazon API Gateway][api-gw], [Amazon S3][s3], [Amazon DynamoDB][dynamodb], [Amazon Cognito][cognito], and [AWS Amplify Console][amplify-console]. La consola de Amplify hospeda recursos web estáticos incluyendo HTML, CSS, JavaScript e imagenes, archivos que son cargados en el browser del usuario desde S3. El JavaScript ejecutado en el browser envía y recibe datos desde un backend público que consta de una API construida usando Lambda y API Gateway. Amazon Cognito provee las funciones de administración de usuarios y autenticación para asegurar el backend. Finalmente, DynamoDB provee la capa de persistencia de datos donde esta puede ser almacenada por la API's usando Lambda.

Ver el diagrama abajo para una representación completa de la architectura

![Mis textos](images/wildrydes-complete-architecture.png)

### Modules

This workshop is divided into four modules. Each module describes a scenario of
what we're going to build and step-by-step directions to help you implement the
architecture and verify your work.

| Module | Description |
| ---------------- | -------------------------------------------------------- |
| [Static Web hosting][static-web-hosting] | Deploy the static website using AWS Amplify Console by first creating a git repository (in either CodeCommit or GitHub) and then pushing the site code. |
| [User Management][user-management] | Configure user management for the website using Amazon Cognito. |
| [Serverless Backend][serverless-backend] | Create an AWS Lambda function that will persist data to an Amazon DynamoDB table. |
| [RESTful APIs][restful-apis] | Expose the Lambda function via an Amazon API Gateway as a RESTful API that the static site can call. |

:warning: These modules are intended to be executed linearly.

After you have completed the workshop you can delete all of the resources that were created by following the [cleanup guide][cleanup].

### Next

:white_check_mark: Review and follow the directions in the [setup guide][setup],
wherein you'll configure your AWS Cloud9 IDE and setup pre-requisites like an
AWS Account.

[wildrydes]: http://wildrydes.com/
[unicorns]: http://www.wildrydes.com/unicorns.html
[amplify-console]: https://aws.amazon.com/amplify/console/
[cognito]: https://aws.amazon.com/cognito/
[lambda]: https://aws.amazon.com/lambda/
[api-gw]: https://aws.amazon.com/api-gateway/
[s3]: https://aws.amazon.com/s3/
[dynamodb]: https://aws.amazon.com/dynamodb/
[setup]: 0_Setup/
[static-web-hosting]: 1_StaticWebHosting/
[user-management]: 2_UserManagement/
[serverless-backend]: 3_ServerlessBackend/
[restful-apis]: 4_RESTfulAPIs/
[cleanup]: 9_CleanUp/
