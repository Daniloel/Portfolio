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
### Descrição
Desenvolver um programa que processe dados oficiais da COVID-19 em SP e os apresente de forma clara e acessível à população, através de gráficos e visualizações, facilitando a compreensão da pandemia.

[GIT - Fatec](https://github.com/LeoAdlerr/Projeto-Integrador-2021-2-Grupo3)



### Tecnologias Utilizadas
<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40" height="40"/> Python: Para desenvolvimento rápido e intuitivo de análise e visualização de dados.<br>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="40" height="40"/> Pandas: Para manipulação eficiente de grandes volumes de dados.<br>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" width="40" height="40"/> Matplotlib: Para visualização de dados com gráficos interativos e personalizáveis.


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
<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40" height="40"/> Python: Para desenvolvimento rápido e intuitivo de análise e visualização de dados. - sei fazer com ajuda<br>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" width="40" height="40"/> Pandas: Para manipulação eficiente de grandes volumes de dados. - sei fazer com ajuda<br>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" width="40" height="40"/> Matplotlib: Para visualização de dados com gráficos interativos e personalizáveis. - sei fazer com ajuda<br>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="40" height="40"/> Git: Sistema de controle de versão distribuído para rastrear alterações no código fonte. - sei fazer com ajuda <br>

<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" width="40" height="40"/> GitHub: Plataforma de hospedagem de código para colaboração e gerenciamento de projetos usando Git. - sei fazer com ajuda<br>


<img loading="lazy" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jira/jira-original.svg" width="40" height="40"/> Jira: Ferramenta de gerenciamento de projetos e rastreamento de bugs, amplamente utilizada em desenvolvimento de software. - sei fazer com ajuda<br>

### SoftSkills
- **Comunicação**: <br>
Durante este semestre, as aulas no formato online apresentaram desafios extras na comunicação, exigindo que eu aprimorasse essa habilidade com meu grupo. Investir na comunicação com a equipe fortaleceu os laços entre os membros e facilitou o aprendizado por meio da troca de experiências individuais.

- **Aprendizado**:
Como este foi meu primeiro semestre, precisei me dedicar intensamente ao estudo para compreender os fundamentos do desenvolvimento de software e adquirir a base necessária para programar em Python, além de aprender a usar ferramentas como o github. O aprendizado contínuo foi essencial para meu progresso, permitindo que eu evoluísse gradativamente e aplicasse os conhecimentos adquiridos na prática.


## Projeto02 - Dom Rock

## Projeto03 - Iacit

## Projeto04 - Embraer

## Projeto05 - Pro4Tech

## Projeto05 - Imagem
