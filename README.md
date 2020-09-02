## Description
<p> This Repo describe the architecture used to deploy my auto refreshing portfolio.</p>

## Purpose 
<p>I created this project to have an site that expose automatically all my github projects and have statistics about trafics</p>

## Architecture
<p>This site will be deploy using docker containers with kubernetes or docker compose.</p>
<p>The exact architecture is explained in detail with the schema below (now it is on paper)</p>
<img src="https://via.placeholder.com/350"/>
<p>For the design I can choose between <a href="https://material.angular.io/">Angular Material Design</a> and <a href="https://vaadin.com/learn/tutorials/using-web-components-in-angular">Vaadin design</a></p>
<p>Getting started with <a href="https://www.springboottutorial.com/creating-microservices-with-spring-boot-part-1-getting-started">Spring boot microservice</a></p>
<p>It contains all this different parts (module) </p>
<ul>
    <li>Front-End app using angular <a href="https://github.com/KarLe15/portfolio-site-front">Repo</a></li>
    <li>Dashboard app using angular <a href="https://github.com/KarLe15/portfolio-site-dashboard">Repo</a></li>
    <li>A Broker to dispatch and receive all requests from modules coded with Java with maybe rabbitMQ <a href="https://github.com/KarLe15/portfolio-site-broker">Repo</a></li>
    <li>A logger coded with nodeJS to handle all async I/O (maybe log to firebase) <a href="https://github.com/KarLe15/portfolio-site-logger">Repo</a></li>
    <li>A request interpreter so the front/dashboard will structure-agnostic <a href="https://github.com/KarLe15/portfolio-site-request-interpreter">Repo</a></li>
    <li>Authentification service to generate JWT with validity<a href="https://github.com/KarLe15/portfolio-site-auth">Repo</a></li>
    <li>A github project collector to get all datas from the github account (maybe in Golang) <a href="https://github.com/KarLe15/portfolio-site-github-collector">Repo</a></li>
    <li>A project analyzer to retreive all data requested data with personnal protocol <a href="https://github.com/KarLe15/portfolio-site-project-analyzer">Repo</a></li>
    <li>A stats collector to register all connction and have a precise informations on the most viewed projects <a href="https://github.com/KarLe15/portfolio-site-stats-collector">Repo</a></li>
</ul>


## Todo section:
### chronologic step
#### Logger
<ol>
	<li>Start with the logger (node js) </li>
	<li>Define structure of the API (parameters) </li>
	<li>Define pattern of output log (line or block) content, order ...</li>
	<li>Write async functions to serialize the output to string</li>
	<li>Implement Singloton for the actual logger (one file)</li>
</ol>

#### Github collector
<ol>
	<li>Start to analyze the Github API</li>
	<li>Start with the logger structure (golang) </li>
	<li>Define structure of the API (parameters) </li>
	<li>Define pattern of output result</li>
</ol>

#### Stats collector
<ol>
	<li>Start with the Stats Collector (Maybe with .NETcore) </li>
	<li>Define structure of the API (parameters) </li>
	<li>Define pattern of output result</li>
	<li>Define the Database to use (Firebase, SQL, NoSQL) (most likely NoSQL or Firebase to handle easily the async)</li>
	<li>Implement all method to handle the computing async</li>
</ol>

#### Global Thinking
<p>Think and check if the structure is still correct, if there is components to add/remove.</p>
<p>Think of a way to retreive data (maybe from new component or already existing ones)</p>
<p>Think of the authentification service (is it necessary, how complex it would be ...)</p>
<p>Think of the request interpreter maybe it could be mixed with the broker</p>


#### Github Project Analyzer
<ol>
	<li>Start to define the metadata to use and add to the project</li>
	<li>Choose the technology to implement (Julia, Python, Go ...)</li>
	<li>Define structure of the API (parameters) </li>
	<li>Define pattern of output result</li>
</ol>


#### Broker
<ol>
	<li>Rethink the structure and the purpose of the broker</li>
	<li>Choose the technology to implement (RabbitMQ, Java, Spring, Go ...)</li>
	<li>Define structure of the API (parameters) </li>
	<li>Define pattern of output result</li>
</ol>

#### Dashboard 
<ol>
	<li>Think of the design of the dashboard with Figma (Material design, bootstrap ....)</li>
	<li>Choose the technology to implement (Angular, React, VueJS, VanillaJS ...)</li>
</ol>

#### WebSite 
<ol>
	<li>Think of the design of the Web Site with Figma (Material design, bootstrap ....)</li>
	<li>Choose the technology to implement (Angular, React, VueJS, VanillaJS ...)</li>
</ol>