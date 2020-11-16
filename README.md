## Maven - multi module project
- Create a maven multi module project in28minutes: https://www.youtube.com/watch?v=zVwUy08SFnA
- in28minutes GitHub multi-module project: https://github.com/in28minutes/MavenIn28Minutes/tree/master/3.multi-module-maven-project
- Using a War Dependency in Maven: https://www.damirscorner.com/blog/posts/20190614-UsingAWarDependencyInMaven.html
- Using a WAR module as dependency in Maven: https://pragmaticintegrator.wordpress.com/2010/10/22/using-a-war-module-as-dependency-in-maven/
- Dependency Management and Versioning With a Maven Multi-Module Project: https://dzone.com/articles/maven-multi-module-project-with-versioning
- Maven 3: Overlay is not a dependency of the project: https://stackoverflow.com/questions/22014671/maven-3-overlay-is-not-a-dependency-of-the-project

### General Concept of Project in Multi modules  
1. Create an application with packaging: pom. This project is just a placeholder for dependencies and will be used as a parent pom. We will refer to this project as {parent-project}.
2. Create a JSF application that contains only the common template that all our web apps will need. This project will have packaging: war. Also it will contain tag <parent> that refers to the {parent-project}. We will refer to this project as {jsf-template-project}.
3. Create other web applications that will use the above template. They will declare as <parent> the {parent-project} and will declare the {jsf-template-project} as dependency of <type> war </type>. 
4. Overlays can be used to customize the war dependency and include or exclude files...
