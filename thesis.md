
ÍNDICE

TODO:
Aim is to understand why gql plus go.
Aim is to build why gql plus go, and how it successfully works.
When building picking up the req - all other thesis
Understanding why go was picked up
Understanding why gql is a successfully solution

Aim is to, light understanding of why gql plus light understanding why go was the opted-in, why it was decided to be open-source, and the successful implementation so we needed build it, why the need to have a gql + go + compat + program schema



rq1. 
rq2. 

Capítulo 1: Introducción	3
Capítulo 2: Planteamiento del Problema	5
2.1 Situación Problemática.	5
2.2 Formulación del Problema.	6
2.3 Justificación de la Investigación.	7
2.4 Objetivos.	8
2.4.1 Objetivo General.	8
2.4.2 Objetivo Específicos.	8
Capítulo 3: Marco Teórico	10
3.1 Antecedentes Internacionales.	10
3.2 Antecedentes Nacionales.	11
3.3 Bases Teóricas.	11
3.4 Definición de Términos.	11
Capítulo 4: Desarrollo del Proyecto	12
4.1. Metodología.	12
4.2 Análisis.	13
4.2.1 Introducción	14
4.2.2 Identificar Tareas	14
4.2.3 Priorizar Tareas	17
4.2.4 Mapear Tareas	17
4.2.5 Alcance.	18
4.2.6 Especificación de Requerimientos.	18
4.2 Diseño.	19
4.3 Arquitectura	19
4.4 Desarollo.	20
4.5 Testeo.	20
4.6 Despliegue.	20
4.7 Artefactos.	21
Capítulo 5: Resultados	21
Conclusiones	22
Recomendaciones	22
Referencias	23


Capítulo 1: Introducción

La presente tesis desarrolla la implementación del proyecto open-source graphql-go que produce varios artefactos principalmente una biblioteca Go, que utiliza GitHub como sistema de control de código y versionamiento, sigue el estándar referencial graphql-js la cuál es una biblioteca open-source construida en JavaScript principalmente sigue la especificación oficial referencial GraphQL.

GraphQL es un protocolo de comunicación, diseñado para comunicar clientes y servidores a través de describir sus capacidades declarativamente usando su propio lenguaje de consultas, mutaciones y subscripciones, sirve para construir sistemas web, idealmente clientes web orientados a la interfaz de usuarios y servidores web.

Es innovador porque soluciona múltiples problemas de protocolos tradicionales, los cuales tienen como principal forma de comunicación centralizar la responsabilidad del lado del servidor web causando problemas de escalabilidad y mantenimiento.

Se logra el objetivo de la tesis a través de cubrir todo el estándar hasta el año 2016, la forma como se verifica que la implementación es funcional es a través de cubrir todos las pruebas de la implementación referencial graphql-js hasta la versión v0.6.0.

El resultado de la tesis es la biblioteca open-source graphql-go, que es usada en muchas empresas de diferentes países y proyectos open-source, causando impacto positivo para poder mejorar la efectividad y eficiencia en la comunicación de clientes-servidores web y creó una referencia estable para otras implementaciones.










Capítulo 2: Planteamiento del Problema
2.1 Situación Problemática.

La forma tradicional de construir software client-server es usando herramientas que permiten su comunicación a través de protocolos tradicionales cómo: RPC[1], SOAP[2], REST[3].

Estas herramientas centralizan el funcionamiento en el servidor, dónde se define con que data se puede interactuar, esta estrategia de comunicación genera varios problemas que son resueltos a demanda con soluciones a demanda.

Múltiples endpoints son creados para poder cubrir diferentes casos de uso lo cuál incrementa la complejidad para poder administrar las peticiones del lado del cliente.

Estos diferentes endpoints causan over-fetching y under-fetching de datos, la consecuencia es que se requiere múltiples peticiones para consolidar la información, ya que el servidor decide que datos enviar por lo tanto los datos recibidos pueden ser mayor o menor a lo esperado.

Una de las principales consecuencias de tener múltiples endpoints es que se crean peticiones anidadas causando complejidad que resulta en el problema conocido cómo: n + 1.

