# opendatabr

Esse pacote contém bases de dados abertas, maioria do Brasil, a serem utilizadas em diversas aplicacoes no R.

~~~R
#Instale o pacote devtoools caso ainda não tenha instalado
#install.packages(devtools)

#instala o pacote opendatabr
devtools::install_github("jonates/opendatabr")
library(ggplot2)

#carrega a base do ideb do ensino médio do Brasil
df <- opendatabr::ideb_brasil_ensino_medio

#Plot o gráfico do IDEB do Brasil, por ano e por rede de ensino.
ggplot2::ggplot(data = df) +
  geom_point(aes(x=ano,y=IDEB,colour=rede))
~~~

