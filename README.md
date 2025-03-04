required plugins : 

Pipeline stage view  --> Enhance the visibility.
AnsiColor
Pipeline Utility Steps --> for reading json file / Zip the files
Nexus Artifact Uploader
Rebuild --> Enables users to rebuild a previous Jenkins job with the same parameters, making reruns quick and efficient.
sonarqube scanner

CI -- uplaoding artifact to Nexus

Nexus :
------
ubuntu OS user name is ubuntu
we must give a key-pair for this to login
wait for 5min to complete setup

public-ip:8081 --> to access 
sign in
default user name --> admin 

Configure AWS cred in Jenkins agent to connect with AWS for backend-deploy job

Maven type artifact:
-----------------------
to identify easly 
group id --> com.expense
artifact id --> backend 
1.0.0 --> version 

http://public_ip:8081/repository/backend/  session 45 (from 20 mins)

CI - up steam job
CD - down stream job

SonarQube:
------------------
need sonarqube plugin

Manage jenkins → tools → add sonarQube scanner → like sonar installing on agent 

Manage jenkins  → system → sonarqube installations → server url e.g http://public_ip:9000/
Name at tools and system should same.
Sonarqube → myaccount → token → for authentication 

Quality Gate:
—---------------
New code → difference between the previous code - present code 

Overall code → code from starting - always prefer quality gate setting on overall code.

Code coverage → unit test write by developers to test the functions → if code have 10 functions → 100% coverage 
Critical issues → 0
Security rating → A
Vulnerabilities → 0

Webhook:
----------

In git - repo → settings → webhook → http://jenkins.hellandhaven.xyz:8080/github-webhook/
In sonar → administration →  configure →  webhook →  http://jenkins.hellandhaven.xyz:8080/sonarqube-webhook/






