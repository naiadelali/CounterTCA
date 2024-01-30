# Projeto de Estudo: Contador com Arquitetura Componível (TCA)

Este projeto é um estudo prático da Arquitetura Componível (The Composable Architecture - TCA), aplicado a um exemplo simples de contador. O TCA é uma abordagem para construção de aplicativos em Swift que promove uma arquitetura mais modular, testável e manutenível.

## Imagem 
![](https://github.com/naiadelali/CounterTCA/blob/master/diagram.png?raw=true)

## Sobre o TCA

A Arquitetura Componível é uma estrutura que ajuda a organizar a lógica de negócios e o estado de um aplicativo de maneira previsível e fácil de entender. Ela se baseia em três conceitos principais:

1. **State (Estado)**: Representa o estado da aplicação ou de uma parte dela. No nosso caso, inclui variáveis como `count`, `fact`, `isLoading` e `isTimerRunning`.

2. **Action (Ação)**: Define as ações que podem ocorrer na aplicação, como incrementar e decrementar o contador, iniciar ou parar um timer e solicitar fatos numéricos.

3. **Reducer**: Uma função pura que recebe o estado atual e uma ação, e retorna um novo estado. É aqui que a lógica de negócios é implementada.

## Funcionalidades do Projeto

O projeto consiste em uma interface simples de contador com as seguintes funcionalidades:

- **Incrementar e Decrementar**: O usuário pode aumentar ou diminuir o valor do contador.
- **Solicitar Fatos Numéricos**: Ao tocar em um botão, o aplicativo faz uma solicitação de rede para obter um fato interessante sobre o número atual do contador.
- **Timer**: Um timer que, quando iniciado, incrementa automaticamente o contador a cada segundo.

## Estrutura do Projeto

O projeto é estruturado em torno do TCA, com cada parte da aplicação claramente definida:

- **CounterFeature**: Contém a lógica do contador, incluindo o estado, as ações e o reducer.
- **CounterView**: A interface do usuário que interage com o `Store` do TCA para enviar ações e mostrar as mudanças de estado.
- **Effects**: Utilizados para lidar com operações assíncronas, como solicitações de rede e o timer.

## Como Executar

Para executar o projeto, você precisará do Xcode e do Swift. Clone o repositório, abra o projeto no Xcode e execute-o em um simulador ou dispositivo.

## Conclusão

Este projeto de estudo oferece uma visão prática de como a Arquitetura Componível pode ser utilizada para construir aplicativos Swift de forma modular e testável. Ele demonstra a separação clara entre lógica de negócios, estado da aplicação e interface do usuário, facilitando a manutenção e expansão do código.