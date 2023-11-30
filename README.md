# Sample

Sample Ansible Role with Molecule

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
3. [ ] Write an Ansible role and playbook using this role to
  a. Deploy an nginx docker image 
  b. Configure this container to run as a systemd service that will run when the system boots
4. [ ] Write a readme with instructions on how to start the box and deploy the service
5. [ ] Commit and push all required files to your repo and send us the URL to your repo. 

We should be able to clone the repo and run molecule converge (will run the Ansible role) to start the environment. 

### Bonus points for 

* [ ] Good readme
* [ ] Unit/integration tests (molecule)
* [ ] Security features
* [ ] Funny memes

Please review the instructions and feel free to reach out with any questions.   

** Note ** systemd should manage the running container

 