Ineficiencia de mantenibilidad porque cuando se hacen cambios en el servidor impacto en cascada en los diferentes clientes que dependen del servidor por lo tanto los clientes son más propensos a errores.

Problemas de escalabilidad en los servidores porque tienen la responsabilidad de decidir y enviar datos lo cuál causa impacto en la redes asociadas porque más recursos son consumidos principalmente el ancho de banda.

Incremento de costo porque los datos que son envíados desde los servidores requieren más capacidad para poder atender la demanda por lo tanto más aprovisionamiento y recursos son necesarios.

Experiencia de desarrollo limitada porque se requiere muchas herramientas para interactuar con cada uno de los protocolos que usan los servidores causando impacto negativo en integrar nuevos.
Lenta experiencia de desarrollo porque múltiples herramientas son requeridas para interactuar con los diferentes protocolos que crean dificultades al momento de integrar nuevos miembros a los proyectos principalmente curvas de aprendizaje complejas.

Complejidad en las aplicaciones del lado del cliente porque son necesarios múltiples niveles de abstracción para coordinar y re-consolidar la información haciendo que el código sea difícil de mantener porque son necesarios muchas soluciones para mitigar los problemas.

Los protocolos tradicionales causan múltiples formas de manejar el versionamiento de las APIs que tienen como resultado complejidad en el servidor que causan limitada extensibilidad.

2.2 Formulación del Problema.

Problema general

Let’s describe why each research question is important.

¿Por qué desarrollar la implementación del estándar GraphQL en el lenguaje de programación Go, y confirmar su compatibilidad con la implementación referencial graphql-js, y cómo validar su utilidad en empresas de diferentes países y múltiples proyectos open-source ?

Problema específicos

Let’s describe why each research question is important.

¿Qué otras bibliotecas open-source similares existen?

¿Cómo fue la coordinación de la construcción de la biblioteca open-source graphql-go?

¿Qué herramientas se usaron para la construcción de la biblioteca open-source graphql-go?

¿Por qué se decidió que la biblioteca graphql-go sea open-source?

¿Qué fue implementado de la biblioteca open-source graphql-go?

¿Cómo la biblioteca open-source graphql-go fue implementado?

¿Cuánto tiempo tomó construir la biblioteca open-source graphql-go?

¿Qué estrategia se usó para construir la biblioteca open-source graphql-go?

¿Dónde fue presentado y cómo fue aceptado?

¿Cuándo alcanzó la estabilidad y qué implica?

¿Cómo medimos la compatibilidad con la implementación referencial?

¿Qué empresas y proyectos open-source usan la biblioteca open-source graphql-go?

¿Cuál es el impacto positivo en las empresas y proyectos open-source?

¿Cuál es el estado actual del proyecto open-source graphql-go?

¿Cuántas personas colaboraron en la construcción del proyecto open-source graphql-go?

¿Cómo es el mantenimiento del proyecto open-source graphql-go?

2.3 Justificación de la Investigación.

Hernández y Mendoza (2018) la justificación de los argumentos son necesarios y responden a las razones del desarrollo del estudio, la importancia del problema y a quién afecta.

Seguidamente se desarrollan las justificaciones del estudio.


Justificación teórica

Hernández y Mendoza (2018) argumentan que se crea valor cuando se justifica una teoría, el resultado puede ser usado por nuevos investigadores y crear nuevos conceptos.

La investigación justifica la teoría porque implementa la biblioteca inicial del estándar GraphQL en el lenguaje de programación Go, crea valor porque funda las bases para siguientes implementaciones.

Además la investigación es justificada porque la biblioteca es necesaria para resolver problemas modernos en el intercambio de datos entre clientes y servidores.

Justificación práctica

Hernández y Mendoza (2018) argumenta que para justificar la práctica se debe crear valor al resolver uno más problemas reales a través de innovaciones y tecnologías para la calidad de los procesos.


