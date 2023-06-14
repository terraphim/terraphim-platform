# terraphim-platform
Overall repository for Terraphim AI Private Cloud Platform. 

Everything below can be build using https://earthly.dev/ or earhtly.ci.

# Background
Terraphim AI cloud is an evolution of [The Pattern](https://github.com/applied-knowledge-systems/the-pattern/) Python/RedisGears based project originally focused on medical domain/medical community. It's a private cloud platform for personal AI assistant and most of the technical details and talks from The Pattern will be applicable to Terraphim AI cloud. 

# Front end for Terraphim AI UI
Located in [terraphim-ui-svelte-ts](https://github.com/terraphim/terraphim-ui-svelte-ts.git) repository, which is a submodule of this repository, written in Svelte and TypeScript it's common across both Python based cloud platform and upcoming Tairi based self contained AI assistant

# Back end for Terraphim AI Cloud Platform
Located in [terraphim-cloud-fastapi](https://github.com/terraphim/terraphim-cloud-fastapi.git) and is basic port of [The Pattern FastAPI](https://github.com/applied-knowledge-systems/the-pattern-api/tree/511ffb481b138f6c49412aad2855e4c2e069c236) written in Python and FastAPI. I have intention to move into common Rust based Poem driven API (80% there) for both cloud and self contained AI assistant. 

# AI/ML Pipeline for the Cloud
Located in [terraphim-platform-pipeline](https://github.com/terraphim/terraphim-platform-pipeline.git) and is Python and RedisGears based pipeline for AI/ML data processing. It's a port of [The Pattern Platform](https://github.com/applied-knowledge-systems/the-pattern-platform/tree/5c272fdf7354eb1cc9dd4876c3735aee1baf724e) from medical domain to personal AI. It depends on RedisGears version 1 (rgcluster) and RedisGraph. It's a bit too complex for my liking and I am moving large parts of it into Rust, unfortunately backend dependencies are not there yet.

# Terraphim Firecracker 
[Terraphim Firecracker](https://github.com/terraphim/terraphim-firecracker) Repository to create a fully functional Firecracker VM with RedisStack and RedisGears installed. It's a base for Terraphim AI Private Cloud Platform.

# Terraphim Private Cloud 
[Terraphim Private Cloud](https://github.com/terraphim/terraphim-private-cloud) is a super fast and super simple private cloud platform based on Caddy, Bash, Firecracker VM and Redis Enterprise.

There are other dependencies like [Terraphim Automata] (https://github.com/terraphim/terraphim-platform-automata), Knowledge Graph parsers and plugins. Not all open sourced. 


# Clone, Run and update all dependencies:
```
git clone --recurse-submodules --remote-submodules https://github.com/terraphim/terraphim-platform.git
```