
# [ST2SAS] - Docker Containers

## TP_1
### 1.1
* Easy to Change: You can change variables without rebuilding the image.
* More Secure: Sensitive info (like passwords) stays safe.
* Cleaner: The Dockerfile stays simple.
* Flexible: You can use different settings for different environments.
### 1.2
* Keeps Data Safe: Without it, your data is lost if the container stops.
* Easier Backup: You can back up and restore your data easily.
* Better Performance: Volumes give faster access to data.
* Easy Updates: You can update the container without losing data.
### 1.4
* Smaller image: It keeps only the necessary files in the final image (no build tools or extra files).
* Separation: It separates the build process from the runtime environment.
* Faster builds: Docker caches steps, so rebuilding is quicker if nothing changes.
### 1.5
* Load Balancing: It spreads traffic across multiple servers to prevent overloading one server.
* Security: It hides your backend servers from the outside world, protecting them from attacks.
* SSL Termination: It handles secure connections (HTTPS), so your servers don’t have to.
* Authentication: It can manage logins and access control before letting users reach your services.
* Caching: It stores frequently used data to make requests faster.
* Easier Setup: It lets you manage multiple services under one domain.
### 1.6
* Easier Management: It lets you manage multiple containers at once with a single command.
* Simple Setup: You define all your services (containers, networks, volumes) in a simple YAML file.
* Environment Consistency: It helps you run the same setup across different environments (local, staging, production).
* Quick Deployment: It speeds up the process of starting and stopping your entire app with just one command.
* Automates Linking: It automatically connects containers and handles their dependencies.
### 1.7
```
docker compose up --build -d
docker down
docker ps
```
### 1.10
* Share Easily: You can share images with others.
* Central Storage: Keeps all your images in one place.
* Version Control: Store different versions and go back to older ones if needed.
* Access Anywhere: Pull images from any machine.
* Automation: Works with tools to automate building and deploying images.
* Collaboration: Multiple people can use the same images.
* Scalable: Easy to manage lots of images in the cloud.

</br></br>

## TP_2
There is my repository for TP2 : [Here](https://github.com/Valentin-Meltz/tp-devops-correction-docker)

### 2.1
You can easily start and stop real services (like databases or message queues) during tests.
It helps you test your app with real dependencies, not just mock services.
After the test, the containers are automatically removed.
### 2.2
* Protect sensitive info (like passwords or API keys).
* Prevent leaks of private data.
* Meet security requirements.
* Control who can access the sensitive data.
### 2.3
* We put needs: build-and-test-backend to make sure this job runs only after the backend build and test job is done.
* If we remove it:
The job might start too early, before the backend is ready, causing errors.
In short, needs makes sure jobs happen in the right order.
### 2.4
* Share them with others.
* Backup the image online.
* Deploy it to different environments.
* Track versions for updates or rollbacks.