La investigación justifica la práctica porque se crea valor mediante la implementación de la biblioteca GraphQL en el lenguaje de programación Go, a través de pequeñas iteraciones que agregan valor, se usó herramientas de desarrollo modernas.


Justificación social
Hernández y Mendoza (2018) argumenta que la justificación social impacta la sociedad y para los usuarios finales de la investigación
La investigación tiene impacto social porque tiene beneficio en las empresas y proyectos porque el estándar GraphQL es open-source lo cual tiene impacto positivo en términos de usar la biblioteca de manera que no incurra en costos, y se pueda obtener el beneficio de múltiples contribuidores que mejoran la implementación.
Así cómo también permite mejor mantenimiento a largo plazo que podrá ser a prueba de futuro, apalancamiento infinitas mejoras cómo errores y correcciones de seguridad.
2.4 Objetivos.
2.4.1 Objetivo General.

Implementar el estándar GraphQL en el lenguaje de programación Go.

2.4.2 Objetivo Específicos.

Describir los detalles de la implementación del estándar GraphQL en el lenguaje de programación Go, especialmente relacionados a seguir la implementación de referencia: graphql-js.

Describir que la implementación cubra los tests fundamentales de la implementación referencial(graphql-js) hasta la versión v0.6.0.

Describir la utilidad de los usuarios finales y su impacto positivo en empresas y proyectos open-source.

Capítulo 3: Marco Teórico
3.1 Antecedentes Internacionales.

99designs/gqlgen (2016/10/12): Implements a schema based graphql which generates all the components on the server side at build time, the key value is that all the parts are described on the graphql file which contains all the definitions of a type system and from there via using the command line interface commands it generates all the Go code which are: An http/s server, GraphQL endpoint and unit tests, and related development tools such as GraphQL Playground.

The drawbacks being that the Go code is auto-generated, which limits the extensibility, since the code is locked-in and making changes are difficult because it requires core dependency from the upstream project.


graph-gophers/graphql-go (2016/10/12): Implements the GraphQL standard by having as an entry-points the schema as a file, and the types resolvers are defined via code, it is used a library, main advantage being the adoption, also the core is shared across other implementations therefore the benefits are increased by the contributions from the open-source community.

The drawbacks being that the schema is defined at text level which have their limitations in terms of extensibility because it requires extra tooling to maintain the schema source of true.


dosco/graphjin (2019/03/24): Implements the GraphQL standard, being main features the ability to generate the API from a schema that generates the SQL queries, so it is an end-to-end solution similar than a object-relational-mapping, it does support multiple databases, allows end users to just focus on the GraphQL schema side so the Go code is generated, using the API enables to perform queries, mutations and subscriptions.

The drawbacks being that the end-to-end solution locks-in the implementation which is hard to extend, therefore the dependency on having internal hooks exposed and requires strong dependency on the maintainers.
3.2 Antecedentes Nacionales.

(Karla Cecilia Reyes Burgos, 2023) Realizó un estudio titulado: Servicios web con GraphQL: una revisión sistemática de la literatura, el cual detalla la recopilación de fuentes que investigan el uso de GraphQL, y tienen cómo principal objetivo responder las siguientes preguntas:
¿Qué áreas de la ciencia demuestran mayor interés en el desarrollo de servicios web usando GraphQL?
Concluye que la medicina es la mayor área de ciencia interesada y que aplica una implementación de GraphQL.
¿Qué países han demostrado mayor interés en el desarrollo de servicios web
usando GraphQL?
Concluye que el país con mayor interés en aplicar una implementación de GraphQL es Estados Unidos.
¿En qué año se encuentran la mayor cantidad de investigaciones con respecto al desarrollo de servicios web usando GraphQL?
Concluye que el año dónde se realizaron más soluciones informáticas es el 2019.

3.3 Bases Teóricas.
3.4 Definición de Términos.

Rapid Application Development (RAD): A methodology that emphasizes and prioritizes rapid iterations of software development.

