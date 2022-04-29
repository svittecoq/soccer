<!-- Title -->
# Soccer project for Toptal

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#rest-api">REST API</a></li>
    <li><a href="#postman">POSTMAN</a></li>
  </ol>
</details>

<!-- GETTING STARTED -->
# Getting Started

To view this project, visit [Heroku Application](http://sv-soccer.herokuapp.com/).

This application is pre-configured with two users :

## First User :
```
username : test@test.com
password : 123AAaa&
```

## Second User :
```
username : user@test.com
password : 123AAaa&
```

## SignUp New User :

Username
```
Username must be a valid email address
```

Password
```
Password must have 8 characters or more with at least :
1 lower case character
1 upper case character
1 numeric character
1 special character !@#$%&
```

<!-- REST API -->
# REST API
## Sign Up
### Request
```
POST /user
Content-Type: application/json;charset=UTF-8
{
  username : <username>,
  password : <password>
}
```
### Response
```
200 OK
Content-Type: application/json;charset=UTF-8
{
  token : <token>
}
```
## Login
### Request
```
POST /login
Content-Type: application/json;charset=UTF-8
{
  username : <username>,
  password : <password>
}
```
### Response
```
200 OK
Content-Type: application/json;charset=UTF-8
{
  token : <token>
}
```
## Get Team
### Request
```
GET /team[/{teamId}]
Content-Type: application/json;charset=UTF-8
```
### Response
```
200 OK
Content-Type: application/json;charset=UTF-8
{
 teamId      : teamId,
 teamName    : teamName,
 teamCountry : teamCountry,
 teamBalance : teamBalance,
 playerArray : [ player1, player2 ,...]
}
```
## Put Team
### Request
```
PUT /team/{teamId}
Content-Type: application/json;charset=UTF-8
{
 teamId      : <teamId>,
 teamName    : <teamName>,
 teamCountry : <teamCountry>,
}
```
### Response
```
200 OK
Content-Type: application/json;charset=UTF-8
{
 teamId    : teamId,
 error     : "Error message if update team error. Null if OK"
}
```
## Put Player
### Request
```
PUT /player/{playerId}
Content-Type: application/json;charset=UTF-8
{
  playerId            : <playerId>,
  playerFirstName     : <playerFirstName>,
  playerLastName      : <playerLastName>,
  playerCountry       : <playerCountry>,
  playerTransferValue : <playerTransferValue>,
  teamId              : <teamId>
}
```
### Response
```
200 OK
Content-Type: application/json;charset=UTF-8
{
 playerId  : playerId,
 error     : "Error message if update player error. Null if OK"
}
```
## Get Market
### Request
```
GET /market
```
### Response
```
200 OK
Content-Type: application/json;charset=UTF-8
{
 teamArray : [ team1, team 2, ...]
}
```
## Post Transfer
### Request
```
POST /transfer
Content-Type: application/json;charset=UTF-8
{
  playerId : <playerId>,
  teamId   : <teamId>
}
```
### Response
```
200 OK
Content-Type: application/json;charset=UTF-8
{
 teamId    : teamId,
 playerId  : playerId,
 error     : "Error message if transfer error. Null if OK"
}
```

<!-- POSTMAN -->
# Postman

Postman collection available for project.
