
# Descrição das atividades solicitadas.

Uma documetação sobre a sprint 7 e 8.


## Criar um repositorio no gitlab e uma pipeline que execute um "echo Hello World"

Para criar um repositório no GitLab, você precisa seguir os seguintes passos:

Faça login na sua conta do GitLab.
Clique no botão New project.
Escolha o tipo de projeto que deseja criar.
Preencha as informações do projeto, como nome, descrição e visibilidade.
Clique em Create project.
Para criar uma pipeline que execute um “echo Hello World”, você precisa seguir os seguintes passos:

Certifique-se de que você tem um corredor disponível para executar seus trabalhos. Se você estiver usando o GitLab.com, pode pular esta etapa. O GitLab.com fornece corredores compartilhados para você.
Crie um arquivo .gitlab-ci.yml na raiz do seu repositório. Este arquivo é onde você define os trabalhos CI/CD.
Quando você cometer o arquivo em seu repositório, o corredor executará seus trabalhos. Os resultados do trabalho são exibidos em um pipeline.
Aqui está um exemplo de arquivo .gitlab-ci.yml que executa um “echo Hello World”:

```bash
  stages:
  - build

build:
  stage: build
  script:
    - echo "Hello World"

```
Este arquivo define um trabalho chamado build que executa um comando echo "Hello World".

Por favor, note que este é um exemplo simples e que você pode personalizar o arquivo .gitlab-ci.yml para atender às suas necessidades específicas.

## Criar uma pipeline que faça o deploy do NGINX e que rode automaticamente após cada alteração.

Para criar uma pipeline que faça o deploy do NGINX e rode automaticamente após cada alteração, você pode seguir os seguintes passos:

Certifique-se de que você tem um corredor disponível para executar seus trabalhos. Se você estiver usando o GitLab.com, pode pular esta etapa. O GitLab.com fornece corredores compartilhados para você.
Crie um arquivo .gitlab-ci.yml na raiz do seu repositório. Este arquivo é onde você define os trabalhos CI/CD.
Quando você cometer o arquivo em seu repositório, o corredor executará seus trabalhos. Os resultados do trabalho são exibidos em um pipeline.
Aqui está um exemplo de arquivo .gitlab-ci.yml que faz o deploy do NGINX e roda automaticamente após cada alteração:

```bash
deploy:
  stage: deploy
  script:
    - apt-get update -qy
    - apt-get install systemd -y
    - apt-get install -y nginx
    - /etc/init.d/nginx start
    - nginx -v

```
Este arquivo define um trabalho chamado deploy que instala o NGINX e inicia o serviço. O trabalho é executado automaticamente quando você faz uma alteração no branch master.

Por favor, note que este é um exemplo simples e que você pode personalizar o arquivo .gitlab-ci.yml para atender às suas necessidades específicas.