Some of the key aspects being:
Prototyping: Leverages testing ideas and collects feedback before creating the final software version.
User Feedback: Focuses on user feedback and continuous iteration of small working parts instead of a strict plan.
Fast turnaround: Benefits the turnaround of the development of the software to pivot making it appealing for developers that are into highly fast paced working environments.

Open-source Development Methodology: A methodology that focuses on collaboration across different numbers of contributors, it is decentralized and in openness development.

Some of the key aspects being:
Peer Review: Continue development of parts that are improved by the community so the risk of errors are reduced as much as possible.

Decentralized Contributors: Development as a decentralized iterations via different tools that the community can leverage for synchronizing all the development workflows without single point of control.

Public Codebase: The source of the project is at a public repository so can be accessed by any contributor to leverage all the benefits that are tied to the license, and the key feature is that security fixes can be addressed.

Rapid Prototyping: Creates the right environment for rapid prototyping of new features, which enables the participation of all the community via the tooling of the source of the code.

Collaboration: Encourages all types of participation which can be from different experiences so the community of contributors are able to participate and learn in different ways.
Capítulo 4: Desarrollo del Proyecto
4.1. Metodología.

The methodologies that were used are:

Rapid Application Development (RAD): We used this methodology in order to implement rapidly iteratively the GraphQL Go implementation following the graphql-js reference:

Prototyping: The GraphQL Go implementation was created from very basic initial interfaces that started from the text source, parser, lexer, AST, collectors and resolver.

User Feedback: As we made progress we received constant feedback that is documented mainly in GitHub, we did not follow a strict plan.

Fast turnaround: We did quick iterations in the implementation because it enabled us to constantly release multiple versions so in order to do so the contributors worked on a fast paced working environment, and also to cover the need of a working version for different companies that leverage the initial versions.


Open-source development methodology: The development of the project was by leveraging the different characteristics of the open-source methodology to have multiple contributors adding value to the project, it is decentralized so the project can be keep forever due to the dependency on GitHub which guarantee durability and also the development was continuously iterated in the openness so any person could benefit from the project from learning, up-to proposing changes.

Peer Review: The project was constantly peer-review by different persons across the planet, and the key part of those besides proposing improvements is that they reported and sent security fixes to keep the project trustable and safe from vulnerabilities.

Decentralized Contributors: The project was iterated and leveraged GitHub as a central control for the development; it enabled multiple contributors from different parts of the planet.

Public Codebase: The project was publicly available since the early stages of development, it allows other contributors to propose security fixes as well as reported bug plus security issues, the license is MIT which matches the reference graphql-js and enables creation of multiple branches of similar projects plus forks with improvements as well as internal forks that require special characteristics that cover inner needs of private projects.

Rapid Prototyping: Since we leveraged GitHub as a central part of the workflow of the project, it enabled rapid iterations of including sets of changes from the graphql-js reference implementation versions.

Collaboration: it enabled different contributors from different parts that learned from the project and they were to add value.
4.2 Análisis.

It was decided to implement the GraphQL standard in Go following the methodologies listed above to have a working initial version and continue iterating from there:
Rapid application development (RAD): From the initial version there was multiple number of iterations that made the library stable:


Prototyping: We have earlier versions that have the implementation work as a prototype which helped us to validate and test main functionalities.

User Feedback: Since we used GitHub as a central main source, there was continued feedback from the community in order to incorporate those.

Fast turnaround: There were multiple pivots on the implementation of the main components with the aim of friendly APIs.

Open-source development methodology: We leveraged GitHub as source of the code, and we used multiple of those features to create the library as a open-source project:


Peer Review: The pull-requests that included new functionality had constantly reviewed to improve the quality and reduce the number of errors.

Decentralized Contributors: We had multiple contributors via GitHub since they were able to review the library and propose improvements and report bugs.

Public Codebase: The library was developed publicly therefore the codebase could be leveraged for different purposes.

Rapid Prototyping: The library was created as continuous iteration via multiple prototypes.
Collaboration: Since GitHub were used, collaboration is the central part of the development with constant collaboration of multiple contributors.
4.2.1 Introducción

