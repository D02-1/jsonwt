### Authentication

Our app works well up until now but it's not secure at all at the moment. Anybody can delete another users account using their id, passwords are not hashed so they are easy to be compromised and there is no authentication taking place anywhere. We will set up a way to authenticate each call using Json Web Tokens, so each user can manage only information created by them. We will also introduce roles for our users. We will have an admin role and a client role and their priviledges should be like the following:

Admin Role

Records
POST/GET/PUT/DELETE.
Users
POST/GET/PUT/DELETE.
Orders
POST/GET/PUT/DELETE.
Client Role

Records
GET.
Users
POST/GET/PUT/DELETE.
Orders
POST/GET/PUT/DELETE.
TODO

Return a token everytime a user is created.
Write a middleware to authenticate all endpoints of our app using the token above.
Hash the password while user creation and login.
Write a middleware that will validate users based on their roles.
