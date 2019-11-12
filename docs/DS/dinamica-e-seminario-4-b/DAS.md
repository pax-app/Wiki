# Documento de Arquitetura de Software

| <td colspan=2>PAX |||
|:-:|:-:|:-:|
| Nome  |E-mail   | Github  |
|  Ésio Gustavo Pereira Freitas | esio.gustavo@gmail.com | @EsioFreitas |
| Fabiana Luiza Vasconcelos Pfeilsticker Ribas | fabianalv.ribas@gmail.com | @FabianaRibas |
| Felipe Campos de Almeida | fepas.unb@gmail.com  | @fepas |
| Gabriel Batista Albino Silva | enggabrielalbino@gmail.com | @gabrielalbino |
| Kaique Henrique de Carvalho Borges  | rique.kaique@gmail.com  | @kaiqueborges |
| Lucas Dutra Ferreira do Nascimento | ldutra98@gmail.com | @lucasdutraf |
| Marcos Nery Borges Júnior | marcosnery.comp@gmail.com | @MarcosNBJ |
| Matheus Figueiredo Pimenta | ultra10vascaino@gmail.com | @Matheusss03 |
| Rogério Silva dos Santos Júnior | junior.rogerio8@gmail.com | @rogerioo |
| Youssef Muhamad Jacob | emaildeyoussefmuhamad@gmail.com | @youssef-md |

> Este documento tem como objetivo registrar a estrutura arquitetural do aplicativo *PAX*, desenvolvido como produto final da disciplina de ADS (Arquitetura e Desenho de Software), no campus do Gama, da Universidade de Brasília.

> O Documento de Arquitetura de Software demonstra o conjunto de visões que pretendem cobrir os aspectos técnicos e estruturais relativos ao desenvolvimento e implantação do sistema *PAX*.



## Histórico de Revisões

| Data  | Versão  | Descrição  | Autor(es)  |
|:-:|:-:|:-:|:-:|
|  08/11/2019 |  1.0 | Inicialização e estruturação do DAS  | Matheus Pimenta  |
|  09/11/2019 |  1.1 | Descrição das visões presentes no DAS  | Matheus Pimenta  |


## Introdução

Projetos desenvolvidos mediante estruturação do *RUP* (*Rational Unified Process*) costumam utilizar o Documento de Arquitetura de Software, dividido em visões, chamada de modelo de visualização 4+1.
Como mostra a imagem acima, as visão contempladas por esse modelo são:

 * Visão de Casos de Uso;
 * Visão Lógica;
 * Visão de Implementação;
 * Visão de Processo;
 * Visão de Implantação;
 * Visão de Dados (opcional).

A *Visão de Dados* é uma etapa optativa introduzida posteriormente para poder aumentar a abrangência e qualidade do documento.

## Requisitos e Restrições Arquiteturais

> Aqui vai ficar a versão mais atualizada do antigo *Documento de Arquitetura* @FabianaRibas e @fepas

| Requisito  | Solução  |
|:-:|:-:|
| Linguagem Front End  |  Flutter |
| Linguagem Back End  |  Flask & Express |
| Plataforma  |   |
| Segurança  |   |
| Persistência (banco)  | PostgreSQL & Firebase  |
| Internacionalização  |   |



## 1. Visão de Casos de Uso

Descrição

> @MarcosNBJ

### 1.1 Lista dos Casos de Uso

Lista resumida com os links dos casos de Uso

### 1.2 Diagrama de Casos de Uso

Diagrama final do Caso de Uso e link da rastreabilidade do mesmo


## 2. Visão Lógica

Descrição

### 2.1 Diagrama de Camadas

> Não sei se será necessário

### 2.2 Diagrama de Pacotes (back e front)

> @Matheusss03 vai fazer

## 3. Visão de Implementação

### 3.1 Diagrama de Classes

> @EsioFreitas @Matheusss03 @gabrielalbino

### 3.2 Diagrama de Sequências

> @Matheusss03

## 4. Visão de Dados (banco)

> @youssef-md e @rogerioo


## 5. Visão de Implantação

### 5.1 Diagrama de Implantação


## 6. Visão de Processos 

### 6.1 Diagrama de Sequencia/Classe focada nos processos existentes

> Está feito @Matheusss03


## 7. Qualidade

### 7.1 NFR (completo com marcadores)

> @youssef-md e @rogerioo

## 8. Referencial Teórico

Philippe Kruchten 1995, "The 4+1 view model of architecture," IEEE Software. 12(6), novembro de 1995.
		A origem das visões 4+1 utilizadas para descrição de arquitetura no RUP. 