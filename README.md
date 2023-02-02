# Permissions & Postgresql

## Features Tasks and Requirements

General

- You have been supplied with two demos, each presenting a key new feature.
  - blogapi-permissions demonstrates how to restrict access to portions of your APIs data.
  - blogapi-postgres demonstrates switching over to using postgres vs sqlite
- Your job is to merge the functionality of both demos.
- Customize your project to use different application features/models than Blog and Post

Django REST Framework

- Make your site a DRF powered API as you did in previous lab.
- Adjust project's permissions so that only authenticated user's have access to API.
- Add a custom permission so that only author of blog post can update or delete it.
- Add ability to switch user's directly from browsable API.

Docker

- NOTE Refer to demo for built out Dockerfile and docker-compose.yml examples.
- create Dockerfile based off python:3.11-slim
- create docker-compose.yml to run Django app as a web service.
- enter docker-compose up --build to start your site.
- add postgres 11 as a service
  - Note: It is not required to include a volume so that data can persist when container is shut down.

- Go to browsable api and confirm site properly restricts users based on their permissions.

Thunder Client

- Used Thunder client to implement status Response to show OK 200
- POST 127.0.0.1:8000/api/token/
- JSON Body include "username" and "password"
- response:

    {
  "refresh": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoicmVmcmVzaCIsImV4cCI6MTY3NTM4NTY2OSwiaWF0IjoxNjc1Mjk5MjY5LCJqdGkiOiI1OWE5YzZiNWUzZjE0NjZmOWEzZWRkN2Q4MTQ5ZWNjOSIsInVzZXJfaWQiOjF9.URT9BD8s-WE1FGROSRUyHVhsJar4FSVzcpoDZwcWRjU",
  "access": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNjc1Mjk5NTY5LCJpYXQiOjE2NzUyOTkyNjksImp0aSI6ImI1ZTMxZTk2NTM3ZjQyY2ZiN2U1NGMzZDhmODE2NmQ1IiwidXNlcl9pZCI6MX0.VkMARS9FNjndNu-_Of81vgAm2tu4fYIUmbt3cOJHHAE"
}
