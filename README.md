docker-phpab
============

Run PHP Autoload Builder (phpab) in Docker container

Build
--------------------

Build from `Dockerfile`:

    ``` sh
    sudo docker build  -t denisura/phpab .
    ```

Verify build:

    ``` sh
    sudo docker run --rm -it denisura/phpab --version
    ```

Usage
--------------------

1. Install the `denisura/phpab` container (optional - this step is performed by Docker automatically when running the container):

    ``` sh
    $ docker pull denisura/phpab
    ```

2. Define an bash alias that runs this container whenever `phpab` is invoked on the command line:

	``` sh
	$ echo "alias phpab='docker run --rm -it -v \$(pwd):/workspace denisura/phpab'" >> ~/.bashrc
	$ source ~/.bashrc
	```

3. Run phpunit as always:

	``` sh
	$ phpab --version
	```