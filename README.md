# ECHOCHATBOT
COMPANY: CODTECH IT SOLUTIONS

NAME: JOELLE AMBAR

INTERN ID: CT08DN1843

DOMAIN: .NET WEB DEVELOPMENT

DURATION: 8 WEEKS

MENTOR: NEELA SANTHOSH

DESCRIPTION OF THE TASK

I successfully undertook the task of creating and deploying an Echo Bot, a foundational conversational AI project, into the Azure cloud environment. This endeavor served as a comprehensive learning experience, encompassing bot development principles, cloud infrastructure provisioning, and secure identity management within Microsoft Azure.

The initial phase of the project involved acquiring the bot's core codebase. I utilized a standard Echo Bot template, specifically the C# .NET Core version, which is publicly available as part of the Bot Builder Samples on GitHub. This provided a robust and pre-structured foundation, allowing me to concentrate on the deployment and configuration aspects rather than building the bot's logic from scratch. The essential files comprising the bot application included `Program.cs`, which is responsible for setting up the host and logging mechanisms, ensuring the application can run and provide diagnostic insights. `Startup.cs` played a critical role in the bot's architecture by handling dependency injection, configuring the various services necessary for the bot's operation, and establishing the HTTP request pipeline for handling incoming messages. Within `Startup.cs`, key configurations included the registration of `BotFrameworkAuthentication` for managing the bot's credentials and `IBotFrameworkHttpAdapter`, which is crucial for facilitating seamless communication between the bot's logic and the broader Bot Framework service. The `EchoBot.cs` file itself contained the straightforward conversational logic: it is designed to receive any incoming message from the user and simply echo the exact same message back as a reply.

The deployment process to Azure was a multi-stage operation that required careful provisioning and configuration of cloud resources. My first step was to provision an Azure App Service. This service was designated as the hosting environment for the bot's web application, residing within a specific resource group. The App Service provides the necessary infrastructure for running the deployed .NET Core application, handling web requests, and ensuring the bot's continuous availability in the cloud.

Subsequently, an Azure Bot resource was created to act as the primary interface between various communication channels and the deployed App Service. This Azure Bot resource serves as a crucial intermediary, routing messages from channels like Web Chat and Direct Line to the bot's backend logic. During the creation of this Bot resource, it was essential to establish a linkage to an Azure Active Directory (AD) App Registration. This App Registration is fundamental for establishing the bot's identity within Azure and enabling its secure authentication with the Bot Framework service.

A critically important aspect of the entire setup involved the precise configuration of the `MicrosoftAppId` and the associated `MicrosoftAppPassword` (which serves as the client secret) within the App Service's Configuration settings. The `MicrosoftAppId` was set to correspond with the Application (client) ID from the Azure AD App Registration. The `MicrosoftAppPassword` was derived from a client secret generated within the Azure AD App Registration, and it was meticulously entered into the App Service configuration to ensure an exact match. Furthermore, verifying that the "Supported account types" within the App Registration was configured as "Accounts in any organizational directory (Any Azure AD directory - Multitenant) and personal Microsoft accounts" was an essential step to ensure the bot's broad compatibility across different user types. Finally, the messaging endpoint configured for the Azure Bot resource was carefully validated to ensure it pointed precisely to the deployed App Service's `/api/messages` path, which is crucial for correct message routing and communication flow.

A pivotal step in validating the bot's functionality was the utilization of the Bot Framework Emulator. By directly providing the bot's messaging endpoint and authentication credentials to the emulator, I could establish a connection and interact with the deployed bot. This direct interaction confirmed that the bot's internal logic was sound, and its ability to process messages and generate replies was fully functional. The successful operation within the emulator served as a strong indicator that the core bot application was robust and correctly deployed. Following these confirmations, the bot was tested within the Azure Web Chat interface, where it also performed as expected. This systematic approach of deployment, meticulous configuration, and thorough testing ensured the successful operation of the Echo Bot in the Azure cloud environment.

OUTPUT 
<img width="1871" height="823" alt="Image" src="https://github.com/user-attachments/assets/89f418d7-cd49-43cf-9a55-9ded1104e01f" />

<img width="1017" height="771" alt="Image" src="https://github.com/user-attachments/assets/b2d4a5e5-96f6-4335-9d3d-598e3493c003" />

<img width="596" height="747" alt="Image" src="https://github.com/user-attachments/assets/9a9a3cc9-1b4b-446d-96c3-551d6f832a53" />

<img width="999" height="971" alt="Image" src="https://github.com/user-attachments/assets/45588d14-6c46-4157-89c1-3cc3bbc2eb48" />
