# CRIAÇÃO E USO DE CLASSIFICADORES

*Documento eProc - Material de Treinamento*

---

---

# CRIAÇÃO E USO DE CLASSIFICADORES

# POR CONTEÚDO NA

# AUTOMATIZAÇÃO DA TRAMITAÇÃO

# PROCESSUAL NO EPROC

![Imagem Imagem_2266](imgs/Imagem_2266.png)


---

**1. Introdução**
**Este tutorial tem por objetivo apresentar a utilidade e a forma de uso do classificador****por conteúdo, funcionalidade disponível no eproc de forma integrada à****Automatização da Tramitação Processual.**
**2. Problemas que busca solucionar**
**No tratamento de demandas judiciais há várias automações que podem ser feitas****simplesmente com os dados cadastrados no processo judicial, tal como classe****judicial, competência, evento, tipo de petição, partes etc.****No eproc, a funcionalidade de automatização da tramitação processual (ou****automatização de localizadores) possibilita que o próprio órgão judicial crie um****conjunto de regras de automação utilizando diversos tipos de controle: por tipo de****petição, por evento, por tempo, por tipo de documento etc.****A automação da tramitação processual permite ainda agregar detalhes às regras,****como, por exemplo, a entidade envolvida, a classe judicial, o assunto do processo.****Mesmo com todas estas possibilidades, em muitos casos a análise do texto do****documento que está sendo juntado ao processo ainda é necessária para a****identificação mais precisa do fluxo que o processo deve seguir.**
## TUTORIAL PARA CRIAÇÃO E USO DE

## CLASSIFICADORES POR CONTEÚDO NA

## AUTOMATIZAÇÃO DA TRAMITAÇÃO

## PROCESSUAL NO EPROC


---

**Desta forma, o classificador por conteúdo permite à própria unidade judicial****cadastrar um conjunto de exemplos de documentos ou filtro por palavras, de modo****que, na juntada de um novo documento, o sistema identifique a similaridade entre o****documento que está sendo juntado em relação aos exemplos cadastrados, além****disso, de forma alternativa, é possível informar filtros por palavras chaves ou frases****que devem constar no documento, essas duas opções de classificação por conteúdo****podem ser utilizadas em conjunto ou separadas.****A partir desta análise de similaridade e/ou filtro por palavras, mais outros critérios****cadastrados na automatização da tramitação processual, o sistema faz a triagem do****processo de forma automatizada.****Os documentos analisados pelo classificador por conteúdo podem ser documentos****PDF juntados por usuários externos (como a petição inicial ou outras petições****intermediárias) ou mesmo documentos HTML produzidos por usuários internos****(despachos, decisões, acórdãos etc).****Importante informar que essa funcionalidade não contempla documentos em formato****PDF que foram digitalizados, ou seja, nos casos onde as informações de um****documento constam como imagens, somente os documentos PDF com texto são****processados.**
**3. Passos para a criação e uso de um classificador por conteúdo**
**Esta seção descreve as etapas que a unidade deve efetuar para criar e utilizar um****classificador por conteúdo. A criação deste deve ser feita por usuário com perfil de****diretor de secretaria (chefe de cartório) ou de gabinete.****Como estudo de caso, este tutorial irá mostrar como criar um classificador para****identificar processos da classe execução fiscal, ajuizados pela Fazenda Nacional,****que sejam referentes a dívidas previdenciárias, na 19ª Vara Federal de Porto Alegre.****Para isto serão analisados os documentos do tipo “Petição inicial”.**


---

**3. 1. Identificar documentos de exemplo e/ou palavras chaves que constam nos**

**documentos**

O primeiro passo para a criação de um classificador por conteúdo é identificar ao

menos três documentos de exemplo. Para cada documento de exemplo, deve-se

anotar o número do processo e o sequencial do evento em que o documento foi

juntado.

Seguindo o exemplo, é possível identificar os seguintes processos na 19ª Vara de

Porto Alegre que são execuções fiscais ajuizadas pela Fazenda Nacional referentes a

dívidas

previdenciárias:

50054620820194047122,

50074471220194047122

e

