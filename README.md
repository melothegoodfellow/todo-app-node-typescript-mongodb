# todo-app-node-typescript-mongodb

A ToDo app API built with Node, TypeScript and MongoDB.

Functionality

//Authentication

- //register in the app.
	method: POST
	body: {
		email: username@domain.com, //mobile number try later
		password: password,
		confirmPassword: password
	}
	url: /register

- //login in the app.
	method: POST
	body: {
		email: username@domain.com, //mobile number try later
		password: password
	}
	url: /login

- //forgot password
	method: POST
	body: {
		email: username@domain.com, //mobile number try later
	}
	url: /forgot-password

- //reset password
	method: PUT
	body: {
		email: username@domain.com, //mobile number try later,
		newPassword: newPassword,
		confirmNewPassword: confirmNewPassword
	}
	url: /reset-password?via-forgot-password=<hash-value>


//ToDo(CRUD)

- //create ToDo
	method: POST
	body: {
		text: "Wash the dishes",
		done: false
	}
	url: /todo

- //list ToDo
	method: GET
	body: {

	}
	url: /todo

- //list one ToDo
	method: GET
	body: {

	}
	url: /todo/<id>

- //update ToDo
	method: PUT
	body: {
		text: "Wash the dishes", //if only not done.
		done: false
	}
	url: /todo/<id>

- //delete ToDo (if not done)
	method: DELETE
	body: {
	}
	url: /todo/<id>

- //update status of ToDo (done: true | false)
	method: PATCH
	body: {
	}
	url: /todo/<id>