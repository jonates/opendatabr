# opendatabr

Esse pacote contém bases de dados abertas, maioria do Brasil, a serem utilizadas em diversas aplicacoes no R.

Atualmente disponibiliza 2 conjuntos de dados:

1. ~~ideb_brasil_ensino_medio~~
2. ~~pnud_uf~~

O ~~ideb_brasil_ensino_medio~~ contém como atributo os valores dos indicadores utilizados para o calculo do ideb do ensino médio para o Brasil, como as taxas de aprovações (por série) e as notas da prova SAEB. Conta também com o valor do IDEB e as metas para os anos de 2005, 2007, 2009, 2013, 2015, 2017 e 2019. Também estratifica essas informações pela rede de ensino.

~~~R
#Instale o pacote devtoools caso ainda não tenha instalado
#install.packages(devtools)

#instala o pacote opendatabr
devtools::install_github("jonates/opendatabr")

#carrega a base do ideb do ensino médio do Brasil
df <- opendatabr::ideb_brasil_ensino_medio

#Plot o gráfico do IDEB do Brasil, por ano e por rede de ensino.
ggplot2::ggplot(data = df) +
  geom_point(aes(x=ano,y=IDEB,colour=rede))
~~~

