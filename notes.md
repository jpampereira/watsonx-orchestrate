# Anotações - Watson X Orchestrate

## 1. Como criar uma instância do Orchestrate na IBM Cloud?

O primeiro passo para criar a sua instância do WatsonX Orchestrate é criar uma conta na IBM Cloud. Após o acesso, o usuário será encaminha para a página inicial da plataforma, conhecida como Dashboard. Nessa página, clicar no botão destacado em vermelho **Criar recurso**.

![Como criar uma instância no WoX - Parte 1](./images//how-to-create-an-instance-1.png)

Nesse momento você será deslocado para o catálogo de produtos oferecidos dentro da plataforma. Na barra de pesquisa, basta digitar *"orchestrate"* e nas opções que aparecem logo abaixo, clique naquela que diz respeito ao WatsonX Orchestrate (destacado em vermelho).

![Como criar uma instância no WoX - Parte 2](./images//how-to-create-an-instance-2.png)

Você será redirecionado para uma página onde deve definir algumas configurações da instância, como a região em que ela será alocada, bem como o nome da instância, grupo de recursos e tags. Por fim, irá clicar no botão **Criar** para iniciar o processo de criação da instância.

- A IBM Cloud oferece um trial de 30 dias do produto.

![Como criar uma instância no WoX - Parte 3](./images//how-to-create-an-instance-3.png)

Após clicar no botão para criar a instância, logo você é encaminhado para dentro dela na página inicial do Orchestrate. Porém, vou mostrar como chegar nessa mesma página a partir da página inicial da plataforma. A partir da página Dashboard, apresentada na primeira imagem, clicar no menu de hambúrguer no campo superior esquerdo e selecionar a opção **Lista de Recursos**. A página de destino traz todos os recursos da IBM Cloud que você possui instanciados na conta do qual você faz parte. O WatsonX Orchestrate está dentro da seção **AI/Aprendizado de máquina**.

![Como criar uma instância no WoX - Parte 4](./images//how-to-create-an-instance-4.png)

Nessa próxima página, clicar em **Launch watsonx Orchestrate**.

![Como criar uma instância no WoX - Parte 5](./images//how-to-create-an-instance-5.png)

Por fim, agora estamos na página inicial da instância que criamos do Watson Orchestrate.

![Como criar uma instância no WoX - Parte 6](./images//how-to-create-an-instance-6.png)

## 2. Como criar seu primeiro agente pela interface gráfica (No code)?

Nesse primeiro exemplo vamos criar o Agent a partir da interface gráfica. Na página inicial da sua instância do Orchestrate, selecionar o menu hambúrguer no campo superior esquerdo e dentro do submenu **Build**, selecionar a opção **Agent Builder**.

![Como criar um Agent no WoX - Parte 1](./images//how-to-create-an-agent-gui-1.png)

Você será redirecionado para uma página onde é possível visualizar todos os seus agentes (*agents*) e ferramentas (*tools*) criados, além de métricas como quantidade de mensagens trocadas pelos agentes, falhas identificadas e latência na comunicação. Para criar um novo agente, basta clicar em **Create agent**.

![Como criar um Agent no WoX - Parte 2](./images//how-to-create-an-agent-gui-2.png)

O primeiro passo é definir se você deseja criar o agente do zero (*from scratch*) ou se quer reaproveitar algum outro template já existente. Em seguida é preciso definir um nome para o agente e por último uma descrição. Clicar em **Create** para ir para a próxima etapa.

- A descrição não ira determinar o comportamento (*behavior*) do seu agente. Ele serve para delimitar o escopo do agente e ajudar outros agentes a entender para que ele serve para no caso de necessidade, fazer a melhor escolha por qual a gente chamar para uma determinada tarefa.

- A descrição deve conter o propósito do agente, e as ferramentas e outros agentes que ele se comunica.

![Como criar um Agent no WoX - Parte 3](./images//how-to-create-an-agent-gui-3.png)

Já na página onde iremos definir as principais configurações do a gente, no primeiro quadrado podemos definir qual modelo de IA o nosso a gente irá utilizar. Via interface gráfica as opções são mais limitadas, mas no caso do a gente ser configurado em Pro Code, há mais opções de modelos disponíveis. Em **Welcome Message**, a mensagem definida irá substituir *"Hello, welcome to watsonx Orchestrate"*.

![Como criar um Agent no WoX - Parte 4](./images//how-to-create-an-agent-gui-4.png)

Podemos definir em **Quick start prompts** alguns exemplos de prompts para mostrar para o usuário algumas opções do que ele pode solicitar para o agente.

![Como criar um Agent no WoX - Parte 5](./images//how-to-create-an-agent-gui-5.png)

Em **Knowledge**, é onde definimos a base de conhecimento do nosso agente, fornecendo os arquivos que ele terá acesso para consulta. Para adicionar uma nova base clicamos em **Choose knowledge**. Em **Edit knowledge settings**, podemos alterar alguns parâmetros referentes as bases.

![Como criar um Agent no WoX - Parte 6](./images//how-to-create-an-agent-gui-6.png)

Devemos escolher que tipo de base de conhecimento desejamos importar. Podemos inserir um arquivo diretamente nessa interface ou apontar para repositórios externos, como um storage.

![Como criar um Agent no WoX - Parte 7](./images//how-to-create-an-agent-gui-7.png)

No nosso exemplo escolhemos a opção **Upload files**, onde anexamos os arquivos diretamente pela interface do Orchestrate.

![Como criar um Agent no WoX - Parte 8](./images//how-to-create-an-agent-gui-8.png)

Após adicionar o arquivo, devemos colocar uma descrição para que o agente saiba para que serve aquele documento. Para submeter essa base de conhecimento, basta clicar em **Save**.

![Como criar um Agent no WoX - Parte 9](./images//how-to-create-an-agent-gui-9.png)

Em **Toolset** definimos as ferramentas que o nosso a gente terá acesso, como por exemplo, uma API ou serviço que ele irá consumir dados. Para criar uma nova ferramenta clicamos em **Add tool**.

![Como criar um Agent no WoX - Parte 10](./images//how-to-create-an-agent-gui-10.png)

Temos várias opções de ferramentas:

1. Podemos adicionar uma ferramenta diretamente do catálogo. A plataforma oferece integração com diversas ferramentas de mercado, como por exemplo, o Service Now em poucos passos, sem a necessidade de se configurar tudo manualmente;

2. Para o caso de adicionar ferramentas da instância local, essa está disponível apenas na versão *On Premises* do Orchestrate e permite adicionar programas que são executados no mesmo ambiente;

3. A opção de adicionar por arquivo ou MCP server permite integrar uma API a partir do seu swagger;

4. Por último, na opção *Agentic Worflow*, é possível construir um fluxo diretamente pela interface do Orchestrate utilizando caixas com drag-and-drop codificáveis e que se integram com outras *Tools* e *Agents*.

![Como criar um Agent no WoX - Parte 11](./images//how-to-create-an-agent-gui-11.png)

No nosso caso, optamos pela criação da ferramenta a partir de um arquivo.

![Como criar um Agent no WoX - Parte 12](./images//how-to-create-an-agent-gui-12.png)

Para isso importamos o YAML do Swagger da nossa API e automaticamente o Orchestrate já identificou todos os endpoints que existem dentro dele. Podemos selecionar apenas aqueles que desejamos que sejam inseridos no nosso agente.

![Como criar um Agent no WoX - Parte 13](./images//how-to-create-an-agent-gui-13.png)

Cada endpoint será considerado uma ferramenta, e todos eles estarão disponíveis para serem consumidos por outros agentes. É importante que os endpoints estejam bem descritos na documentação para que o agente tenha ciência do que cada um deles faz.

![Como criar um Agent no WoX - Parte 14](./images//how-to-create-an-agent-gui-14.png)

![Como criar um Agent no WoX - Parte 15](./images//how-to-create-an-agent-gui-15.png)

Além das ferramentas, podemos definir também outros agentes que o nosso pode se comunicar. Nesse exemplo vamos seguir apenas com um único agente, porém, esse caso será de extrema importância quando estivermos falando sobre arquiteturas de multiagentes.

![Como criar um Agent no WoX - Parte 16](./images//how-to-create-an-agent-gui-16.png)

Na seção de **Behavior** (comportamento), é onde vamos inserir o prompt que descreve como nosso agente deve funcionar, indicando o seu contexto, orientando as situações em que ele deve utilizar cada uma das bases de conhecimentos, ferramentas e agentes configurados, definindo como ele deve se comportar em determinadas situações e se necessário, definindo os limites de atuação (*guard-rails*). Esses comportamentos também podem ser configurados na seção de **Guidelines**.

![Como criar um Agent no WoX - Parte 17](./images//how-to-create-an-agent-gui-17.png)

Por último, definimos por qual canal aquele agente ira se comunicar (Teams, Facebook, API etc.).

![Como criar um Agent no WoX - Parte 18](./images//how-to-create-an-agent-gui-18.png)

Para publicar o seu agente você deve clicar em **Deploy**. Nesse momento um modal trazendo a revisão dos conteúdos inseridos. Caso esteja tudo ok, clique novamente em **Deploy**.

![Como criar um Agent no WoX - Parte 19](./images//how-to-create-an-agent-gui-19.png)

Seremos redirecionados novamente para a página do Orchestrate que contém todos os nossos agentes e ferramentas criados. Podemos perceber que o agente que acabamos de criar já aparece e contém uma tag de `Live`, o que indica que ele já está rodando.

![Como criar um Agent no WoX - Parte 20](./images//how-to-create-an-agent-gui-20.png)

Seja durante a fase de configuração ou após a publicação, podemos testar o nosso agente enviando prompts e verificando se ele está atuando da forma esperada.

Para validar se ele está atuando corretamente, podemos expandir a seção de *reasoning* (raciocínio) para entender de qual base de conhecimento, ferramenta ou agente ele retirou aquela resposta.

![Como criar um Agent no WoX - Parte 21](./images//how-to-create-an-agent-gui-21.png)
![Como criar um Agent no WoX - Parte 22](./images//how-to-create-an-agent-gui-22.png)
![Como criar um Agent no WoX - Parte 23](./images//how-to-create-an-agent-gui-23.png)
![Como criar um Agent no WoX - Parte 24](./images//how-to-create-an-agent-gui-24.png)

### 2.1. Criando uma Solução Multiagente

Em um próximo exercício, a ideia era construir um agente que auxiliasse nas tarefas de um banco, o GFM Bank. Esse banco contava com funcionários de diferentes áreas que desempenhavam diversas operações: O pessoal do caixa trabalhava com consulta de saldo e transferências. Quando era necessário mexer com cheque especial (solicitar ou desabilitar) ou pedir a reversão de uma transferência, o pessoal do caixa deveria encaminhar para o time de Backoffice. Quando haviam dúvidas sobre os produtos oferecidos pelo banco, era necessário encaminhar para os especialistas de produto. Essas operações demoravam horas e exigiam do cliente entrar em contato com diversas pessoas. A ideia nesse exercício então foi implementar uma solução onde cada uma dessas áreas era de responsabilidades de um agente e todos eles eram coordenados por um agente orquestrador.

![Arquitetura Multiagente para o Banco GMF](./images/banking-backoffice-exercise-architecture.png)

Na página onde podemos visualizar todos os agentes e ferramentas que a nossa instância possui, podemos ver a presença de quatro agentes destacados em cores diferentes. Os destacados em laranja são os agentes especializados, isto é, são aqueles que serão invocados pelo agente orquestrador quando este identificar que a tarefa solicitada pelo usuário pode ser resolvida por um determinado agente especialista. O destacado em vermelho é o agente orquestrador, que é aquele que irá interagir diretamente com o usuário e receber as solicitações.

![Solução de Multiagente para o Banco GMF - Parte 1](./images/banking-backoffice-exercise-1.png)

Para que os agentes especialistas não fiquem disponíveis para o usuário via interface do WatsonX Orchestrate, na sua configuração devemos desabilitar a opção **Home Page** em **Channels**.

![Solução de Multiagente para o Banco GMF - Parte 2](./images/banking-backoffice-exercise-2.png)

Na seção **Agents**, devemos configurar todos os agentes que o nosso orquestrador pode se comunicar. Mesmo que existam mais agentes dentro da nossa instância do Orchestrate, o nosso agente só visualizará àqueles que foram configurados nessa etapa.

- Vemos que apenas dois agentes foram configurados. Isso porque se olharmos para o desenho da arquitetura da solução, vimos que o orquestrador não se comunica diretamente com o agente de Backoffice, sendo isso responsabilidade do agente de caixa.

![Solução de Multiagente para o Banco GMF - Parte 3](./images/banking-backoffice-exercise-3.png)

Quando clicamos em **Add agent** temos a opção de adicionar um agente do catálogo (por exemplo, uma integração com o Service Now sem a necessidade de você construir essa comunicação na mão), um agente da sua instância (que é o nosso caso), ou agentes externos.

![Solução de Multiagente para o Banco GMF - Parte 4](./images/banking-backoffice-exercise-4.png)

Se voltarmos na página inicial do Orchestrate onde podemos interagir via chat com os nosso assistentes, vamos ver que apenas o agente orquestrador estará disponível para conversa, como já era esperado.

![Solução de Multiagente para o Banco GMF - Parte 5](./images/banking-backoffice-exercise-5.png)

## 3. Como criar seu primeiro agente via ADK (Pro code)?

O IBM watsonx Orchestrate Agent Development Kit (ADK) é um conjunto de ferramentas (biblioteca Python e comandos na CLI) que permitem a construção e o deploy de *agents* e *tools* para o IBM watsonx Orchestrate de forma programática.

### 3.1. Instalando o ADK

Para facilitar a experiência, foi criado uma imagem Docker que automatiza a criação do ambiente do ADK.

Primeiramente vamos entender o que a [imagem](./adk/Dockerfile) configura no ambiente:

- Como explicado na definição do ADK, ele é formado por um conjunto de ferramentas, incluindo uma biblioteca Python. Sendo assim, a imagem base utilizada é a do Python na versão 3.13. Atualmente, o ADK está disponível a partir da versão 3.11;

- Em seguida é criado e definido `wxo-adk` como o diretório de trabalho, onde serão depositados nossos projetos que forem desenvolvidos;

- Em seguidas são executados três comandos sequencialmente: o primeiro instala a biblioteca do Orchestrate utilizando o gerenciador de pacotes `pip` do Python. O segundo comando cria um ambiente de desenvolvimento local também com o nome `wxo-adk` e esse ambiente é relacionado a nossa instância do Orchestrate na IBM Cloud. Será mostrado como obter o endereço da nossa instância pela Cloud e como passar esse valor como argumento no `build` da imagem. Por último, é feito um comando para ativar o ambiente e passar a API Key de autenticação. Assim como o endereço da instância, a API Key é obtida pela Cloud e passada como argumento no `build` da imagem.

- Comando para fazer o `build` da imagem Docker (é preciso estar dentro do diretório `adk`):

  ```Docker
  docker build --build-arg WXO_INSTANCE=<URL_INSTANCIA> --build-arg WXO_API_KEY=<API_KEY_CLOUD> -t wxo-adk .
  ```

  - Para obter a URL da instância:

    ![Obter URL da Instância do WxO](./images/obtain-instance-url.png)

  - Para obter a API Key, será necessário acessar a página de IAM da sua conta IBM Cloud e gerar uma nova chave de API:

    ![Obter API Key da Conta](./images/obtain-account-api-key-1.png)

    ![Obter API Key da Conta](./images/obtain-account-api-key-2.png)

Após a geração da imagem, agora devemos subir o container do nosso ambiente do ADK utilizando o [compose](./adk/docker-compose.yaml). Para isso também é preciso estar dentro do diretório `adk`:

```Docker
docker-compose up -d
```

Após a criação do ambiente, para acessá-lo, executamos:

```Docker
docker container exec -it wxo-adk sh
```

Para validarmos que estamos dentro do ambiente do ADK, executamos:

```ADK
orchestrate env list
```

- E obtemos o seguinte resultado que evidencia que de fato estamos no ambiente do ADK:

  ![Listar ambientes do ADK](./images/adk-environment-list.png)

## 4. Links

- [Documentação WatsonX Orchestrate](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base)

- [Documentação WatsonX Orchestrate ADK](https://developer.watson-orchestrate.ibm.com/)

- [Repositório GitHub do Bootcamp](https://github.com/bootcampwxo/bootcampwxo/tree/main)

- [From Zero to Hero](https://ruslanmv.com/blog/hello-watsonx-orchestrate)
