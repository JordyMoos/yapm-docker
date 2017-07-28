yapm in docker
==============

Getting started
---------------

### Clone this repository

```bash
$ git clone https://github.com/JordyMoos/yapm-docker.git
$ cd yapm-docker
```

### Change the required settings

- Edit `.env` and configure the domain and email.
- Also add the same domain in `client/config.json`

### Change optional settings
- Further modify `client/config.json` to your needs
- Change `server/config.yml` if you want to

### Setup the passwords

- Option one: Start with the default password
```bash
$ ./create-default-password.sh
```

- Option two: Copy your password files into the directory `./encrypted/`

### Run the password manager

```bash
$ docker-compose up --build -d
```

The first time takes a while

### You can check the logs like so

```bash
$ docker-compose logs -f
```

