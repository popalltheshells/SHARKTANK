#To build: docker build -t linkfinder .
#To execute: docker run -it linkfinder <target_url.js> -o cli

# Use wolfi-base Chainguard image
FROM cgr.dev/chainguard/wolfi-base

# Set the working directory
WORKDIR /tmp

# Install git (needed for cloning)
RUN apk add --no-cache git

# Install Python and pip
RUN apk add --no-cache python3 py3-pip

# Clone and install LinkFinder
RUN git clone https://github.com/GerbenJavado/LinkFinder.git && \
    cd LinkFinder && \
    pip3 install -r requirements.txt

# Set the working directory to LinkFinder
WORKDIR /tmp/LinkFinder

# Set the entrypoint to run LinkFinder with the provided arguments
ENTRYPOINT ["python3", "linkfinder.py", "-i"]
