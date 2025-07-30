# Sistema de Botão de Pânico \- IFPB 

Este projeto foi desenvolvido por **Alexandre Freitas de Lima Pacheco** e **Robson Luan Fernandes Pereira** para a disciplina de Padrões de Projetos do curso de Engenharia de Computação do IFPB.

### **🚀 Demonstração ao Vivo**

A aplicação está publicada na nuvem e pode ser acessada através do link abaixo:

  https://alexandre-pacheco.github.io/botao-panico/

## **✨ Imagens da Aplicação🎯 Sobre o Projeto**

## 
<img width="1163" height="557" alt="Opera Instantâneo_2025-07-30_030802_alexandre-pacheco github io" src="https://github.com/user-attachments/assets/2095418f-57b7-490f-8399-46e10c86dd9a" />
<img width="997" height="712" alt="Opera Instantâneo_2025-07-30_030841_alexandre-pacheco github io" src="https://github.com/user-attachments/assets/c9e573b8-5e6c-4ad3-94e6-0e2f2d177b4e" />
<img width="1105" height="1275" alt="Opera Instantâneo_2025-07-30_030859_alexandre-pacheco github io" src="https://github.com/user-attachments/assets/e71f1b5c-4a41-442c-8745-c0579d38af50" />
<img width="1076" height="798" alt="Opera Instantâneo_2025-07-30_030918_alexandre-pacheco github io" src="https://github.com/user-attachments/assets/24248114-b660-4572-ad38-b8f4fde420f5" />





O Sistema de Botão de Pânico é uma solução de segurança para a comunidade acadêmica do IFPB. O projeto foi construído utilizando uma arquitetura cliente-servidor moderna para demonstrar a aplicação de padrões de projeto num ambiente realista.

## **🏛️ Arquitetura da Solução**

A aplicação é dividida em duas partes independentes que se comunicam através de uma API REST:

1. **Backend (O "Cérebro"):**  
   * **Tecnologia:** Servidor desenvolvido em **Java** puro, utilizando a biblioteca HttpServer nativa para criar os endpoints da API. O projeto é gerido com **Maven**.  
   * **Responsabilidades:** Contém toda a lógica de negócio, incluindo a implementação dos 9 padrões de projeto, gestão de utilizadores, processamento de alertas de pânico e controlo de estado dos incidentes.  
   * **Alojamento:** Publicado na [Render.com](https://render.com) como um serviço web.  
   * **Repositório:** [**Alexandre-Pacheco/servidor-panico-java**](https://github.com/Alexandre-Pacheco/servidor-panico-java)  
2. **Frontend (A "Interface"):**  
   * **Tecnologia:** Interface de utilizador desenvolvida com **HTML5, Tailwind CSS e JavaScript puro**.  
   * **Responsabilidades:** Apresenta as telas de utilizador e administrador, captura as interações (cliques em botões, preenchimento de formulários) e comunica-se com o backend via fetch para enviar e receber dados.  
   * **Alojamento:** Publicado no [GitHub Pages](https://pages.github.com/).  
   * **Repositório:** [**Alexandre-Pacheco/botao-panico**](https://github.com/Alexandre-Pacheco/botao-panico)

## **🛠️ Padrões de Projeto (Implementados no Backend Java)**

A lógica central do servidor foi construída aplicando 9 padrões de projeto para garantir um código robusto, modular e de fácil manutenção:

| Padrão de Projeto | Onde foi Utilizado | Propósito |
| :---- | :---- | :---- |
| **Singleton** | Na MonitoringCentral para garantir um único ponto de gestão de incidentes. | Assegurar uma instância única para um recurso global. |
| **Factory Method** | Na UserFactory para criar objetos de Aluno e Professor. | Desacoplar a criação de objetos de utilizadores do sistema principal. |
| **Observer** | Para notificar a MonitoringCentral instantaneamente quando um novo alerta é acionado. | Permitir a comunicação em tempo real entre o acionador do alerta e a central. |
| **State** | Para gerir o ciclo de vida de um Incidente (Pendente, Em Atendimento, Resolvido, etc.). | Controlar o comportamento de um objeto conforme o seu estado interno muda. |
| **Strategy** | No LocationProvider, permitindo alternar entre a coleta de localização por GPS ou Wi-Fi. | Tornar algoritmos de localização intercambiáveis e independentes. |
| **Command** | Para encapsular a ação de TriggerAlertCommand (acionar o pânico). | Transformar uma solicitação num objeto, permitindo mais flexibilidade. |
| **Facade** | Na PanicSystemFacade, que serve como ponto de entrada único para todas as requisições da API. | Prover uma interface simplificada para um conjunto complexo de funcionalidades. |
| **Adapter** | No AdminAuthService para simular a adaptação de um sistema de autenticação. | Permitir que interfaces incompatíveis trabalhem juntas. |
| **Builder** | A classe IncidentReportBuilder existe no backend, embora a construção final do relatório seja feita no frontend. | Separar a construção de um objeto complexo da sua representação. |

## **🚀 Como Executar Localmente**

Para executar o projeto no seu ambiente de desenvolvimento, precisa de iniciar o backend e o frontend separadamente.

1. **Executar o Backend (Java):**  
   * Clone o repositório servidor-panico-java.  
   * Abra o projeto numa IDE Java (ex: IntelliJ, Eclipse, VS Code).  
   * Execute a classe principal br.ifpb.pdp.server.MainServer.  
   * O servidor estará a funcionar em http://localhost:8080.  
2. **Executar o Frontend (HTML):**  
   * Clone o repositório botao-panico.  
   * Certifique-se de que a API\_BASE\_URL no ficheiro index.html está a apontar para http://localhost:8080/api.  
   * Abra o ficheiro index.html num navegador web.

## **👨‍💻 Autores**

* **Alexandre Freitas de Lima Pacheco**  
* **Robson Luan Fernandes Pereira**
