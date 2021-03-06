# Simple_Auth_API

Simple Auth API  Build With  <a href="https://www.tornadoweb.org/en/stable/">Tornado</a>  Framework For Handling Authentication Process With Session ID Also Called a Transient Cookie

---------------------------------------

# setup:
<table>
<tr>
<td> 1)  git clone https://github.com/MedAmineFouzai/Simple_Auth_API </td>
</tr>
<tr>
<td> 2) cd Simple_Auth_API</td>
</tr>
<tr>
<td> 3) pip install pipenv</td>
</tr>
</tr>
<td> 4) pipenv --python 3.6</td>
</tr>
<tr>
<td> 5) pipenv install - r requirements.txt</td>
</tr>
<tr>
  <td>
    6) run project with <a href="https://pypi.org/project/torn/">torn cli</a> : <b>#command: [ torn run ] </b>  </td>
 </tr>
</table>

---------------------------------------


"Session" is the term used to refer to a user's time browsing a web site. It's meant to represent the time between their first arrival at a page in the site until the time they stop using the site


![](https://github.com/MedAmineFouzai/Simple_Auth_API/blob/master/Captures/easy.jpg)


---------------------------------------

# Usage:

the best way to understand things is to keep it simple and clear and implemente the problem or the concept in a native way  before using any tool or a thrid party libery or a framework .


the server has 3 end points [ /signup , /login , /logout ]:


### Requesting: [http://localhost:8000/signup](http://localhost:8000/signup)

 in JSON : 
      
      {
        "name":"example"
        "email"="example@gmail.com,
        "password":"example"
      }


in url arguments : http://localhost:8000/signup?name=example&email=example@gmail.com&password=example

Response well be a user object like this :
     
      {  
      "_id": {
       "$oid": "5ec0cc38b8ea4c1f03037e85"
       }, 
      "name": "UserExample", 
      "email": "example@gmail.com", 
      "password":"50d858e0985ecc7f60418aaf0cc5ab587f42c2570a884095a9e8ccacd0f6545c", 
      "SessionID": "ca31c9da-878f-4b8e-8480-4ed68c5c581d"}
      }

### Requesting: [http://localhost:8000/login](http://localhost:8000/login)

the same data as /signup except the name field
both endpoint well return the same resualt wich is a user object with a SessionID from Database 


---------------------------------

### Requesting: [http://localhost:8000/logout](http://localhost:8000/logout)

this end point will clear all cookies and reset every thing 

![](https://github.com/MedAmineFouzai/Simple_Auth_API/blob/master/Captures/Capture.PNG)


