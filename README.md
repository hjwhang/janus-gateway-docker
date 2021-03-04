# Janus gateway in a Docker Container


## Usage
Assuming `docker` and `docker-compose` are installed:

Build the image
```shell
$ docker build -t linagora/janus-gateway .
```

Run the container
(Insert Static IP instead of `<YOUR DOCKER IP>`)
```shell
$ DOCKER_IP=<YOUR DOCKER IP> docker-compose up
```

Where ports:
  - **80**: expose janus documentation and admin/monitoring website (port 10201 from external IP)
  - **7088**: expose Admin/monitor server
  - **8088**: expose Janus server
  - **8188**: expose Websocket server
  - **10000-10200/udp**: Used during session establishment


Edited [from this repo](https://github.com/linagora/docker-janus-gateway)
