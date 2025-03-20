<h1 align="center">Danilo Verginio da Silva</h1>

### Introdução
<div align="justify">
Meu nome é Danilo Vergínio da Silva e sou tecnólogo em Banco de Dados pela FATEC São José dos Campos. Durante minha formação, adquiri sólidos conhecimentos em bancos de dados relacionais e NoSQL, além de experiência em desenvolvimento de software utilizando linguagens como Python, Java, javaScript e SQL.
Ao longo dessa jornada, desenvolvi habilidades técnicas e interpessoais, como liderança de equipes em projetos de desenvolvimento, capacidade de trabalhar em ambientes colaborativos e a prática de boas práticas de programação, através de Projetos Integrados (API).
</div>

<div align="center">
  <a href="https://github.com/Daniloel">
    <img loading="lazy" src="https://avatars.githubusercontent.com/u/88066389?v=4" width="250" height="250" style="border-radius: 10px;" alt="Danilo Verginio">
    <br>
  </a>
</div>
  


### Principais Conhecimentos
- Java: Para criação de API's REST com Spring.
- SQL: Para modelagem, criação e manipulação de Banco de Dados.
- Git: Versionamento de código.
- Vue.js: Framework JavaScript.

# Contatos
<div>
<a href="https://github.com/Daniloel" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-GitHub-%23000?style=for-the-badge&logo=github&logoColor=white" target="_blank"></a>
<a href="https://www.linkedin.com/in/seu-usuário-linkedln-aqui" target="_blank"><img loading="lazy" src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>

## Projeto01 - Fatec
***Sistema de visualização de dados da covid-19 no estado de São Paulo.***

### Parceiro Corporativo  
FATEC

### Descrição
Desenvolver um programa que processe dados oficiais da COVID-19 em SP e os apresente de forma clara e acessível à população, através de gráficos e visualizações, facilitando a compreensão da pandemia.

