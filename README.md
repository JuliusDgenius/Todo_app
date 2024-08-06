A todo list application built with Python and Flask to demonstrate how to
build a RESTful API using flask and python.

This is only a basic app that does nothing much other than provide urls via
which you can query the server and get tasks in the in-memory database, post
a task, update a task and delete a task. It is based on the tutorial
[Designing a RESTful API with Python and Flask](https://blog.miguelgrinberg.com/post/designing-a-restful-api-with-python-and-flask)
by [Miguel Grinberg](https://blog.miguelgrinberg.com/author/Miguel%20Grinberg).

How to Use
Since this is a basic app, you can test it on the command-line using [curl](http://curl.haxx.se/).

First run the program in a terminal like so:\
`python3 app.y`

Once the app is running, open another terminal and issue requests for the url.\
`curl -i http://localhost/todo/api/v1.0/tasks` will retrieve all the tasks available.

`curl -i http://localhost/todo/api/v1.0/tasks/[task_id]`
will get a single task by task id.

`curl -i -X POST -d {"title":"Read a book"} http://localhost/todo/api/v1.0/tasks`\
will create a new task with the title of 'Read a book'. The descritpion can be an empty string.\

`curl -i -X PUT -d {"title":"Do laundry"} http://localhost/todo/api/v1.0/tasks/[task_id]`\
will update the title of a task with the given task id to 'Do laundry'.

`curl -i -X DELETE http://localhost/todo/api/v1.0/tasks/[task_id]`
will delete the task with the given id.
