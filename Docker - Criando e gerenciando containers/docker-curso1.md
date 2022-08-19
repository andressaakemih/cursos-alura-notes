# Docker: Criando e gerenciando containers

Assunto: Docker
Criado: March 3, 2022 12:06 PM
Finalizado: No
Materiais: https://cursos.alura.com.br/course/docker-criando-gerenciando-containers
Plataforma: Alura

## I - Conhecendo o Docker

### Atividades:

I - Se precisarmos lidar com conflito de portas ou controle de versionamento em uma das
aplicações que estivermos desenvolvendo, de que forma poderemos resolver estes problemas?

- Podemos utilizar máquinas virtuais a fim de garantir o isolamento entre as aplicações.
→ Máquinas virtuais são capazes de isolar sistemas, com isso,
o controle sobre a aplicação fica mais fácil.
- Podemos utilizar containers com o objetivo de isolar as aplicações.
    
    → Containers podem isolar diversas aplicações, facilitando o controle acerca de portas e versões.
    

II - Recentemente aprendemos como os containers agem para garantir isolamento entre eles e o host, a fim de manter os comportamentos independentes entre cada um dos sistemas e aplicações. Por qual meio os containers conseguem atingir tal objetivo?

- Através de namespaces.
    
    →  Com a utilização de namespaces, os containers conseguem garantir isolamento em diversas camadas.
    

### Instalação Linux:

→ Mensagem de permissão negada para executar comando: `docker run ID_CONTAINER`

```bash
\\ sudo usermod -aG docker $USER
```

→ Reiniciar após dar permissão

### Notas:

Nessa aula aprendemos:

- Máquinas virtuais possuem camadas adicionais de virtualização em relação a um container;
- Containers funcionam como processos no host;
- Containers atingem isolamento através de namespaces;
- Os recursos dos containers são gerenciados através de cgroups.

## II - Os primeiros comandos

### Atividades:

I - Já  aprendemos que ao utilizar o Docker precisamos conhecer e saber para que servem alguns comandos para fazer ações quando trabalhamos com containers, sendo um deles o `docker run`.

Escolha a alternativa que mostra como a definição do comportamento do Docker ao executarmos o comando.

- O comando `docker run` é responsável por executar um container em nosso host.
    
    → Através deste comando, o docker irá executar o container da maneira esperada.
    

II - Quando queremos executar um container e usamos o comando  `docker run`, ocorre uma série de etapas ordenadas até que a execução seja feita efetivamente.

Selecione a alternativa que melhor descreve este fluxo.

- Procura a imagem localmente -> Baixa a imagem caso não encontre localmente -> Valida o hash da imagem -> Executa o container.
    
    → Este é o fluxo adotado pelo docker para execução de um container.
    

### Comandos:

```bash
\\ docker ps

\\ docker stop ID_CONTAINER

\\ docker ps -a

\\ docker start ID_CONTAINER

\\ docker exec -it ID_CONTAINER bash

\\ docker pause ID_CONTAINER

\\ docker unpause ID_CONTAINER

\\ docker rm ID_CONTAINER

\\ docker run -it ubuntu bash
```

### **Atividades:** **Run vs Exec**

III - Recentemente, vimos sobre o comando `docker run` e `docker exec`.  Sabemos que ambos os comandos envolvem o fluxo de inicialização e execução de comandos em containers, porém em contextos diferentes.

Selecione a alternativa com a diferença do funcionamento entre esses comandos.

- O `docker run`  cria um novo container e o executa. O `docker exec`  permite executar um comando em um container que já está em execução.
    
    → Esta é a grande diferença entre ambos.
    

```bash
\\ docker port ID_CONTAINER

\\ docker rm ID_CONTAINER --force

\\ docker run -d -p 8080:80 dockersamples/static-site
```

IV -  As flags `-p` e `-P`  são úteis quando queremos fazer o mapeamento de portas entre nosso 
container e o nosso host. Existe um comando responsável pela visualização de como o mapeamento de portas de um container está sendo feito.

Selecione a alternativa que corresponde a este comando.

- `docker port`
    
    → Este comando é responsável por exibir como o mapeamento de portas de um container está sendo feito.
    

### Notas:

Nessa aula aprendemos:

- O Docker Hub é um grande repositório de imagens que podemos utilizar;
- A base dos containers são as imagens;
- Como utilizar comandos acerca do ciclo de vida dos containers, como: `docker start`, para iniciar um container que esteja parado; docker `stop`, para parar um que esteja rodando; `docker pause`, para pausar um container e `docker unpause` para iniciar um container pausado;
-Conseguimos mapear portas de um container com as flags `p` e `P`.

## III - Criando e compreendendo imagens

Uma imagem nada mais é do que um conjunto de camadas, que na imagem estamos representando pelas cores vermelha, azul, rosa claro e cinza. É um conjunto de camadas, e quando juntamos essas camadas nós formamos imagens.

E essas camadas em si são independentes, cada uma tem seu respectivo ID, por exemplo, cada uma tem o seu respectivo identificador.

**Por que os containers são tão “leves”?** Pode ser que, por exemplo, no nosso host nós já tenhamos algumas das camadas que queremos, então no momento em que fizermos um `pull` ou um `run` que vai fazer um `pull` consequentemente, nós vamos fazer download só das camadas que precisamos.

*Então o Docker é inteligente suficiente para reutilizar essas camadas para compor novas imagens.*

Conseguimos ter uma performance muito boa já que não precisamos ter informação duplicada ou triplicada.

Quando temos nossa imagem, ela é ready only. Isso significa que não conseguimos modificar as camadas dessas imagem depois que ela foi criada.

No momento em que temos essa imagem “*dockersamples/static-site*” ela é imutável, assim como, por exemplo, a imagem que temos do nosso Ubuntu. 

Como conseguimos escrever dentro do container se a imagem que gera o nosso container é apenas para leitura? Se ele é bloqueada para escrita como é que o container consegue escrever informação dentro dela?

Porque no fim das contas, quando criamos o container, nada mais é do que uma imagem com uma camada adicional de read-write, de leitura e escrita.

Quando criamos um container, trata-se de uma camada temporária em cima da imagem, onde conseguimos escrever informações. Sendo assim, no momento que deletamos o container, essa camada extra também é deletada.

### Comandos:

```bash
\\ docker images

\\ docker run -it ubuntu bash (modo interativo com o terminal da imagem/container)

\\ docker inspect ID_CONTAINER

\\ docker history ID_CONTAINER
```

### Atividades:

I - Anteriormente vimos como as imagens se diferem de containers e como são compostas. Sabemos até então que imagens são “receitas” para gerar containers, porém, ainda precisamos fixar como imagens são construídas e gerenciadas pelo Docker.

Selecione as alternativas verdadeiras sobre a utilização de imagens.

- Imagens são compostas por uma ou mais camadas.
    
    → As camadas são a menor unidade que compõem uma imagem.
    
- Podemos visualizar as camadas de uma imagem através do comando `docker history`.
    
    → Este comando é responsável por exibir quais são as camadas de uma imagem.