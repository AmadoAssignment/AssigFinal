# AssigFinal
/*
Assumptions:
1- client and the servers are from same company So i use: resource owner credentials grant type instead of authorization code, implicit, client credentials
2- HTTPS
3- Access token valid for 3 minutes and refresh token valid for 1 hour
4- Resuorse is a Object called User which has: id, name, age, and salary, to test the intraction with different type of requests like: get, post, put and delete.



Attempt to access resources [REST API] without any authorization [will fail of-course].
GET http://localhost:8080/SpringSecurityOAuth2Example/user/

Ask for tokens[access+refresh] using HTTP POST on /oauth/token, with grant_type=password,and resource owners credentials as req-params. 
Additionally, send client credentials in Authorization header.
POST http://localhost:8080/SpringSecurityOAuth2Example/oauth/token?grant_type=password&username=bill&password=abc123

Ask for a new access token via valid refresh-token, using HTTP POST on /oauth/token, with grant_type=refresh_token,and sending actual refresh token. Additionally, send client credentials in Authorization header.
POST http://localhost:8080/SpringSecurityOAuth2Example/oauth/token?grant_type=refresh_token&refresh_token=

Access the resource by providing an access token using access_token query param with request.
GET http://localhost:8080/SpringSecurityOAuth2Example/user/?access_token=
GET http://localhost:8080/SpringSecurityOAuth2Example/user/1?access_token=
DELETE http://localhost:8080/SpringSecurityOAuth2Example/user/1?access_token=

<DefaultOAuth2AccessToken xmlns="">
    <access_token>7869134d-b229-4f86-ab96-813a695cbd28</access_token>
    <token_type>bearer</token_type>
    <refresh_token>d21e9e79-8d29-4686-a891-80e1ecd44876</refresh_token>
    <expires_in>179</expires_in>
    <scope>read write trust</scope>
</DefaultOAuth2AccessToken>






*/
