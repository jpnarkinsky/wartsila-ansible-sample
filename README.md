# Sample

Sample Ansible Role with Molecule

# MEME Server

This ansible role will starts an nginx server that serves a meme.  
Whether the meme is funny will be left as an exercise for the observer.

The ansible role/playbook assumes that the docker server, etc. will be running 
on the local machine, therefore there's no inventory.  The role I've created
will create a systemd service called `docker.nginx` and start said service. The 
service is created using a dockerfile (in templates/docker) and alters the 
"official" docker nginx image with a custom html page that displays a meme.  

## Disclaimers

Frankly, it's been about 5 years since I used Ansible at all, and I've
never used `molecule`. My intention had been to bring myself up to speed, 
but due to another offer that is demanding a swift decision I decided
it was better to get this in, even though it's not really complete, 
hoping for the best.  I will continue to work on enhancing it further 
if there's still interest.

In part, this is necessary because it seems like molecule (running in a docker)
doesn't like the way I laid out the project, and can't handle me expecting to 
make changes to the **local** systemd.  I just don't have time to figure 
all that out now that I'm on such a short timeline.

## Prerequisites

1. A linux-ish system with Docker installed and configured in systemd.  Also, needs to have a reasonably modern version of Python installed.

2. Install dependencies and setup a venv:

```
python -m venv venv
. venv/bin/activate
pip install -U pip
pip install -r requirements.txt
```

~~3. Run unit tests~~

>
 [!WARNING] these don't work.
```
molecule test
```

## Instructions

```
# In the repository root
ansible-playbook main.yaml
```

####### ORIGINAL README FOLLOWS ########

### Instructions


## Requirements

Setup Ansible with pip.

```
python -m venv venv
. venv/bin/activate
pip install -U pip
pip install -r requirements.txt
```

**Centos 7 on Docker requires cgroupsv1**

## Testing

`molecule test`

## Role Variables

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

## Dependencies

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

## License

UNLICENSED

## Author Information

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

## Instructions

### Attached is a barebones Ansible repo with molecule testing.   

The instructions for the homework assignment are as follows: 

1. [X] Create a public repo, either in Github or Bitbucket, and store your work there.
  a. good commit 
  b. message atomic commits
2. [X] Download and save the attached file contents to your repo
3. [X] Write an Ansible role and playbook using this role to
  a. Deploy an nginx docker image 
  b. Configure this container to run as a systemd service that will run when the system boots
4. [X] Write a readme with instructions on how to start the box and deploy the service
5. [X] Commit and push all required files to your repo and send us the URL to your repo. 

We should be able to clone the repo and run molecule converge (will run the Ansible role) to start the environment. 

### Bonus points for 

* [X] Good readme
* [ ] Unit/integration tests (molecule)
* [X] Security features
* [X] Funny memes

Please review the instructions and feel free to reach out with any questions.   

** Note ** systemd should manage the running container

 