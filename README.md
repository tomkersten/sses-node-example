Server-Sent Events (SSEs), Node.js (Express.js), and Redis
==========================================================

This is an example application demonstrating one way to approach
delivering Server-Sent Events with Node.js (leveraging Express.js).

The application accompanies a blog post at:
[http://tomkersten.com/articles/server-sent-events-with-node/](http://tomkersten.com/articles/server-sent-events-with-node/)

Requirements
------------

1. Redis
1. Node.js
1. Express.js

Using it...
-----------

1. Clone the repo locally
1. cd into the cloned directory and run `node app.js`
1. Visit http://localhost:8000/ in one browser window (Page A)
1. Open another window and visit http://localhost:8000/fire-event/anything-you-want-here (Page B)
1. Look at 'Page A' again...and you should see a message including the name of the page you
   visited ('anything-you-want-here')
   1. Additionally, if you open up `redis-cli` and issue `PUBLISH updates 'some message here'`, you should see your message show up as well.
