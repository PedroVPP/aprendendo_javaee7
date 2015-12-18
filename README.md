# aprendendo_javaee7
Repositório para aprender java EE 7

## Java EE Components

Java EE applications are made up of components. A Java EE component is a self-contained functional software unit that is assembled into a Java EE application with its related classes and files and that communicates with other components.

The Java EE specification defines the following Java EE components:

 - Application clients and applets are components that run on the client.

 - Java Servlet, JavaServer Faces, and JavaServer Pages (JSP) technology components are web components that run on the server.

 - EJB components (enterprise beans) are business components that run on the server.

Java EE components are written in the Java programming language and are compiled in the same way as any program in the language. The differences between Java EE components and "standard" Java classes are that Java EE components are assembled into a Java EE application, they are verified to be well formed and in compliance with the Java EE specification, and they are deployed to production, where they are run and managed by the Java EE server.

## Web Components

Java EE web components are either servlets or web pages created using JavaServer Faces technology and/or JSP technology (JSP pages). **Servlets** are Java programming language classes that dynamically process requests and construct responses. **JSP pages** are text-based documents that execute as servlets but allow a more natural approach to creating static content. **JavaServer Faces technology** builds on servlets and JSP technology and provides a user interface component framework for web applications.

Static HTML pages and applets are bundled with web components during application assembly but are not considered web components by the Java EE specification. Server-side utility classes can also be bundled with web components and, like HTML pages, are not considered web components.

## Business Components

Business code, which is logic that solves or meets the needs of a particular business domain such as banking, retail, or finance, is handled by enterprise beans running in either the business tier or the web tier. Figure 1-4 (Business and EIS Tiers) shows how an enterprise bean receives data from client programs, processes it (if necessary), and sends it to the enterprise information system tier for storage. An enterprise bean also retrieves data from storage, processes it (if necessary), and sends it back to the client program.

## Enterprise Information System Tier

The enterprise information system tier handles EIS software and includes enterprise infrastructure systems, such as enterprise resource planning (ERP), mainframe transaction processing, database systems, and other legacy information systems. For example, Java EE application components might need access to enterprise information systems for database connectivity.

## Java EE Containers

Remember when we said that "A Java EE component is a self-contained functional software unit that is assembled into a Java EE application with its related classes and files and that communicates with other components."? Well then, before it can be executed, a web, enterprise bean, or application client component must be assembled into a Java EE module and deployed into its container. The deployment process installs Java EE application components in the Java EE containers. The containers are provided by a Java EE server.

The assembly process involves specifying container settings for each component in the Java EE application and for the Java EE application itself. Container settings customize the underlying support provided by the Java EE server, including such services as security, transaction management, Java Naming and Directory Interface (JNDI) API lookups, and remote connectivity. Here are some of the highlights.

 - The Java EE security model lets you configure a web component or enterprise bean so that system resources are accessed only by authorized users.

 - The Java EE transaction model lets you specify relationships among methods that make up a single transaction so that all methods in one transaction are treated as a single unit.

 - JNDI lookup services provide a unified interface to multiple naming and directory services in the enterprise so that application components can access these services.

 - The Java EE remote connectivity model manages low-level communications between clients and enterprise beans. After an enterprise bean is created, a client invokes methods on it as if it were in the same virtual machine.

Because the Java EE architecture provides configurable services, components within the same application can behave differently based on where they are deployed. For example, an enterprise bean can have security settings that allow it a certain level of access to database data in one production environment and another level of database access in another production environment.

The container also manages nonconfigurable services, such as enterprise bean and servlet lifecycles, database connection resource pooling, data persistence, and access to the Java EE platform APIs

## Container Types

The server and containers are as follows:

 - Java EE server: The runtime portion of a Java EE product. A Java EE server provides EJB and web containers.

 - EJB container: Manages the execution of enterprise beans for Java EE applications. Enterprise beans and their container run on the Java EE server.

 - Web container: Manages the execution of web pages, servlets, and some EJB components for Java EE applications. Web components and their container run on the Java EE server.

 - Application client container: Manages the execution of application client components. Application clients and their container run on the client. 

 - Applet container: Manages the execution of applets. Consists of a web browser and a Java Plug-in running on the client together.

## Java EE Application Assembly and Deployment

A Java EE application is packaged into one or more standard units for deployment to any Java EE platform-compliant system. Each unit contains

 - A functional component or components, such as an enterprise bean, web page, servlet, or applet

 - An optional deployment descriptor that describes its content

Once a Java EE unit has been produced, it is ready to be deployed. Deployment typically involves using a platform's deployment tool to specify location-specific information, such as a list of local users who can access it and the name of the local database. Once deployed on a local platform, the application is ready to run.

[Brief summary of the technologies required by the Java EE platform and the APIs used in Java EE applications](https://docs.oracle.com/javaee/7/tutorial/overview007.htm)

[Java EE 7 APIs in the Java Platform, Standard Edition 7](https://docs.oracle.com/javaee/7/tutorial/overview008.htm)



