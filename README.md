# Jokes App

### Creating The Project
* create repo on GitHub (add gitignore file Java) and copy the GitHub link
* go terminal and cd to projects workplace
* terminal - git clone link from GitHub
* go IDE - new project - Spring Initializer - new project
* change folder to the one where cloned folder located (don't cd to folder - ignore warning)
* choose JAR + maven + check java version
* select dependencies:
    * Spring Web
    * Thymeleaf
* start project and download maven files (if not auto enabled)

### Add Chuck Norris Actuator
* add dependency in POM
  * groupId: guru.springframework
  * artifactId: chuck-norris-for-actuator
  * version: 2.4.0
* reload Maven
* check Maven tab for having chuck-noris-for-actuator in Dependencies (or find it in External libraries)

### Service layer
* create services package
* create interface with method
* create class with implementation to previous interface 
  * add @Service annotation 
  * create private final object from Chuck Noris + create constructor

### Control layer
* create controllers package
* add @Controller annotation 
* create private final interface of service + constructor 
* create String method with args Model model 
* add to method - model.addAttribute("joke", jokeService.getJoke())
* return page, for example "index"
* add annotation to method @RequestMapping({"/", ""})

### View layer
* in templates create index.html (html 5)
* add xmlns:th="http://www.thymeleaf.org" to html tag 
* add to p tag - th:text="${joke}"
* run and go to localhost:8080