50054880620194047122. Como iremos analisar a petição inicial, naturalmente o

sequencial do evento da distribuição será o sequencial “1”.

Além disso, é importante identificar palavras chaves ou frases que aparecem em

todos os documentos, essas informações podem ser utilizadas para criação de uma

regra específica de filtro por palavras.

Neste estudo de caso estamos criando o classificador na RSPOA19 e utilizando

documentos de exemplo de processos também da RSPOA19, além disso, serão

utilizadas as palavras chaves “previd” e “dívida”. Porém, os exemplos poderiam ser de

processos de outra vara.

**3. 2. Criação do classificador**

Utilizando o perfil de diretor de secretaria (ou diretor de gabinete/secretaria no caso

do 2º grau) devemos acessar a tela “Automatização da Tramitação Processua”,

conforme ilustra a Figura 1.

![Imagem Imagem_2303](imgs/Imagem_2303.png)

*Figura 1: Tela de Automatizar Tramitação Processual (posteriormente estará disponível no item de menu também)*


---

![Imagem Imagem_2304](imgs/Imagem_2304.png)

![Imagem Imagem_2305](imgs/Imagem_2305.png)

O sistema irá listar os classificadores já criados, cada vara tem seus classificadores

de conteúdo próprios, que atualmente não podem ser compartilhados com outras

varas (Figura 2).

*Figura 2: Lista de classificadores*

*Figura 3: Tela de cadastramento de classificador*

Como queremos criar um novo classificador, devemos acionar a opção “Novo”. O

sistema irá apresentar a tela de cadastramento (Figura 3).

Devemos dar um nome para o novo classificador. Este nome será exibido como opção

na tela de Automatização da Tramitação Processual. No nosso estudo de caso, iremos

chamar o classificador de “FN Previdenciário”.


---

Para melhorar a precisão dos classificadores é possível informar as principais palavras

ou frases que aparecem nos documentos de exemplo, desta forma, se os documentos

que estão sendo comparados não possuírem a(s) palavra(s) ou frase(s) informadas, o

sistema automaticamente desconsidera os mesmos, essa opção é muito útil

especialmente em documentos muito parecidos mas que tratam de pedidos

diferentes.

É uma boa prática a utilização de pelo menos uma palavra no campo filtro por

palavras. O filtro por palavras permite diferentes tipos de expressões:

**Aspas simples ‘. .’ ou duplas “. .” para frases: “art. 126” E “extinção da**

**punibilidade”**

1.

**OU para indicar uma ou mais palavras/frases válidas: (extint OU extinção)**

2.

**Deve-se utilizar parênteses para filtros OU (. .. OU. .. ): (extint OU extinção) E**

**(art. 924 OU artigo 924)**

3.

**Pode-se utilizar E para indicar mais de uma palavra obrigatória: extinto E**

**sumária**

4.

**Exclamação! ou NÃO para indicação de palavra(s) que não devem constar:**

**NÃO extint E! art. 12**

5.

Para esse estudo de caso os documentos devem conter a palavra “previd", o que na

prática inclui as palavras previdenciário, ou previdenciária, ou previdência, dentre

outras variações com o prefixo previd, além disso, a palavra dívida.

O sistema faz distinção da acentuação nas palavras, mas desconsidera as diferenças

de letras maiúsculas ou minúsculas nas comparações.

A seguir, é exibida a opção “tolerância”. Nesta opção podemos indicar o quão similar

aos documentos de exemplo o documento analisado deve ser.


---

No nosso exemplo, iremos manter 5% de tolerância (Figura 3).

Na sequência, podem ser cadastrados documentos de exemplo. Há duas formas: i)

informar o número do processo e sequencial do evento ou ii) fazer o envio de um

arquivo já salvo no computador. No estudo de caso, estamos utilizando a primeira

opção.

Sendo assim, iremos incluir os documentos de exemplo que havíamos anotado no

passo 1. Para tanto devemos preencher o número do processo, o sequencial do evento

e acionar a opção “Buscar” (Figura 4).

![Imagem Imagem_2306](imgs/Imagem_2306.png)

Por exemplo, configurando a tolerância como 5%, o documento a ser analisado deve

