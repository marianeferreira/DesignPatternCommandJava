# DesignPatternCommandJava
Implementação do padrão de projeto Command em Java

Comportamental - o padrão de projeto Command O padrão de projeto comportamental tem como foco a maneira como as classes e objetos se comunicam uns com os outros. A ideia central do padrão Command é produzir um maior nível de acoplamento fraco entre as partes envolvidas (leia-se as classes).

Vamos usar um exemplo do mundo real, pedir um prato em um restaurante elegante. O fluxo é: você faz o pedido (comando) ao garçom (quem "invoca" o pedido), que o entregará ao chef (receptor do pedido), para que você possa receber o alimento.

O fluxo da operação do lado técnico é: você faz um comando concreto, que implementa a interface Command, pedindo que o receptor realize uma ação e envia o comando a quem invoca o pedido. Essa é a pessoa que sabe a quem dar esse comando. O chef é o único que sabe o que fazer com o comando/pedido específico. Assim, quando o método "execute" daquele que invoca o pedido é executado, ele, por sua vez, faz com que o método execute dos objetos de comando seja passado ao receptor, completando assim as ações necessárias.

Client faz um Order (pedido) e define o Receiver (Receptor) como sendo o Chef. Order é enviado ao Waiter (Garçom), que saberá quem deve executar o pedido (ou seja, quando dar ao chefe o pedido para que ele o faça). Quando quem invoca o pedido é executado, o método execute de Order é executado no receptor (ou seja, o chef recebe o comando para cozinhar a massa ou para assar o bolo).
