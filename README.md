# ForgetmeNot

Microservice based web app for a University Course made in 2 person team.
The idea is quite simple. Users provide links to their calendars and state how long before events they would like reminder to be displayed.
There are 3 microservices and a frontend. 
* frontend (my responsibility) - not too complicated frontend with basic react and mui.
* reminders (my responsibility) - keeps the reminder messages that the user should have displayed and provides an api to manage those reminders
* calendars (teammate's responsiiblity) - main responsibility is to store calendar's links and periodically check if any reminders should be added
* users (teammate's responsibility) - manages sessions and tokens/logins

We used varnish as a loadbalancer and redis for a fast cache. Everything is set up to work with docker compose.

## Running locally
To run locally simply move to the main directory and run
`docker compose up -d`
After a while, the site should be running on `http://localhost:3000`.