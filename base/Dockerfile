ARG BASEIMAGE
FROM ${BASEIMAGE}

# Disable interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Enable Vulkan support
RUN apt-get update && apt-get install -y --no-install-recommends libvulkan1 && \
	rm -rf /var/lib/apt/lists/* && \
	VULKAN_API_VERSION=`dpkg -s libvulkan1 | grep -oP 'Version: [0-9|\.]+' | grep -oP '[0-9|\.]+'` && \
	mkdir -p /etc/vulkan/icd.d/ && \
	echo \
	"{\
		\"file_format_version\" : \"1.0.0\",\
		\"ICD\": {\
			\"library_path\": \"libGLX_nvidia.so.0\",\
			\"api_version\" : \"${VULKAN_API_VERSION}\"\
		}\
	}" > /etc/vulkan/icd.d/nvidia_icd.json

# Since UE4 refuses to run as the root user under Linux, create a non-root user
RUN useradd --create-home --home /home/ue4 --shell /bin/bash --uid 1000 ue4 && \
	usermod -a -G audio,video ue4
USER ue4
