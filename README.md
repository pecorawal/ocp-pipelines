# ocp-pipelines
Openshift Pipelines Sample

## How to use 

There are some use steps indicated to have your Red Hat OpenShift Pipelines works properly.

First we need to define the simple steps to achieve the mostly types of languages in a simple way of manner.

Each app has your own directory with respective pipelines for CI.

## Pipeline 

The initial step is to understand how pipeline yaml structure works and how is the main steps to get the most simple way build an app.

Below is an ASCII diagram which can be used as blueprint reference for most os cases.

+----------------+       +-------------------+       +-----------------------+       +--------------------------+       +------------------+
|   Fetch-Repo   | ----> |     App Build     | ----> | App Push to Registry  | ----> | Add Version Tag to Git   | ----> |     App Deploy   |
| (Clonar Código)|       | (Construir Imagem)|       | (Empurrar para Reg.)  |       | (Adicionar Tag de Versão)|       | (Implantar App)  |
+----------------+       +-------------------+       +-----------------------+       +--------------------------+       +------------------+
        ^                                                                                                                         ^
        |                                                                                                                         |
        +-------------------------------------------------------------------------------------------------------------------------+
                                        (Fluxo de Dados: Código-Fonte, Imagem Construída, Tag de Versão)