[Repositório](https://github.com/Daniloel/Projeto-Integrador-2021-2-Grupo3)



### Tecnologias Utilizadas
- **Python**: Para desenvolvimento rápido e intuitivo de análise e visualização de dados.<br>
- **Pandas**: Para manipulação eficiente de grandes volumes de dados.<br>
- **Matplotlib**: Para visualização de dados com gráficos interativos e personalizáveis.


### Contribuições pessoais
<div align="justify">
Como desenvolvedor de software, participei ativamente no desenvolvimento deste projeto, contribuindo tanto na lógica de programação, que neste caso foi procedural, com foco em laços e condições, quanto na obtenção de dados. Meu envolvimento não se limitou apenas à codificação, mas também à proposição de ideias que auxiliaram no progresso do projeto.
Durante o desenvolvimento do projeto, tive a oportunidade de aprender e utilizar o sistema de versionamento Git e a plataforma GitHub. Essa experiência foi fundamental para o meu crescimento como desenvolvedor, permitindo que eu trabalhasse de forma colaborativa e organizada, controlando as diferentes versões do código e facilitando o trabalho em equipe.
</div>
<details>
<summary><b>Utilização de laços</b></summary>
No exemplo, um laço permitiu criar um mecanismo para selecionar as análises desejadas.
    plpl = str("")
    while plpl !=("90"):
        print('''[ 1 ] dado específico
                    [ 2 ] comparações
                        [ x ] Voltar a escolha das cidades/estado''')
        F = input("Digite a sua escolha: ")

        if F == "1":
            print("escolha entre os dados disponíveis(abaixo):")
            print('''[ 1 ] Casos confirmados
                                         [ 2 ] Óbitos confirmados''')
            FF = input("Digite a sua escolha: ")

            if FF == "1":

                print('''\033[0;35mEscolha uma das opçoes
                                            [ 1 ] data expecifica
                                            [ 2 ] última data disponível
                                            [ 3 ] Ano de 2020
                                            [ 4 ] Ano de 2021
                                            [ 5 ] 1ºSemestre 2020
                                            [ 6 ] 2ºSemestre 2020
                                            [ 7 ] 1ºSemestre 2021
                                            [ 8 ] 2ºSemestre 2021
                                            [ 9 ] Range inputável\033[m''')
                esc = str("")

                while esc != ("1", "2", "3", "4", "5", "6", "7", "8"):

                    esc = str(input('Digite a sua escolha(1, 2, 3, 4, 5 ,6, 7, 8, 9): '))

                    if esc == "1":
                        dt2 = input("\033[0;35mDigite a data nesse formato(ano-mês-dia)ex:yyyy-mm-dd:\033[m")

                        colDT2 = colSP1.loc[colSP1["date"] == dt2]

                        while colDT2.empty:
                            print("\033[0;31mData não encontrada\n Digite novamente\033[m")
                            dt2 = input("Digite a data nesse formato(ano-mês-dia)ex:yyyy-mm-dd:")
                            colDT2 = colSP1.loc[colSP1["date"] == dt2]

                        colDT2 = colDT2.drop("state", axis=1)
                        colDT2 = colDT2.drop("place_type", axis=1)

                        plt.bar(colDT2['date'], colDT2['new_confirmed'], label='Casos', color='g', ls='--',
                                lw='2')  # Caso queira grafico de barras colocar - plt.bar()
                        plt.legend(loc=2, fontsize='15')  # Personalização da legenda
                        plt.ylabel('Casos Confirmados')  # Nome do Eixo Y
                        plt.xlabel('Data')  # Nome do Eixo X
                        plt.title('Gráfico situação de casos por dia')  # Título do gráfico
                        xxxx = colDT2.sum()
                        print("Casos de Covid no dia:")
                        print(xxxx["new_confirmed"])
                        plt.show()
                        break
</details>


<details>
<summary><b>Gráficos</b></summary>
Através do matplolib foi possivel criar gráficos para a visualizção do cliente;

		plt.bar(colDT2['date'], colDT2['new_confirmed'], label='Casos', color='g', ls='--',
		    lw='2')  # Caso queira grafico de barras colocar - plt.bar()
	    plt.legend(loc=2, fontsize='15')  # Personalização da legenda
	    plt.ylabel('Casos Confirmados')  # Nome do Eixo Y
	    plt.xlabel('Data')  # Nome do Eixo X
	    plt.title('Gráfico situação de casos por dia')  # Título do gráfico
	    xxxx = colDT2.sum()
	    print("Casos de Covid no dia:")
	    print(xxxx["new_confirmed"])
    		plt.show()
</details>

### Aprendizados efetivos

### Hard Skills

- **Python**: sei fazer com ajuda
- **Pandas**:  sei fazer com ajuda
- **Matplotlib**: sei fazer com ajuda
- **Git**:  sei fazer com ajuda 
- **GitHub**:  sei fazer com ajuda
- **Jira**:  sei fazer com ajuda

### SoftSkills
<div align="justify">
- <strong>Comunicação</strong>: Durante este semestre, as aulas no formato online apresentaram desafios extras na comunicação, exigindo que eu aprimorasse essa habilidade com meu grupo. Investir na comunicação com a equipe fortaleceu os laços entre os membros e facilitou o aprendizado por meio da troca de experiências individuais.
</div>
<div align="justify">
- <strong>Aprendizado</strong>:Como este foi meu primeiro semestre, precisei me dedicar intensamente ao estudo para compreender os fundamentos do desenvolvimento de software e adquirir a base necessária para programar em Python, além de aprender a usar ferramentas como o github. O aprendizado contínuo foi essencial para meu progresso, permitindo que eu evoluísse gradativamente e aplicasse os conhecimentos adquiridos na prática.
</div>

## Projeto02 - Dom Rock
***Sistema de gerenciamento de clientes.***

### Parceiro Corporativo 
DOM ROCK

## Descrição do projeto
<div align="justify">
O projeto teve como desafio desenvolver um sistema eficiente para a gestão e ativação de clientes na plataforma Dom Rock. A solução deveria ser orientada à entrada e processamento de dados, permitindo a configuração de parâmetros e variáveis específicas de cada cliente para viabilizar a alocação estratégica de recursos. Além disso, o sistema deveria possibilitar a estimativa de consumo com base em fatores como volume de dados, número de usuários e demais variáveis relevantes, garantindo uma distribuição precisa e otimizada.
Para atender a essas necessidades, foi essencial a criação de interfaces intuitivas para cada etapa do processo, facilitando tanto a ativação quanto a gestão dos cadastros. A modelagem adequada da base de dados foi outro aspecto fundamental, assegurando a escalabilidade do sistema e sua integração futura com outras plataformas. Por fim, a solução incorporou mecanismos para a geração de relatórios e consultas detalhadas, proporcionando maior visibilidade e controle sobre o processo, tanto para a empresa quanto para os clientes.
</div>

[Repositório](https://github.com/DatatechOffice/datatech_api)

## Tecnologias utilizadas

- **Java**: Linguagem para desenvolvimento da aplicação back-end,utilizada com as lógicas para inserção, selecionar, deletar e excluir.
- **Java Swing**: Biblioteca de interface gráfica de usuário utilizada para criar interfaces gráficas.
- **SqlServer**: Foi utilizado um banco na nuvem azure(SqlServer) onde os dados de login e dos pedidos dos clientes foram armazenados;

### Contribuições pessoais
<div align="justify">
Contribuí para a modelagem da parte do banco de dados e implementei a conexão com o banco utilizando o padrão DAO (Data Access Object). Além disso, ajudei na criação do banco e das tabelas, garantindo uma estrutura adequada para armazenar e organizar os dados. Essa abordagem permitiu uma interação eficiente entre a aplicação e o banco de dados, oferecendo maior organização e flexibilidade na manipulação das informações.
</div>
<details>
  <summary><b>Modelo Relacional</b></summary>
  <br>
   Modelo do Banco de Dados.
	
   ![Imagem do Projeto](https://github.com/DatatechOffice/datatech_api/blob/main/Modelagem_Banco/DerDatatechGold.png))


</details> 

### Aprendizados efetivos

### Hard Skills
- **SQL**: sei fazer com ajuda
- **Modelagem de dados**: sei fazer com ajuda
- **Integração com banco de dados**: sei fazer com ajuda
- **Orientação a objetos**: sei fazer com ajuda

### SoftSkills
<div align="justify">
- <strong>Colaboração</strong>:Colaboração: Colaborei com a equipe para entender quais eram os requisitos necessários para o desenvolvimento técnico. Além disso, contribuí com as questões técnicas do banco e do backend."
</div>
<div align="justify">
- <strong>Criatividade</strong>: Ao trabalhar com uma empresa real pela primeira vez, foi necessário aplicar criatividade para desenvolver uma solução que atendesse aos requisitos estabelecidos.
</div>

## Projeto03 - Iacit
***Sistema de visualização de dados meteorológicos***

### Empresa parceira  
IACIT

## Descrição do projeto
<div align="justify">
O projeto desenvolvido para a IACIT teve como objetivo otimizar o processamento e a geração de relatórios customizados de dados meteorológicos, eliminando processos manuais e aumentando a eficiência da empresa. A solução foi uma aplicação web que permite a importação e o armazenamento de dados do Instituto Nacional de Meteorologia (INMET) em um banco de dados, possibilitando consultas filtradas por data, região, estado, estação e variáveis meteorológicas.
Além disso, o sistema oferece funcionalidades avançadas, como exibição de informações em gráficos e cards, além da exportação de relatórios detalhados em formato de planilhas. Com um controle de acesso integrado, funcionários com permissões administrativas podem gerenciar usuários e relatórios, garantindo maior segurança e organização no uso da plataforma.
</div>

[Repositório](https://github.com/DatatechOffice/Api_Iacit)

## Tecnologias utilizadas
<div align="justify">
- <strong>Java e Spring</strong>:O backend da aplicação foi desenvolvido em Java, utilizando o framework Spring Boot para agilizar o desenvolvimento e a configuração do projeto. Com o uso do Spring, foram criadas APIs REST que permitem a comunicação entre o frontend e o banco de dados, garantindo a persistência dos dados meteorológicos e o envio de informações em formato JSON.
A injeção de dependências do Spring facilitou a implementação de recursos essenciais, tornando o sistema mais modular e eficiente. Dessa forma, a aplicação conseguiu oferecer uma estrutura robusta para o processamento e a disponibilização de dados meteorológicos de forma ágil e segura.
</div>
<div align="justify">
- <strong>Html, Css, Javascript</strong>:O frontend da aplicação foi desenvolvido com JavaScript, HTML e CSS, garantindo uma interface dinâmica e interativa. O JavaScript possibilitou a manipulação dos dados em tempo real, exibindo informações por meio de gráficos e cards, enquanto o HTML estruturou os elementos e o CSS assegurou um design responsivo e intuitivo.
</div>
<div align="justify">
- <strong>PostgreSQL</strong>:O PostgreSQL foi utilizado como sistema de gerenciamento de banco de dados relacional para armazenar e organizar os dados meteorológicos, incluindo informações de estações e regiões. Sua eficiência, versatilidade e alto desempenho facilitaram a consulta, manipulação e geração de relatórios, garantindo um armazenamento seguro e otimizado para grandes volumes de dados.
</div>

### Contribuições pessoais
<div align="justify">
No projeto, atuei como desenvolvedor fullstack, contribuindo tanto no frontend quanto no backend e no banco de dados. No frontend, realizei o levantamento e estudo das ferramentas mais adequadas para a interface do usuário. No backend, desenvolvi APIs para a comunicação entre o sistema e o banco de dados. Além disso, participei da modelagem do banco de dados, garantindo uma estrutura eficiente para armazenar e acessar as informações.
</div>

<details>
  <summary><b>API REST</b></summary>

```java
@Controller
public class PrecipitacaoController {

    @Autowired(required = true)
    private ServicePrecipitacao precipitacaoService;

    @PostMapping(value = { "/precipitacao" }, consumes = MediaType.APPLICATION_JSON_VALUE)
    public ResponseEntity<List<Precipitacao>> postFiltroPorData(@RequestBody FilterDataVo data) throws ParseException {
        List<Precipitacao> listPrecipitacao = precipitacaoService.getByFilter(data.getEstacao(), data.getDataInicio(),
                data.getDataFim());

        return listPrecipitacao != null && listPrecipitacao.size() > 0
                ? new ResponseEntity<List<Precipitacao>>(listPrecipitacao, HttpStatus.CREATED)
                : new ResponseEntity<List<Precipitacao>>(listPrecipitacao, HttpStatus.BAD_REQUEST);
    }
}
```

</details> 

<details>
  <summary><b>Requisição HTTP</b></summary>

```javascript
async function carregar_UF(valUF){
	if(valUF.length >= 1){
		
		const resUF = await fetch('../data/estados.json');
		const UFJson = await resUF.json();

		var html = "<ul class='list-group' position-fixed>";
		for(let i = 0; i < UFJson.length; i++){
			if(UFJson[i].name.toLowerCase().startsWith(valUF.toLowerCase())){
				html += "<li class='list-group-item list-group-item-action' onclick='get_name_UF("+JSON.stringify(UFJson[i].name)+")'>" + UFJson[i].name + "</li>";
			}
		}
		html += "</ul>";
		document.getElementById('pesquisa_UF').innerHTML = html;
	}else{
		document.getElementById('pesquisa_UF').innerHTML = '';
	}
}
```

</details> 

### Aprendizados efetivos
### Hard Skills
- **SQL**: sei fazer com autonomia
- **PostgreSQL**: sei fazer com autonomia
- **Git e github**: sei fazer com autonomia
- **Consumo de API** Rest: sei fazer com autonomia
- **Desenvolvimento de código através de interfaces**: sei fazer com ajuda

### SoftSkills
<div align="justify">
- <strong>Versatilidade</strong>:Atuei tanto no front-end quanto no back-end deste projeto, o que exigiu a capacidade de adaptar-me às diferentes demandas de cada stack, garantindo um desenvolvimento equilibrado e eficiente.
</div>
<div align="justify">
- <strong>Proatividade</strong>: Busquei compreender as necessidades do projeto e interagir ativamente com toda a equipe, contribuindo com ideias e sugestões para que, juntos, pudéssemos encontrar as melhores soluções de forma eficiente.
</div>

## Projeto04 - Embraer
***Sistema de controle de configuração de aeronaves***

### Parceiro Corporativo
Embraer

## Descrição do projeto
<div align="justify">
A gestão das configurações de aeronaves é um desafio crítico na indústria aeronáutica. Para otimizar esse processo, foi desenvolvido um sistema que permite aos usuários consultar, verificar e editar itens instalados ou aplicáveis a diferentes chassis, conforme uma base de dados estruturada. O sistema armazena todas as regras de composição dos itens e, ao consultar um número de chassi, recupera e exibe as informações relevantes para o usuário, garantindo precisão e eficiência na gestão dos componentes.
Além disso, a solução foi aprimorada com uma interface intuitiva, voltada para a experiência do usuário, permitindo acesso tanto por computadores quanto por dispositivos móveis via hospedagem em nuvem. No caso específico da Embraer, um Sistema de Controle de Configuração de Aeronaves foi customizado para facilitar a verificação de configurações antes do voo, ajudando os pilotos a garantir a segurança e a eficiência operacional das aeronaves.
</div>

[Repositório](https://github.com/GroupHextech/HEXTECH-API4sem)

## Tecnologias utilizadas
- **Java e Spring Boot**: A programação foi realizada em Java, utilizando o Spring Boot, um framework robusto, para o desenvolvimento de aplicações web e criação de APIs RESTful.
- **Vue.js**: Para a interface de usuário, foi adotado o Vue.js, um framework JavaScript que facilita a construção de frontends dinâmicos e responsivos.
- **Autonomous Database Oracle**: A gestão dos dados foi realizada através do Oracle Autonomous Database, uma plataforma de banco de dados em nuvem automatizada e escalável.

### Contribuições pessoais
<div align="justify">
Atuei como Product Owner no projeto, sendo responsável por definir e priorizar funcionalidades, garantindo que a equipe entregasse valor ao negócio. Gerenciei o backlog, alinhei expectativas com stakeholders e assegurei que o produto atendesse às necessidades dos usuários. Além disso, facilitei a comunicação entre as partes envolvidas, tomei decisões estratégicas e acompanhei o desenvolvimento para garantir a entrega eficiente e alinhada aos objetivos do projeto.
</div>

### Aprendizados efetivos
### Hard Skills
- **Slack**: sei fazer com autonomia
- **Git e github**: sei fazer com autonomia
  
### SoftSkills
<div align="justify">
- <strong>Adaptabilidade</strong>: Com uma equipe nova, precisei me adaptar rapidamente ao ambiente e às dinâmicas de trabalho. A flexibilidade foi essencial para lidar com mudanças e desafios,
garantindo que mantivéssemos o foco no objetivo final e atendêssemos às necessidades do cliente de forma ágil e eficiente.
</div>
<div align="justify">
- <strong>Comunicação</strong>:No projeto, desenvolvi minhas habilidades de comunicação ao interagir diretamente com o cliente para levantar requisitos e alinhar expectativas. Essa experiência me permitiu aprimorar a escuta ativa, a clareza na transmissão de informações e a capacidade de articular soluções de forma eficiente, garantindo que as necessidades do cliente fossem compreendidas e transformadas em requisitos bem definidos para a equipe de desenvolvimento.
</div>

## Projeto05 - Pro4Tech
***Sistema interativo de visualizaçãode de dados dos processo de recrutamento e seleção***

### Parceiro Corporativo 
Pro4Tech

## Descrição do projeto
<div align="justify">
O objetivo da aplicação é desenvolver um dashboard interativo para centralizar e visualizar dados do processo de recrutamento e seleção de uma empresa. A plataforma permitirá análises em tempo real de métricas como número de candidatos, tempo médio de contratação e custos, além de gerar relatórios dinâmicos que apoiam a tomada de decisões estratégicas.
Os usuários poderão personalizar relatórios de acordo com suas necessidades, aplicando filtros para visualizar informações específicas. Com essa abordagem, a ferramenta visa otimizar o processo de recrutamento, identificando padrões e tendências que contribuam para maior eficiência e melhor alocação de recursos.
</div>

[Repositório](https://github.com/Localhost-305/LocalHost305)


## Tecnologias utilizadas
- **java**:Linguagem de programação orientada a objetos, amplamente usada para desenvolvimento de sistemas corporativos, aplicativos móveis e servidores, com portabilidade garantida pela Java Virtual Machine (JVM).
- **Github Actions**:Plataforma de automação para CI/CD integrada ao GitHub, permitindo a criação de fluxos de trabalho para testes, compilação e deploy automáticos de código.
- **React**:Biblioteca JavaScript para criação de interfaces de usuário interativas e reutilizáveis, focada em componentes e otimizada para aplicativos de uma única página (SPA).
- **Python**Linguagem de programação de alto nível, conhecida pela sintaxe simples e versatilidade, amplamente usada em análise de dados

### Contribuições pessoais
<div align="justify">
No projeto, atuei como desenvolvedor backend, sendo responsável pela criação de APIs REST que permitissem a interação eficiente com os dados provenientes do banco de dados. Além de tratar e organizar esses dados de forma otimizada, garanti que as informações fossem processadas corretamente para atender às necessidades do sistema. Também contribuí para o desenvolvimento do frontend, colaborando na apresentação dos dados em um formato visual mais acessível.
</div>

<details>
  <summary><b>Api Rest</b></summary>

```java
@RestController
@RequestMapping("/hiring")
public class FactHiringController {

    private final FactHiringService factHiringService;

    public FactHiringController(FactHiringService factHiringService) {
        this.factHiringService = factHiringService;
    }

    @GetMapping("cost")
    public ResponseEntity<List<Map<String, Object>>> getHiringCost(
            @RequestParam @DateTimeFormat(pattern = "yyyy-MM-dd") LocalDate startDate,
            @RequestParam @DateTimeFormat(pattern = "yyyy-MM-dd") LocalDate endDate) {
        List<Map<String, Object>> totalCost = factHiringService.calculateTotalCostPerMonth(startDate, endDate);
        return ResponseEntity.ok(totalCost);
    }

```

</details> 


<details>
  <summary><b>React</b></summary>

```javaScript
 <StyledCard bordered>
          <div className="card-bg"></div>
          <h1 className="card-title">Retenção Média</h1>
          <h2 className="card-date" style={{ fontSize: '50px', margin: '35px 0px 0px 0px' }}>
            <span>{retentions ? `${Math.floor(retentions.retentionDays)} dias` : '0 dias'}</span>
          </h2>
        </StyledCard>

```
</details> 

<details>
  <summary><b>CI</b></summary>

```javaScript
name: Workflow de Integração Contínua

on:
  push:
    branches:
      - feature/LOC-69

jobs:
  build-CI:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Setup Node
        uses: actions/setup-node@v4
        with:
          node-version: 20
          cache: 'npm'

      - name: Install dependencies
        run: npm install
        
      - name: Run npm ci
        run: npm ci

      - name: Build React app
        run: npm run build

      - name: Run tests
        run: npm test


```

</details> 

### Aprendizados efetivos
### Hard Skills
- **Integração do banco com Spring Data**: sei fazer com autonomia
- **Arquitetura REST**: sei fazer com autonomia
- **Gitflow Workflow**: sei fazer com autonomia
- **Continuous integration (CI)** : sei fazer com autonomia
  
### SoftSkills
<div align="justify">
- <strong>Trabalho em equipe</strong>: A sintonia e a cooperação entre os integrantes foram essenciais neste projeto. Com a adoção de novas tecnologias, foi preciso que todos aprendessem juntos e trocassem conhecimentos, assegurando que cada um compreendesse a aplicação das inovações no desenvolvimento. Graças a uma comunicação clara e ao forte espírito colaborativo, conseguimos tornar o processo mais eficiente, acelerando e aprimorando a produtividade.
</div>
<div align="justify">
- <strong>Adaptabilidade</strong>: Durante o projeto, fui desafiado a trabalhar com React, mesmo sem conhecimento prévio da tecnologia. Diante dessa situação, busquei aprender rapidamente, explorando documentações, realizando cursos e aplicando os conceitos no desenvolvimento. A capacidade de adaptação foi essencial para compreender a estrutura do framework e contribuir de forma eficiente para o projeto.
</div>

## Projeto06 - Imagem
***Sistema de análise de sentimento por geolocalização***

### Parceiro Corporativo 
Imagem

## Descrição do projeto
<div align="justify">
O desafio proposto foi desenvolver uma plataforma sofisticada para analisar e visualizar os sentimentos dos clientes com base em avaliações online, integrando tecnologia de ponta para fornecer insights geograficamente contextualizados.
A solução consiste em uma inteligência artificial (IA) que analisa sentimentos nas avaliações de clientes sobre hotéis, classificando-os como neutros, positivos ou negativos. Os dados foram armazenados em um banco de dados não relacional, e com base nesses dados foi desenvolvido um software que apresentava insights valiosos por meio de funcionalidades como mapas interativos, gráficos de tendências, cards informativos e um sistema de gerenciamento de acesso. 
</div>

[Repositório](https://github.com/CarcaraTec/Imagem-api6sem)
## Tecnologias utilizadas 

- **Java e Spring boot**: A linguagem Java foi utilizada em conjunto ao framework Spring para desenvolvimento da camada de segurança da aplicação.
- **Python e Flask**: A linguagem Python foi utilizada em conjunto ao framework Flask para desenvolvimento web e criação de API's REST.
- **MongoDB**: Tecnologia em banco de dados nao relacional para armazenar os dados do nosso dataset.
- **MySQL**: Sistema de gerenciamento de banco de dados utilizado para armazenar dados dos usuarios.
- **Vue.js**: Framework javascript Vue.js para o frontend da aplicação.

### Contribuições pessoais

<div align="justify">
No papel de Scrum Master, fui responsável por gerenciar as tarefas entre os desenvolvedores, garantindo uma melhor distribuição do trabalho e o alinhamento com os objetivos do projeto. Atuei ativamente na remoção de impedimentos, facilitando a execução das atividades e assegurando que a equipe pudesse trabalhar de forma mais fluida e produtiva.
Além disso, acompanhei e mantive atualizado o burndown chart, monitorando o progresso do time e auxiliando na identificação de possíveis gargalos. Com isso, contribuí para a organização e eficiência do desenvolvimento, promovendo um ambiente colaborativo e alinhado com os princípios ágeis.
</div>

### Aprendizados efetivos
### Hard Skills
- **Python**: sei fazer com autonomia
- **MongoDB**: sei fazer com ajuda
- **YouTrack** : sei fazer com autonomia
  
### SoftSkills
<div align="justify">
- <strong>Colaboração</strong>:Atuei lado a lado com a equipe, oferecendo suporte, trocando conhecimentos e propondo soluções para impulsionar o desenvolvimento do projeto. Além disso, contribuí ativamente para a implementação da LGPD, auxiliando na adaptação do sistema às diretrizes de proteção de dados.
</div>	
<div align="justify">
- <strong>Comunicação</strong> Mantive uma comunicação clara e constante com a equipe, garantindo alinhamento entre os desenvolvedores e facilitando o fluxo de informações. Atuei conduzindo reuniões diárias, removendo impedimentos e promovendo um ambiente onde todos pudessem expressar ideias e preocupações. Além disso, incentivei a troca de feedbacks e a colaboração entre os membros, assegurando que o time trabalhasse de forma integrada e produtiva para alcançar os melhores resultados no projeto
</div>
