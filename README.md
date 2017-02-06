<h2>Spring 4 Annotation based + Spring Security + Spring Oauth2 </h2>

In this project, I have implemented  spring4  Annotation based + spring security + Spring oauth2 integration.

I have created sample project, Just need to import in Eclipse or STS.

This is a maven based project so build this project & run it on JBOSS/EAP.

Thanks to websystique. 
Source : http://websystique.com/spring-security/secure-spring-rest-api-using-oauth2/

<h4>Running the application </h4>
Run it and test it using two different clients.

Client 1: Postman

Try to access a resource without any auth info, wil get a 401.

Endpoints and their purpose

Attempt to access resources [REST API] without any authorization [will fail of-course].<br/>
GET http://localhost:8080/SpringSecurityOAuth2Example/user/ 
<br/>
Ask for tokens[access+refresh] using HTTP POST on /oauth/token, with grant_type=password,and resource owners credentials as req-params. Additionally, send client credentials in Authorization header.<br/>
POST http://localhost:8080/SpringSecurityOAuth2Example/oauth/token?grant_type=password&username=bill&password=abc123 
<br/>
Ask for a new access token via valid refresh-token, using HTTP POST on /oauth/token, with grant_type=refresh_token,and sending actual refresh token. Additionally, send client credentials in Authorization header.<br/>
POST http://localhost:8080/SpringSecurityOAuth2Example/oauth/token?grant_type=refresh_token&refresh_token=094b7d23-973f-4cc1-83ad-8ffd43de1845 
<br/>
Access the resource by providing an access token using access_token query param with request.<br/>
GET http://localhost:8080/SpringSecurityOAuth2Example/user/?access_token=3525d0e4-d881-49e7-9f91-bcfd18259109 
<br/>
