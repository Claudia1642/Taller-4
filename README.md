# Taller-4

## Diego Villaizan, Claudia Garzon

musica <- read_csv("C:\\Users\\HP\\Documents\\songs_normalize (1).csv")
songs_normalize (1)
library(ggplot2)
library(tidyverse)
install.packages("patchwork")
install.packages("gapminder")
library(gapminder)
library(gghighlight)
library(patchwork)
install.packages("gghightlight")
## 1
ggplot(musica, aes(x = danceability , y = valence)) +
  geom_point(color="blue", alpha= 0.3)

## 2

ggplot(musica, aes(x= factor(mode), y= energy))+
  geom_boxplot(aes(color=factor(mode),fill=mode))+
  theme(legend.position = "none")
## 3 
A1 <- ggplot(musica ,aes(x = danceability, y = valence))+
  geom_point(color = "blue", alpha = 0.3)

A2 <- ggplot(musica, aes(x= factor(mode), y= energy))+
  geom_boxplot(aes(color=factor(mode),fill=mode,))+
  theme(legend.position = "none")
(A1 | A2)
