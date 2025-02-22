Container images for running packaged UE4 projects
==================================================

The various tags of the [adamrehn/ue4-runtime](https://hub.docker.com/r/adamrehn/ue4-runtime) image provide minimal, pre-configured environments for running packaged Unreal Engine projects with full GPU acceleration via the [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-docker). (For more details on the NVIDIA Container Toolkit, see the [NVIDIA Container Toolkit primer](https://unrealcontainers.com/docs/concepts/nvidia-docker) on the Unreal Containers community hub.) Note that these images will work with packaged Linux builds **from any source**, not just builds packaged using the container images from the [ue4-docker](https://github.com/adamrehn/ue4-docker) project.

Both OpenGL+Vulkan and OpenGL+Vulkan+CUDA variants are provided. Each image variant is also available in a configuration with [VirtualGL](https://www.virtualgl.org/) bundled for displaying the output of OpenGL applications using the host system's display. See the section [Using the VirtualGL images](#using-the-virtualgl-images) for usage details.

For details on using these images to perform cloud rendering via the NVIDIA Container Toolkit, see the [Cloud rendering guide](https://unrealcontainers.com/docs/use-cases/cloud-rendering) on the Unreal Containers community hub. There are also [example Dockerfiles](https://github.com/adamrehn/ue4-example-dockerfiles) available that demonstrate various uses of Unreal Engine containers, including multi-stage build workflows that encapsulate packaged projects in variants of the `ue4-runtime` image.


## Alias tags

The following tags are provided as convenient aliases for the fully-qualified tags of common image variants:

- **latest** is an alias for **20.04-vulkan**
- **16.04-opengl** is an alias for **16.04-vulkan**
- **18.04-opengl** is an alias for **18.04-vulkan**
- **20.04-opengl** is an alias for **20.04-vulkan**
- **virtualgl** is an alias for **20.04-vulkan-virtualgl**
- **noaudio** is an alias for **20.04-vulkan-noaudio**
- **hostaudio** is an alias for **20.04-vulkan-hostaudio**


## Ubuntu 20.04 tags

- **20.04-vulkan**: Ubuntu 20.04 + OpenGL + Vulkan + PulseAudio Client + PulseAudio Server
- **20.04-cudagl11.0**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client + PulseAudio Server
- **20.04-cudagl11.0.3**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client + PulseAudio Server
- **20.04-cudagl11.1**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client + PulseAudio Server
- **20.04-cudagl11.1.1**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client + PulseAudio Server
- **20.04-cudagl11.2.0**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client + PulseAudio Server
- **20.04-vulkan-noaudio**: Ubuntu 20.04 + OpenGL + Vulkan (no audio support)
- **20.04-cudagl11.0-noaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0 (no audio support)
- **20.04-cudagl11.0.3-noaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0.3 (no audio support)
- **20.04-cudagl11.1-noaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1 (no audio support)
- **20.04-cudagl11.1.1-noaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1.1 (no audio support)
- **20.04-cudagl11.2.0-noaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.2.0 (no audio support)
- **20.04-vulkan-hostaudio**: Ubuntu 20.04 + OpenGL + Vulkan + PulseAudio Client (uses host PulseAudio Server)
- **20.04-cudagl11.0-hostaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client (uses host PulseAudio Server)
- **20.04-cudagl11.0.3-hostaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client (uses host PulseAudio Server)
- **20.04-cudagl11.1-hostaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client (uses host PulseAudio Server)
- **20.04-cudagl11.1.1-hostaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client (uses host PulseAudio Server)
- **20.04-cudagl11.2.0-hostaudio**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client (uses host PulseAudio Server)
- **20.04-vulkan-virtualgl**: Ubuntu 20.04 + OpenGL + Vulkan + PulseAudio Client + PulseAudio Server + VirtualGL
- **20.04-cudagl11.0-virtualgl**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **20.04-cudagl11.0.3-virtualgl**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client + PulseAudio Server + VirtualGL
- **20.04-cudagl11.1-virtualgl**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **20.04-cudagl11.1.1-virtualgl**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **20.04-cudagl11.2.0-virtualgl**: Ubuntu 20.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client + PulseAudio Server + VirtualGL


## Ubuntu 18.04 tags

- **18.04-vulkan**: Ubuntu 18.04 + OpenGL + Vulkan + PulseAudio Client + PulseAudio Server
- **18.04-cudagl9.2**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 9.2 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl10.0**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.0 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl10.1**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.1 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl10.2**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.2 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl11.0**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl11.0.3**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl11.1**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl11.1.1**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl11.2.0**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client + PulseAudio Server
- **18.04-cudagl11.2.1**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.1 + PulseAudio Client + PulseAudio Server
- **18.04-vulkan-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan (no audio support)
- **18.04-cudagl9.2-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 9.2 (no audio support)
- **18.04-cudagl10.0-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.0 (no audio support)
- **18.04-cudagl10.1-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.1 (no audio support)
- **18.04-cudagl10.2-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.2 (no audio support)
- **18.04-cudagl11.0-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0 (no audio support)
- **18.04-cudagl11.0.3-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0.3 (no audio support)
- **18.04-cudagl11.1-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1 (no audio support)
- **18.04-cudagl11.1.1-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1.1 (no audio support)
- **18.04-cudagl11.2.0-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.0 (no audio support)
- **18.04-cudagl11.2.1-noaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.1 (no audio support)
- **18.04-vulkan-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl9.2-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 9.2 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl10.0-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.0 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl10.1-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.1 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl10.2-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.2 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl11.0-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl11.0.3-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl11.1-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl11.1.1-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl11.2.0-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-cudagl11.2.1-hostaudio**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.1 + PulseAudio Client (uses host PulseAudio Server)
- **18.04-vulkan-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl9.2-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 9.2 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl10.0-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl10.1-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl10.2-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 10.2 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl11.0-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl11.0.3-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl11.1-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl11.1.1-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl11.2.0-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **18.04-cudagl11.2.1-virtualgl**: Ubuntu 18.04 + OpenGL + Vulkan + CUDA 11.2.1 + PulseAudio Client + PulseAudio Server + VirtualGL


## Ubuntu 16.04 tags

- **16.04-vulkan**: Ubuntu 16.04 + OpenGL + Vulkan + PulseAudio Client + PulseAudio Server
- **16.04-cudagl9.0**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.0 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl9.1**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.1 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl9.2**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.2 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl10.0**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.0 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl10.1**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.1 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl10.2**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.2 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl11.0**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl11.0.3**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl11.1**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl11.1.1**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl11.2.0**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client + PulseAudio Server
- **16.04-cudagl11.2.1**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.1 + PulseAudio Client + PulseAudio Server
- **16.04-vulkan-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan (no audio support)
- **16.04-cudagl9.0-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.0 (no audio support)
- **16.04-cudagl9.1-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.1 (no audio support)
- **16.04-cudagl9.2-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.2 (no audio support)
- **16.04-cudagl10.0-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.0 (no audio support)
- **16.04-cudagl10.1-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.1 (no audio support)
- **16.04-cudagl10.2-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.2 (no audio support)
- **16.04-cudagl11.0-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0 (no audio support)
- **16.04-cudagl11.0.3-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0.3 (no audio support)
- **16.04-cudagl11.1-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1 (no audio support)
- **16.04-cudagl11.1.1-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1.1 (no audio support)
- **16.04-cudagl11.2.0-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.0 (no audio support)
- **16.04-cudagl11.2.1-noaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.1 (no audio support)
- **16.04-vulkan-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl9.0-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.0 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl9.1-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.1 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl9.2-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.2 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl10.0-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.0 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl10.1-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.1 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl10.2-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.2 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl11.0-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl11.0.3-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl11.1-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl11.1.1-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl11.2.0-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-cudagl11.2.1-hostaudio**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.1 + PulseAudio Client (uses host PulseAudio Server)
- **16.04-vulkan-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl9.0-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl9.1-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl9.2-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 9.2 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl10.0-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl10.1-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl10.2-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 10.2 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl11.0-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl11.0.3-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.0.3 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl11.1-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl11.1.1-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.1.1 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl11.2.0-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.0 + PulseAudio Client + PulseAudio Server + VirtualGL
- **16.04-cudagl11.2.1-virtualgl**: Ubuntu 16.04 + OpenGL + Vulkan + CUDA 11.2.1 + PulseAudio Client + PulseAudio Server + VirtualGL


## Vulkan rendering

**Offscreen rendering with Vulkan requires projects built with Unreal Engine 4.25.0 or newer.** To render offscreen, specify the `-RenderOffscreen` flag when running your packaged Unreal project.

Vulkan rendering under Unreal Engine 4.24 or older will require bind-mounting the X11 socket from the host system and propagating the `DISPLAY` environment variable so that output can be rendered to a window. See the section below for details on the required `docker run` flags.


## Using the VirtualGL images

The `virtualgl` configuration of each image variant adds the following components:

- The X11 libraries needed for running applications that create X11 windows
- [VirtualGL](https://www.virtualgl.org/) itself, which provides the `vglrun` command for interposing OpenGL function calls

To run a container using a VirtualGL-enabled image, the Docker host system will need to be running an X11 server and you will need to bind-mount the host's X11 socket inside the container like so:

```bash
# Replace "adamrehn/ue4-runtime:virtualgl" with your chosen image tag
docker run --gpus=all -v/tmp/.X11-unix:/tmp/.X11-unix:rw -e DISPLAY adamrehn/ue4-runtime:virtualgl bash
```

The manner in which you need to invoke UE4 projects inside the container depends on your use case:

- If you are running the container locally on a machine with an OpenGL-enabled X11 configuration (e.g. a standard desktop installation of Ubuntu 18.04) then the [GLVND](https://github.com/NVIDIA/libglvnd) dispatch library provided by the NVIDIA base images will handle the relevant OpenGL function calls without the need to use VirtualGL. **Running UE4 projects via `vglrun` in this scenario will actually reduce performance** due to the additional interposition overheads, so be sure to run projects directly. (e.g. `./MyProject.sh`)

- If you are running the container on a remote host and are using X11 forwarding to display the window on your local machine then you will need to run UE4 projects via `vglrun` in order to ensure OpenGL functionality will work from within an SSH session. (e.g. `vglrun ./MyProject.sh`)


## Audio output

By default, the container images are configured to spawn a PulseAudio server on demand when packaged Unreal projects initialise audio output. This allows the Unreal Engine to produce audio output inside the container which can then be captured (e.g. using Pixel Streaming for Linux.) However, this behaviour may be undesirable for use cases where the host system's X11 socket is bind-mounted and output is displayed on the host, since audio output will not be propagated alongside the rendered output. The `hostaudio` configuration of each image variant overrides this default behaviour and instructs the Unreal Engine to instead use a PulseAudio socket bind-mounted from the host system, thus allowing audio output to be heard on the host. To bind-mount the PulseAudio socket from the host system, use the following flag:

```bash
"-v/run/user/$UID/pulse:/run/user/1000/pulse"
```


## Building the images from source

Building the container images from source requires Python 3.5 or newer and the dependency packages listed in [requirements.txt](https://github.com/adamrehn/ue4-runtime/blob/master/requirements.txt).

To build the images, simply run `build.py`. This will automatically query Docker Hub to retrieve the list of available [nvidia/cudagl](https://hub.docker.com/r/nvidia/cudagl) base images based on Ubuntu LTS releases and build all variants of the `adamrehn/ue4-runtime` image accordingly.


## Legal

Copyright &copy; 2019 - 2021, Adam Rehn. Licensed under the MIT License, see the file [LICENSE](https://github.com/adamrehn/ue4-runtime/blob/master/LICENSE) for details.

The file [pulseaudio-default.pa](./base/pulseaudio-default.pa) is adapted from the [default PulseAudio configuration data](https://github.com/pulseaudio/pulseaudio/blob/v12.2/src/daemon/default.pa.in), which is part of PulseAudio and is licensed under the [GNU Lesser General Public License version 2.1 or newer](https://github.com/pulseaudio/pulseaudio/blob/master/LGPL).
