# Sample Developer Application

EchoHeaders is a sample python/django application which reads request headers, and displays the values back to the user.

## Setup the test environment

### Steps

* Run the setup script
`~/tests/05_developer_app/setup.sh`
* Achieve the GOALs
* Run the cleanup script
`~/tests/05_developer_app/cleanup.sh`

## GOALs

All tasks can be completed in `/tmp/05_developer_app/app`

#### Build and Run EchoHeaders Container

* Build the container image
* Run the container image
  * You must be able to CTRL+C out of the container when running it in foreground 
	  * docker -it
* Successfully access the service using `cURL`
* Successfully access the service using your browser

#### Configure the application to use a PostgreSQL database

* Inspect the application source code to determine database requirements
* Update the `docker-compose.yml` spec to support a backend `postgres` database
* Run the container image
* Successfully access the website in your browser

#### Configure the application to test for a database connection before starting

* What approach would you typically use to achieve this?
* Try to implement it
* Run the application container and show how the connection is tested

#### Extra Questions

* Order of Statements in Dockerfile
  * How does the order of statements in the Dockerfile affect the final image ? 
	* What if we moved the ENV stanzas ? Do you think there is a better place in the Dockerfile for them to be ? 


#### What do you notice about the access-logs of the python application
* Implement fixes for any issues you notice
