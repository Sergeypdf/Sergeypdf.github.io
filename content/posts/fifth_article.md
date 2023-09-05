title: How Flask handles requests
date: 2022-06-17
description: Routing in Flask and the route decorator
tag: flask
project: Course on Flask for beginners
platform: Flask Workshop
link: https://www.coursera.org/projects/python-flask

How does Flask know what function to display when it receives a request from the client?

Flask maps the URL and render functions to be rendered. The mapping definition (routing) is created using the route decorator or the add_url_rule() method on a Flask instance. These mappings can be accessed using the url_map attribute on the Flask instance.

	>>>
	>>> from main2 import app
	>>> app.url_map
	Map([<Rule '/' (OPTIONS, GET, HEAD) -> index>,
	 <Rule '/static/<filename>' (OPTIONS, GET, HEAD) ->  static>,
	 <Rule '/books/<genre>' (OPTIONS, GET, HEAD) ->  books>,
	 <Rule '/user/<user_id>' (OPTIONS, GET, HEAD) ->  user_profile>])
	>>>

As you can see, there are 4 rules. Flask defines URL matches in the following format:

	url pattern, (comma separated list of HTTP methods handled by the route) -> view function to execute

Path /static/<filename> automatically added for Flask static files. Working with static files will be discussed in a separate lesson "Serving static files in Flask".