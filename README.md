# Dimensional reduction and batch effect removal

![](https://github.com/jmacdon/Bioc2020Anno/workflows/.github/workflows/basic_checks.yaml/badge.svg)

# Workshop description


## Prerequisites

* Basic knowledge of R syntax
* Familiarity with the SummarizedExperiment class
* Basic knowledge of DelayedArray object and hdf5 storing procedure.

## Preparation

To be able to follow along with this workshop, we have created a
Docker installation that includes the devel version of R, and all
required Bioconductor packages. In order to access this, you need to
first install [Docker](https://docs.docker.com/engine/install/) on
your own computer. Once you have done that, you can then load the
Docker container for this workshop by starting Docker.

How you do this is dependent on your operating system.

### Windows

Hit the 'Windows' key (lower left on your keyboard, between Ctrl and
Alt), then type Docker. If Docker is installed you should see Docker
App highlighted - click Enter to start the App. It can take some time
to get started. You can see it's doing something by clicking on the
little caret (^) in the lower right of your screen - there should be a
little animated Docker icon which indicates it's starting. Once it is
started, open a CMD prompt by hitting the Windows key again and typing
cmd, then Enter. In the CMD prompt type

```
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 fedeago/surfingnewwave
```

You can choose any password for rstudio - that's what you will use to
log in. It will take some time for the Docker to be downloaded and
started, so you might consider doing this ahead of time.

### Linux

For Linux, it depends on how you installed. If you used a package
installer then presumably Docker will be set to start
automatically. Otherwise you need to start the Docker daemon by hand
(or set it to start automatically). There are too many variables to
give much detailed information here; for those on Linux, the
assumption is that you probably know what you are doing and can figure
it out from the Docker install page.

To start the daemon, if neccessary, do

```
sudo dockerd &
## followed by 

sudo docker run hello-world

```

If Docker is installed correctly it should print something
informative. To get the Docker container, it's the same as for
Windows.

```
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 fedeago/surfingnewwave
```

#### Knowed issue

There could be a problem running docker with the following message:

```
The system cannot find the file specified. In the default daemon configuration on Windows, the docker client must be run elevated to connect . This error may also indicate that the docker daemon is not running.

```

To work around this problem I opened the power shell as administrator and rn the following comand

```
cd "C:\Program Files\Docker\Docker"
./DockerCli.exe -SwitchDaemon
```

as described in this [stackoverflow question](https://stackoverflow.com/questions/40459280/docker-cannot-start-on-windows)

### MacOS

There is an installer for MacOS. As with Windows, follow the
instructions - it's just a regular drag'n'drop install. Once it's
installed and started, open a terminal prompt and as above type.

```
docker run -e PASSWORD=<choose_a_password_for_rstudio> -p 8787:8787 fedeago/surfingnewwave
```

## Run Docker

For all operating systems, once the Docker container is initialized,
you can access it by opening a browser and typing

```
http://localhost:8787
```

Which should present you with an RStudio login. Use rstudio as the
username and the password you used to start the Docker.


Then please open the file 'vignettes/vignette.Rmd' to start the workshop.