The implementation was decided to be built because at the time when the GraphQL standard was released in 2015, and at that time there was no implementation available in the programming language Go, therefore the opportunity to create a Go library for it.

One important highlight is that the standard was released at similar time together with the reference implementation graphql-js, therefore those two artifacts were used to identify the tasks that are part of this section.

The tasks matches the main functionalities of the reference implementation graphql-js, so the main components were the central part of each iteration via pull requests so we could accomplish compatibility at each version level.

4.2.2 Identificar Tareas

The strategy we did in order to find the tasks to create the Go implementation was to port changes matching the versions from graphql-js at component level, some tasks did include changes on multiple components.

Those tasks were delivered using GitHub via pull-requests, besides porting changes there were small incremental improvements.

The following tasks were identified:

Task Name
Components
Description
Pull Requests
Version
Porting changes from graphql-js version 0.4.18.
Errors, languages, types, execution, validation.
Port changes from graphql-js up to the version v0.4.18 which includes the following functionalities:
Consolidate the extension definition outside the type definition.
Make operation name optional.
Compliance with the int sizing based on the specification.
Changes on the function signature of graphql.NewTypeInfo
Enable the possibility of removing the experimental FieldDefFn.
https://github.com/graphql-go/graphql/pull/117 
0.4.18.
Porting changes from graphql-js version 0.5.0.


Port changes from graphql-js up to the version v0.4.18 which includes the following functionalities:
Improvements on introspection related to directive locations.
Improvements in the schema language related to directives.
Consolidates the `getTypeOf` method into the executor component.
Schema changes related to types.
Consolidate arguments including context to executor.
Improvements in types overlapping in rules component.
Add schema definition into language component.
https://github.com/graphql-go/graphql/pull/123 
0.5.0.
Porting changes from graphql-js version 0.6.0.




https://github.com/graphql-go/graphql/pull/192
0.6.0.
Executor




https://github.com/graphql-go/graphql/pull/8 


Source




https://github.com/graphql-go/graphql/pull/5


Visitor




https://github.com/graphql-go/graphql/pull/10 


Printer




https://github.com/graphql-go/graphql/pull/10 


Parser




https://github.com/graphql-go/graphql/pull/2 


Lexer




https://github.com/graphql-go/graphql/pull/3 


AST








Collector








Resolver




https://github.com/graphql-go/graphql/pull/288 


Types




https://github.com/graphql-go/graphql/pull/12 


Errors




https://github.com/graphql-go/graphql/pull/423


CircleCI




https://github.com/graphql-go/graphql/pull/361




4.2.3 Priorizar Tareas

Task priority was based on the iteration of different versions matching the reference implementation, below we list the tasks names along their priority and duration.


Task Name
Priority
Duration
Contributor
Pull Request












4.2.4 Mapear Tareas

Tasks mapping are based on matching the unit tasks against the project thesis requirements, below we list the tasks names against their requirements plus the main implementation components.

Task Name
Requerimientos Funcionales
GraphQL Component
Pull Request










4.2.5 Alcance.

Research goals:
Identify the problems of the traditional client-server protocols.
Implement the GraphQL standard in Go.
Produce a Go open-source library.
Verify the compatibility against the GraphQL reference implementation.
Create the environment for preserving the end-result.

Goals clarifications:
Problems identified were opted-in to consider only the following protocols: 
Implementation limited up-to graphql-js version: 0.6.0.
Specific features were implemented starting from graphql-js version: 0.6.0.



Potential biases identification:
Implementation is committed to open-source.
Standard implementation graphql-js compatible commitment.

Limits of the research:
Limited up-to a graphql-js version 0.6.0 tests suites.
Limited to GraphQL schema programmatically defined.

Not included in this research:
Other type of schema definition strategies such as: Inference from text schema-first.


4.2.6 Especificación de Requerimientos.

Related to how the system behaves at an internal level.
How all different apis of gql behave

Requerimientos funcionales:
Source: Source-in.
Parser: Source to AST and Lexer.
Lexer: Tokenizes the source-in.
AST: The source as a tree.
Collector: Matches AST to resolvers.
Resolver: Produces end-result, meaning the source-out.

