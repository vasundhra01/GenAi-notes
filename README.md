# FastAPI
Backend: handles logic, authetication, databse, payment, AI processing, security

eg; Google Maps API, OpenAI API, Stripe AI- payments etc
User->Frontend->API->Backend->Database
FastAPI is a framework not a server. Uvicorn is the server
## HTTP protocol
CRUD:
C-Create- POST
R-Read-GET
U-Update- PUT
D- Deletion - DELETE

JSON: JavsScript Object notation-> easy, lightweight, language independent, easy to parse

Flask-> lightweight but more manual work. Lightweight framework of WSGI

Django-> auth+admin panel but heavy, complex

FastAPI-> fast, async, type safety, automation docs-> AI good
uses Python
## async support : ASGI
wsgi- web server gateway interface -- web server(apache/nginx) + python web application (Flask, Django)-- bridge.
one common standard so any python app works with any compatible server
Browser → Web Server → WSGI → Python App
❌ webSockets, live chat, async, streaming
### asgi- async server getway interface-- websockets, async programming, real time apps, 
eg Uvicron
#### *starlet*
ASGI framework/toolkit. lightweight framework for ASGI. extremely fast. async first, minimal
FastAPI internally uses Starlette routing, asyn handling, req/response sys

FastAPI
   ↓
Starlette
   ↓
 ASGI
   ↓
Uvicorn
## WebSockets
comm protocol-> persistent two way/full-duplex connection b/w client and server. HTTP-> connection closes after response. But in webSocket , connection always open, supports real time comm. WhatsApp, stock market, food delivery tracking, live notifs. Initially HTTP-> browser send upgrade req to webSocket
Begins as a HTTP handshake, upgrades to persistent TCP based connection
# automatic validation: pydantic 
-> python lib -> we define a data structure

Pydantic: BaseModel class-> helps define data model-> make sure request/response data adheres to that constraint

response_model: make a class that inherits from baseModel. API attemps to validate response against this.

FastAPI
-> validates data against response_model. ensures data meets the expected structure/types.-> auto converts response data to match structure of pydantic model
-> returns only specified fields.
-> raises validation error to catch issues early
FastAPI validates data against specified pydantic model
helps understand API better
# swagger
automatically creates swagger UI + API docs

{ Postman-> API creation and testing-> server request and response-> limited documentation but good for testing and team collboration. good api collections. QA. automating workflows

Swagger-> better for documentation -> browser based docs and automated api docs. good for design}
{swagger ui-> documentation webpage, swagger editor-> api design tool, actual api standard-> openAPI}
## Client-Server Architecture
Client- request send- browser, frontend, app --> connects to internet
Server- request process - response --> connects to database
## ORM
# Uvicorn
ASGI Server, recieves HTTP requests, execute python code
