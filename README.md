## Description
<p> This Repo describe the architecture used to deploy my auto refreshing portfolio.</p>

## Purpose 
<p>I created this project to have an site that expose automatically all my github projects and have statistics about trafics</p>

## Architecture
<p>This site will be deploy using docker containers with kubernetes or docker compose.</p>
<p>The exact architecture is explained in detail with the schema below (now it is on paper)</p>
<img src="https://via.placeholder.com/350"/>
<p>For the design I can choose between <a href="https://material.angular.io/">Angular Material Design</a> and <a href="https://vaadin.com/learn/tutorials/using-web-components-in-angular">Vaadin design</a></p>
<p>Getting started with <a href="https://www.springboottutorial.com/creating-microservices-with-spring-boot-part-1-getting-started">String boot microservice</a></p>
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
