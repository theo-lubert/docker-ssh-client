# Ssh-client
Very simple SSH client image

# GitLab CI

```yml
job:
  image: theolubert/ssh-client
  script:
    - echo "$SSH_PRIVATE_KEY_STAGING" > ~/.ssh/id_rsa
    - ssh $SSH_HOST 
```

# Docker

```sh
docker run --rm -it \
    -v ~/.ssh/your_key:/root/.ssh/id_rsa \
    theolubert/ssh-client bash
```