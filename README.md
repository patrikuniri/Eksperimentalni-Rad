Instructions how to run benchmark

1. Open a in the directory containing the docker-compose.yml
2. Run the following command to start docker:

	docker-compose up -d

3. Open a new terminal and run the following comands to benchmark:
	
	ab -n 100 -c 1 http://localhost/	- without load balancer
	ab -n 100 -c 10 http://localhost/	- without load balancer
	ab -n 100 -c 1 http://localhost:8080/	- with load balancer
	ab -n 100 -c 10 http://localhost:8080/	- with load balancer

4. When you are done, run the following command to close docker:

	docker-compose down

If any errors, you may need to install Docker and Nginx first.

https://kinsta.com/knowledgebase/install-nginx/     - link on how to install Nginx for all platforms
https://docs.docker.com/desktop/install/windows-install/	- link for Docker Desktop for Windows
