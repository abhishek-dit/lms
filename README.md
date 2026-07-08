<div align="center" markdown="1">

<h1>Ace It Up</h1>

**Easy to use Learning Management System**

</div>

## Ace It Up

Ace It Up is an easy-to-use learning system that helps you bring structure to your content. It is a whitelabeled fork of [Frappe Learning](https://github.com/frappe/lms), licensed under AGPL-3.0.

### Key Features

- **Structured Learning**: Design a course with a 3-level hierarchy, where your courses have chapters and you can group your lessons within these chapters. This ensures that the context of the lesson is set by the chapter.

- **Live Classes**: Group learners into batches based on courses and duration. You can then create Zoom live class for these batches right from the app. Learners get to see the list of live classes they have to take as a part of this batch.

- **Quizzes and Assignments**: Create quizzes where questions can have single-choice, multiple-choice options, or can be open ended. Instructors can also add assignments which learners can submit as PDF's or Documents.

- **Getting Certified**: Once a learner has completed the course or batch, you can grant them a certificate. The app provides an inbuilt certificate template. You can use this or else create a template of your own and use that instead.

### Under the Hood

- [**Frappe Framework**](https://github.com/frappe/frappe): A full-stack web application framework.

- [**Frappe UI**](https://github.com/frappe/frappe-ui): A Vue-based UI library, to provide a modern user interface.

## Development Setup

### Docker

You need Docker, docker-compose and git setup on your machine. Refer [Docker documentation](https://docs.docker.com/). After that, follow below steps (using the local `docker/` directory of this repo):

**Step 1**: Setup and run the container

    cd docker
    docker compose up -d

**Step 2**: The site [http://lms.localhost:8000/lms](http://lms.localhost:8000/lms) should now be available. The default credentials are:
- Username: Administrator
- Password: admin

### Local

To setup the repository locally follow the steps mentioned below:

1. Install bench and setup a `frappe-bench` directory by following the [Installation Steps](https://frappeframework.com/docs/user/en/installation)
1. Start the server by running
	```sh
	$ bench start
	```
1. In a separate terminal window, run the following commands (replace the `get-app` URL with your fork's git URL).
	```sh
	$ bench new-site aceitup.test
 	$ bench --site aceitup.test add-to-hosts
 	$ bench get-app https://github.com/frappe/payments
 	$ bench get-app https://github.com/abhishek-dit/lms
 	$ bench --site aceitup.test install-app lms
	```
1. Now open the URL `http://aceitup.test:8000/lms` in your browser, you should see the app running

## Attribution & License

This project is a fork of [Frappe Learning](https://github.com/frappe/lms) by Frappe Technologies Pvt Ltd, and remains licensed under the [GNU AGPL-3.0](license.txt). Source code for any modifications must be made available under the same license.