Related to the usability, ux of the end-user, at external level.
Requerimientos no funcionales:

Performance:
Usability:
Scalability:
Security:
Maintainability:
Compatibility:
Portability:

Related to the domain category of the type of software, specific to the domain/industry.
Requerimientos de dominio:
GraphQL Standard Spec:
Open-source Standards:
Go Standards:
4.2 Diseño.
What are the internal design of the GraphQL standard, let’s add here diagrams of the workflow, also let’s add each component workflow, prop using uml something like that, also, let’s add GraphQL Playground, GraphQL GraphiQL.

4.3 Arquitectura

query/mutation/subscription as source.
Source: Source-in.
Parser: Source to AST and Lexer.
Lexer: Tokenizes the source-in.
AST: The source as a tree.
Collector: Matches AST to resolvers.
Resolver: Produces end-result, meaning the source-out.

State machine is a representation of a workflow of nodes that produce as an end-result a given state, the nodes that produce the final state can be partial, meaning the paths of the end-result are defined per set.

GraphQL have multiple components that can be represented as a state machine, for example the most important component that are abstracted as:
AST state machine, up-down direction.
Source partial state machine, because one way flow.


4.4 Desarollo.

How is the distribution of the task accomplished ? Let’s add here screenshots of the PRs, maybe a table, let’s break the task into a simpler list and here let’s add more detailed tasks.

Also we could add a taks mapping against the components and linking with the code components in Go down to graphql js components.
4.5 Testeo.

Also let’s add percentage of accomplishing for reaching the desire covering tests results of graphql-js.

Also we are matching the tasks names against the set of unit tests in order to make sure the compatibility against the graphql-js reference implementation.


Task Name
GraphQL JS Unit Test
GraphQL Go Unit Test
Pull Request










4.6 Despliegue.

TODO: Add screenshots of each tool, for main components of gql.

The open-source project was centralized in GitHub, where we leverage different features that enabled the openness of the library, such as:

Comments: 
Pull Requests:
Issues:
Stats:
Documentation:
Releases:
Tags:

Also we had a continuous integration pipeline that guarantees that new functionality was fully tested against all the test suite, we leverage the following both providers: TravisCI and CircleCI.

TravisCI was deprecated in favor of CircleCI due to the latter having more modern functionality that was better for the future proof of the project.

The following features of the continuous integration are in place:
Building:
Per Go version building:




To guarantee that the suite of unit tests matched a high level standard set at a percentage accepted by the open-source community we leveraged Coveralls, and the following features were used:




Besides that we also leverage the Go’s feature “go doc” in order to self document the library

4.7 Artefactos.

End result library at github.


Capítulo 5: Resultados
What was found as part of the research, focused on the main research question ?
What are the research data collected that supports the success of this research, text and numbers end-results ?

Qualitative data:
List of unit tests from reference implementation.

Quantitative data:
Percentage compatibility of unit tests against reference implementation.

Artifacts:
An open-source Go library.
Conclusiones
What are the answers of the secondary questions that are part of the research ?
What are the end results describing that the objectives were successfully accomplished ?

Recomendaciones
What are the recommendations for future related work that is strongly tie to this thesis ?





Referencias

Facebook, Inc. (2019). GraphQL referencia estándar: https://spec.graphql.org/October2021/
GraphQL Spec: https://github.com/graphql/graphql-spec
Official Website: https://graphql-go.github.io/graphql-go.org/
GraphQL Queries as state machine: https://rmosolgo.github.io/ruby/graphql/2016/11/12/graphql-query-as-a-state-machine.html
GraphQL Spec License: https://jointdevelopment.org/
Open Systems Interconnection: https://aws.amazon.com/what-is/osi-model/
REST: https://datatracker.ietf.org/doc/html/rfc7231 
SOAP: https://datatracker.ietf.org/doc/html/rfc4227
RPC: https://datatracker.ietf.org/doc/html/rfc5531 https://datatracker.ietf.org/doc/html/rfc1050