ser bem similar aos exemplos para disparar a regra de automação (no máximo 5% de

diferença entre o documento analisado e os exemplos).

Não convém aumentar muito a tolerância para que a automação não seja disparada

indevidamente.
<small>Tolerância é a porcentagem aceitável de diferenças do</small><small>conteúdo do documento analisado em relação aos</small><small>exemplos</small><small>cadastrados.</small><small>Quanto</small><small>menor</small><small>a</small><small>tolerância</small><small>configurada, mais similar devem ser os documentos de</small><small>exemplo e os documentos a serem analisados para que</small><small>seja aplicada a regra de automação de localizadores.</small>
*Figura 4: Detalhe para buscar os documentos de um processo e evento*


---

![Imagem Imagem_2307](imgs/Imagem_2307.png)

![Imagem Imagem_2308](imgs/Imagem_2308.png)

Após isto, devemos selecionar o documento desejado, neste caso INIC1, e acionar a

opção “Incluir”. Feito isso, o documento de exemplo passa a ser exibido mais abaixo

(Figura 5).

Para finalizar o cadastramento dos documentos de exemplo, deve-se repetir os

passos para os demais documentos, que são: informar processo e sequencial do

evento, “Buscar”, selecionar documento, “Incluir”. Ao fim, os documentos serão

listados (Figura 6). Devem ser cadastrados ao menos três documentos de exemplo.

Nesta lista, há a opção de excluir um documento de exemplo (lembrando que a

opção de excluir irá apenas remover o documento da lista de exemplos do

classificador, não causará nenhum impacto na exibição do documento no processo).

*Figura 5: Detalhe que ilustra a seleção de um documento e a opção de “Incluir”*

*Figura 6: Detalhe da lista de documentos de exemplo e da opção “Salvar”.*


---

![Imagem Imagem_2309](imgs/Imagem_2309.png)

![Imagem Imagem_2310](imgs/Imagem_2310.png)

Por fim, para cadastrar de fato o classificador, deve-se acionar a opção “Salvar”. O

sistema irá exibir uma mensagem de sucesso e passará a listar o classificador recém

cadastrado (Figura 7).

*Figura 7: Confirmação do cadastramento*
<small>É possível cadastrar um classificador por conteúdo de</small><small>três formas diferentes:</small><small>1) informar apenas o “Filtro por Palavras”, ou</small><small>2) ao menos três “Documentos de Exemplo" com alta</small><small>similaridade, ou</small><small>3) ambas as opções em conjunto.</small>
Na listagem dos documentos, além de editar ou excluir, no classificador é possível

cadastrar um filtro dos tipos de documentos que devem ser considerados no

classificador, ao clicar no ícone, conforme figura 7, será mostrada a tela figura 8 que

permite incluir os tipos de documentos que serão considerados, essa mesma opção

de informar os tipos de documentos está disponível no cadastro do classificador por

conteúdo.

Caso não seja informado nenhum tipo de documento, o sistema irá considerar todos

os tipos de documentos ao executa o classificador.

Na figura 8, o sistema apresenta a opção de “Configuração Padrão” ou

“Configuração Manual”, a configuração padrão só irá aparecer se o Tribunal optar

por configurar um conjunto de tipos de documento a serem considerados como

padrão e usados apenas caso não seja cadastrado nenhum tipo de documento de

forma manual.


---

![Imagem Imagem_2311](imgs/Imagem_2311.png)

**3. 3 Criação da regra de automação**

O efetivo uso do classificador por conteúdo somente será dado com a sua utilização

em uma regra de automação de localizadores. Sendo assim, para a criação de uma

regra de automação, o usuário com perfil de diretor de secretaria, ou chefe de

cartório, ou diretor de gabinete/secretaria no 2º grau, deve acessar o item de menu

“Localizadores” > “Automatizar Localizadores do Órgão” ou “Automatização da

Tramitação Processual".

Na tela “Automatizar Tramitação Processual”, deve-se acionar a opção “Novo” (Figura

9). Para o exemplo serão considerados apenas os documentos do tipo “Petição

Inicial”.

![Imagem Imagem_2312](imgs/Imagem_2312.png)

