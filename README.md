# jupyter-container

Adds a single-user Jupyter notebook service to your [Ansible Container](https://github.com/ansible/ansible-container) project. Designed for use with [JupyterHub](https://github.com/jupyterhub/jupyterhub).

Run the following commands
to install the service:

```
# Set the working directory to your Ansible Container project root
$ cd myproject

# Install the service
$ ansible-container install marcusianlevine.jupyter-container
```

## Requirements

- [Ansible Container](https://github.com/ansible/ansible-container)
- An existing Ansible Container project. To create a project, simply run the following:
    ```
    # Create an empty project directory
    $ mkdir myproject

    # Set the working directory to the new directory
    $ cd myproject

    # Initialize the project
    $ ansible-contiainer init
    ```

## Role Variables

* `py2_env`
    * Name of the Python 2 virtualenv added to conda
* `jupyterhub_pip_version`
    * Must match the version of JupyterHub installed on the Hub spawning from this image
* `cran_packages`
    * List of R packages to install
* `conda2_packages`
    * List of conda Python2 paackages to install
* `pip2_packages`
    * List of pip Python2 packages to install
* `extra_conda3_packages`
    * List of extra conda Python3 packages to install in addition to `conda2_packages`
* `extra_pip3_packages`
    * List of extra pip Python3 packages to install in addition to all listed in `pip2_packages`
* `extra_lab_extensions`
    * List of extra Jupyter Lab extensions (npm packages) to install


## Dependencies

*Note: this role is designed to build from a [single-user Jupyter notebook base image](https://hub.docker.com/r/jupyterhub/singleuser/)*

## License

BSD

## Author Information

Written by Marcus Levine for CKM Advisors.
