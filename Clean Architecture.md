**Clean Architecture** é uma abordagem de design de software proposta por ==Robert C. Martin==, também conhecido como ==%% Uncle Bob %%==, que visa organizar o código de forma a promover manutenibilidade, testabilidade e flexibilidade, separando claramente as responsabilidades em camadas concêntricas. 

O princípio central é o desacoplamento da lógica de negócios do sistema de influências externas, como interfaces de usuário, bancos de dados e frameworks, garantindo que as dependências sigam uma direção unidirecional, com camadas externas dependendo das internas, mas não o contrário.

 A arquitetura é fundamentada em princípios como a inversão de dependências, a separação de preocupações e a facilidade de testes, permitindo que mudanças em tecnologias externas, como bancos de dados ou interfaces, não afetem o núcleo do sistema. 
 
 Apesar dos benefícios, sua implementação pode gerar complexidade desnecessária se aplicada de forma rígida, especialmente em projetos pequenos, o que exige uma abordagem pragmática e equilibrada.

A estrutura proposta pela arquitetura ocorre em camadas separadas, sendo elas respectivamente:
- [[Domain]]
- [[Infrastructure]]
- [[Application]]
- [[Presentation]]

Cada uma dessas camadas possui suas próprias regras internas de comunicação e organização, podemos ver de forma simples e visual no [[Diagrama Clean Architecture.canvas|Diagrama Clean Architecture]] quem depende de quem, mas reforçando:
-  [[Domain]] não conhece nenhuma das camadas, apenas a si mesma.
-  [[Application]] conhece apenas [[Domain]].
-  [[Infrastructure]] conhece apenas [[Domain]] e [[Application]].
-  [[Presentation]] conhece apenas [[Application]].