*Figura 8: Tipos documentos de filtro do classificador*

Essa configuração padrão, tem por objetivo evitar que o sistema utilize no

classificador por conteúdo documentos de informações, complementares, tal como

anexos, informações etc.

Para o exemplo serão considerados apenas os documentos do tipo “Petição Inicial”.

*Figura 9: Tela de automação de localizadores*


---

![Imagem Imagem_2313](imgs/Imagem_2313.png)

![Imagem Imagem_2314](imgs/Imagem_2314.png)

![Imagem Imagem_2315](imgs/Imagem_2315.png)

*Figura 10: Regra da automação que utiliza classificador por conteúdo*

No estudo de caso que estamos usando como exemplo neste tutorial, desejamos

criar uma regra de automação para remover do localizador “PETIÇÃO INICIAL” e

incluir um localizador mais específico.

Para tanto, iremos usar o tipo de controle “Por Documento”, sendo o tipo de

documento “Petição Inicial”. Iremos restringir a análise aos processos da classe

“Execução Fiscal” quando a parte autora for a entidade “União – Fazenda Nacional”.

A figura 10 ilustra o preenchimento da regra. Ao final do preenchimento, lembrar de

acionar a opção “Salvar” para persistir a nova regra. Pronto, a regra de automação

que faz uso do classificador por conteúdo está ativa.


---

![Imagem Imagem_2316](imgs/Imagem_2316.png)

*Figura 11: Área de testes classificador por conteúdo*

**4. Área de teste do Classificador por Conteúdo**

Após realizar o cadastro de um Classificador por Conteúdo, o sistema disponibiliza,

na tela Lista de Classificadores, o botão “Área de teste”.

Essa área permite avaliar se para um determinado documento o classificador de

conteúdo irá funcionar corretamente, conforme as regras cadastradas.

Para testar os classificadores, adicione um ou mais arquivos. O sistema irá avaliar a

similaridade entre os arquivos adicionados nesta área em comparação com todos os

classificadores da vara.

Os arquivos utilizados nesta área de teste não serão armazenados no sistema, nem

possuem qualquer influência no funcionamento dos classificadores. É apenas um

teste para indicar a efetividade das regras cadastradas.


---

![Imagem Imagem_2264](imgs/Imagem_2264.png)
**Divisão de Apoio Judiciário****Diretoria de Suporte à Jurisdição de Primeiro Grau****Tribunal de Justiça do Estado de Santa Catarina**<small>SUPORTE</small><small>EPROC</small>
No exemplo da figura 11, a coluna “Similaridade verificada” mostra o resultado do

teste: o arquivo adicionado como documento de teste apresentou 98, 97% de

similaridade com o classificador “Expropriação: Pedido de Extinção Art. 26 - Juízo 1”,

além disso, foi “Classificado pelo filtro por palavras”, por isso, o sistema aponta ele

como “Classificado“ - a cor verde indica que o documento atendeu aos critérios de

classificação por conteúdo e será aplicado na automação de localizadores.

Caso não tenham sido informados documentos de exemplo, apenas filtro por

palavras, nas três colunas “Similaridade verificada”, “Tolerância verificada” e

“Similaridade de modelos” será mostrada a informação “(Sem documentos)”.

A coluna “Similaridade dos modelos” aponta o índice de similaridade entre os

documentos de exemplo previamente cadastrados no respectivo classificador. Ela

não tem relação com o documento de teste.

A coluna “Classificado por filtro por palavras? ”, aponta “(Sim)” se o documento foi

classificado pelo critério cadastrado, indica “(Não)” se não passou pelos filtros

informados e “(Não informado)”, caso não tenha sido informado um filtro por palavras.

Para que o documento seja considerado “Classificado”, precisa atender ao filtro por

palavras, caso esse esteja cadastrado, e também o percentual de similaridade do

documento, em relação aos três ou mais documentos de exemplo, precisa ser maior

que: “Similaridade dos modelos” menos a “Tolerância configurada”.

No exemplo indicado, a similaridade verificada é de 98, 97%, que é maior que 93, 44%

(98, 44% - 5%).
