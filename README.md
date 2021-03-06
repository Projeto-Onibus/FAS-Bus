# FAS-Bus: Fleet Analysis Sistem

The FAS-Bus application is an system that collect, store, correct and display statistical data related to the city of Rio de Janeiro's bus fleet. It's is an example of a *FAS* (*Fleet Analysis System*) implementation. *FAS* stores, correct and exibit statistical data of an IoT-Integrated fleet with constant GPS monitoring. It's main objective is to correct the IoT generated data using GPU acceletation and distributed processing in order to provide better fleet analysis.

## Base do sistema

O sistema é composto de 5 containers responsáveis por diferentes tarefas, são eles:
* [Database](https://github.com): Possui a engine [PostgreSQL](https://www.postgresql.org/) para gerenciar o banco de dados, já configurada para inicializar com a estrutura e funções necessárias.
* [Insertion](): Container que faz a coleta dos dados por minuto de uma origem (no caso, da API da prefeitura) e envia os dados diariamente ao banco de dados, depois de seu devido pré-processamento.
* [Processing](): Container opcional que tem o 

## Pré-requisitos

Toda máquina em que se pretende rodar o sistema deve ser linux e instalar o Docker para execução dos containers.

* Processing:
    * Placa de vídeo da NVIDIA compatível com CUDA
    * Drivers NVIDIA compatíveis
    * Instalação do [Container toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html#docker) da NVIDIA.
    
* Database:
    * (Recomendação) Montar arquivos do banco de dados em um SSD NVMe.


## Instalação

Para fazer a instalação do sistema 