# Danilo Verginio da Silva
Meu nome é Danilo Vergínio da Silva e sou tecnólogo em Banco de Dados pela FATEC São José dos Campos. Durante minha formação, adquiri sólidos conhecimentos em bancos de dados relacionais e NoSQL, além de experiência em desenvolvimento de software utilizando linguagens como Python, Java, javaScript e SQL. Ao longo dessa jornada, desenvolvi habilidades técnicas e interpessoais, como liderança de equipes em projetos de desenvolvimento, capacidade de trabalhar em ambientes colaborativos e a prática de boas práticas de programação, através de Projetos Integrados (API).

| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/88066389?v=4" width=115><br><sub>Danilo Verginio</sub>](https://github.com/Daniloel) |     
| :---: |

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

## [Projeto01 - Fatec](primeiroSemestre/README.md)
***Sistema de visualização de dados da covid-19 no estado de São Paulo.***

### Parceiro Corporativo  
FATEC

### Descrição
Desenvolver um programa que processe dados oficiais da COVID-19 em SP e os apresente de forma clara e acessível à população, através de gráficos e visualizações, facilitando a compreensão da pandemia.

[GIT - Fatec](https://github.com/LeoAdlerr/Projeto-Integrador-2021-2-Grupo3)



### Tecnologias Utilizadas
- **Python**: Para desenvolvimento rápido e intuitivo de análise e visualização de dados.<br>
- **Pandas**: Para manipulação eficiente de grandes volumes de dados.<br>
- **Matplotlib**: Para visualização de dados com gráficos interativos e personalizáveis.


### Contribuições pessoais
Como desenvolvedor de software, participei ativamente no desenvolvimento deste projeto, contribuindo tanto na lógica de programação, que neste caso foi procedural, com foco em laços e condições, quanto na obtenção de dados. Meu envolvimento não se limitou apenas à codificação, mas também à proposição de ideias que auxiliaram no progresso do projeto.
Durante o desenvolvimento do projeto, tive a oportunidade de aprender e utilizar o sistema de versionamento Git e a plataforma GitHub. Essa experiência foi fundamental para o meu crescimento como desenvolvedor, permitindo que eu trabalhasse de forma colaborativa e organizada, controlando as diferentes versões do código e facilitando o trabalho em equipe.

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

- **Python**: Para desenvolvimento rápido e intuitivo de análise e visualização de dados. - sei fazer com ajuda<br>
- **Pandas**: Para manipulação eficiente de grandes volumes de dados. - sei fazer com ajuda<br>
- **Matplotlib**: Para visualização de dados com gráficos interativos e personalizáveis. - sei fazer com ajuda<br>
- **Git**: Sistema de controle de versão distribuído para rastrear alterações no código fonte. - sei fazer com ajuda <br>
- **GitHub**: Plataforma de hospedagem de código para colaboração e gerenciamento de projetos usando Git. - sei fazer com ajuda<br>
- **Jira**: Ferramenta de gerenciamento de projetos e rastreamento de bugs, amplamente utilizada em desenvolvimento de software. - sei fazer com ajuda<br>

### SoftSkills
- **Comunicação**: <br>
Durante este semestre, as aulas no formato online apresentaram desafios extras na comunicação, exigindo que eu aprimorasse essa habilidade com meu grupo. Investir na comunicação com a equipe fortaleceu os laços entre os membros e facilitou o aprendizado por meio da troca de experiências individuais.

- **Aprendizado**:
Como este foi meu primeiro semestre, precisei me dedicar intensamente ao estudo para compreender os fundamentos do desenvolvimento de software e adquirir a base necessária para programar em Python, além de aprender a usar ferramentas como o github. O aprendizado contínuo foi essencial para meu progresso, permitindo que eu evoluísse gradativamente e aplicasse os conhecimentos adquiridos na prática.


## Projeto02 - Dom Rock
***Sistema de gerenciamento de clientes.***

### Parceiro Corporativo 
DOM ROCK

## Descrição do projeto
O projeto teve como desafio desenvolver um sistema eficiente para a gestão e ativação de clientes na plataforma Dom Rock. A solução deveria ser orientada à entrada e processamento de dados, permitindo a configuração de parâmetros e variáveis específicas de cada cliente para viabilizar a alocação estratégica de recursos. Além disso, o sistema deveria possibilitar a estimativa de consumo com base em fatores como volume de dados, número de usuários e demais variáveis relevantes, garantindo uma distribuição precisa e otimizada.

Para atender a essas necessidades, foi essencial a criação de interfaces intuitivas para cada etapa do processo, facilitando tanto a ativação quanto a gestão dos cadastros. A modelagem adequada da base de dados foi outro aspecto fundamental, assegurando a escalabilidade do sistema e sua integração futura com outras plataformas. Por fim, a solução incorporou mecanismos para a geração de relatórios e consultas detalhadas, proporcionando maior visibilidade e controle sobre o processo, tanto para a empresa quanto para os clientes.

[GIT - DomRock](https://github.com/DatatechOffice/datatech_api)

## Tecnologias utilizadas

- **Java**: Linguagem para desenvolvimento da aplicação back-end,utilizada com as lógicas para inserção, selecionar, deletar e excluir.
- **Java Swing**: Biblioteca de interface gráfica de usuário utilizada para criar interfaces gráficas.
- **SqlServer**: Foi utilizado um banco na nuvem azure(SqlServer) onde os dados de login e dos pedidos dos clientes foram armazenados;

### Contribuições pessoais
Contribuí para a modelagem da parte do banco de dados e implementei a conexão com o banco utilizando o padrão DAO (Data Access Object). Além disso, ajudei na criação do banco e das tabelas, garantindo uma estrutura adequada para armazenar e organizar os dados. Essa abordagem permitiu uma interação eficiente entre a aplicação e o banco de dados, oferecendo maior organização e flexibilidade na manipulação das informações.

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
- **Colaboração**:Colaboração: Colaborei com a equipe para entender quais eram os requisitos necessários para
 o desenvolvimento técnico. Além disso, contribuí com as questões técnicas do banco e do backend."

- **Criatividade**: Ao trabalhar com uma empresa real pela primeira vez, foi necessário aplicar criatividade para desenvolver uma solução que atendesse aos requisitos estabelecidos.

## Projeto03 - Iacit
***Sistema de visualização de dados meteorológicos***

### Empresa parceira  
IACIT

## Descrição do projeto

[GIT - IACIT](https://github.com/DatatechOffice/Api_Iacit)

## Tecnologias utilizadas
### Contribuições pessoais
### Aprendizados efetivos
### Hard Skills
### SoftSkills


## Projeto04 - Embraer
***Sistema de controle de configuração de aeronaves***

### Parceiro Corporativo
Embraer

## Descrição do projeto

[GIT - EMBRAER](https://github.com/GroupHextech/HEXTECH-API4sem)
## Tecnologias utilizadas
### Contribuições pessoais
### Aprendizados efetivos
### Hard Skills
### SoftSkills
- **Adaptabilidade**: Com uma equipe nova, precisei me adaptar rapidamente ao ambiente e
às dinâmicas de trabalho. A flexibilidade foi essencial para lidar com mudanças e desafios,
garantindo que mantivéssemos o foco no objetivo final e atendêssemos às necessidades do cliente de forma ágil e eficiente.

## Projeto05 - Pro4Tech

***Sistema interativo de visualizaçãode de dados dos processo de recrutamento e seleção***

### Parceiro Corporativo 
Pro4Tech

## Descrição do projeto
O objetivo da aplicação é desenvolver um dashboard interativo para centralizar e visualizar dados do processo de recrutamento e seleção de uma empresa. A plataforma permitirá análises em tempo real de métricas como número de candidatos, tempo médio de contratação e custos, além de gerar relatórios dinâmicos que apoiam a tomada de decisões estratégicas.

Os usuários poderão personalizar relatórios de acordo com suas necessidades, aplicando filtros para visualizar informações específicas. Com essa abordagem, a ferramenta visa otimizar o processo de recrutamento, identificando padrões e tendências que contribuam para maior eficiência e melhor alocação de recursos.

## Tecnologias utilizadas
### Contribuições pessoais
### Aprendizados efetivos
### Hard Skills
### SoftSkills

## Projeto06 - Imagem
***Sistema de análise de sentimento por geolocalização***

### Parceiro Corporativo 
Imagem

## Descrição do projeto
O desafio proposto foi desenvolver uma plataforma sofisticada para analisar e visualizar os sentimentos dos clientes com base em avaliações online, integrando tecnologia de ponta para fornecer insights geograficamente contextualizados.

A solução consiste em uma inteligência artificial (IA) que analisa sentimentos nas avaliações de clientes sobre hotéis, classificando-os como neutros, positivos ou negativos. Os dados foram armazenados em um banco de dados não relacional, e com base nesses dados foi desenvolvido um software que apresentava insights valiosos por meio de funcionalidades como mapas interativos, gráficos de tendências, cards informativos e um sistema de gerenciamento de acesso. 


[GIT](https://github.com/CarcaraTec/Imagem-api6sem)
## Tecnologias utilizadas 

- **Java e Spring boot**: A linguagem Java foi utilizada em conjunto ao framework Spring para desenvolvimento da camada de segurança da aplicação.
- **Python e Flask**: A linguagem Python foi utilizada em conjunto ao framework Flask para desenvolvimento web e criação de API's REST.
- **MongoDB**: Tecnologia em banco de dados nao relacional para armazenar os dados do nosso dataset.
- **MySQL**: Sistema de gerenciamento de banco de dados utilizado para armazenar dados dos usuarios.
- **Vue.js**: Framework javascript Vue.js para o frontend da aplicação.

### Contribuições pessoais
### Aprendizados efetivos
### Hard Skills
### SoftSkills
