# Quizzy
`Quizzy` is a proof-of-concept for a quiz taking platform, similar to Sporcle or Buzzfeed. This is the final project for CS3200 Database Design at Northeastern University with group members Meredith Scott, Jenna Sigman, and Nicole Sorial. Users can take quizzes and see some statistics, and quiz writers can upload, edit, and delete quizzes, as well as view aggregated statistics for quizzes they have written

Link to video: www.youtube.com/watch?v=mcXT-ZRPsHg&ab_channel=MeredithScott

## Disclaimer
Not all of the features of this app are fully functional. Specifically, as there is no proper backend server, the statistics-related operations do not work as well as one would hope, as there isn't a set way to update them (the data aggregates very quickly and it would be very expensive to maintain on a per transaction basis -- we would likely opt for a nightly operation that updates all the quiz statistics in bulk). Rather, as the app stands now, it displays the statistics as they are in the database at time of data generation. In a future iteration of the project, we would add improved handling to this data on the server side.

# MySQL + Flask Boilerplate Project

This repo contains a boilerplate setup for spinning up 3 Docker containers: 
1. A MySQL 8 container
1. A Python Flask container with a REST API implementation
1. A Local AppSmith Server, the repo for which can be found (here)[https://github.com/nicolesorial/quizzy-appsmith]

## How to setup and start the containers
**Important** - you need Docker Desktop installed

1. Clone this repository.  
1. Create a file named `db_root_password.txt` in the `secrets/` folder and put inside of it the root password for MySQL. 
1. Create a file named `db_password.txt` in the `secrets/` folder and put inside of it the password you want to use for the a non-root user named webapp. 
1. In a terminal or command prompt, navigate to the folder with the `docker-compose.yml` file.  
1. Build the images with `docker compose build`
1. Start the containers with `docker compose up`.  To run in detached mode, run `docker compose up -d`. 




