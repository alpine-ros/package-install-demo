# A demonstration to install Alpine ROS packages
The live demo was performed at [ROSCon JP 2019](http://roscon.jp/) presentation!

**FIXME: Currently, this demo is setup for Intel graphic accelerator.**

1. Install [Docker](https://docs.docker.com/install/) and [docker-compose](https://docs.docker.com/compose/install/)
2. Build Docker Image
    ```
    $ cd cd neonavigation/alpine/
    $ docker-compose build
    ```
3. Enable X11 from Docker container
    ```
    $ xhost +
    ```
4. Run the demonstration
    ```
    $ docker-compose up
    ```

For comparizon, Ubuntu equivalent is placed under `neonavigation/ubuntu/`.
