# Day 3 - Docker multi stage build
This just shown that multiple base images can be used in a Dockerfile.
Eg. starting with a Node.js base to compile a react static app and then copying the build output onto an nginx base, which then can be used to host.

Instead of downloading the sample repo I'll just include the Dockerfile example without running.