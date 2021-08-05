# dotnet-docker-win

Documentation

Create => Main Project  .NET 5.0 (Disable Docker Support)

Create Solutions

Create => dev_v1 (API)

Create => dev_v2 (Same Config)

Create => dev_v3 (Same Config)

Create => dev_v4 (Same Configure)

Changes to make:

1. Create Common directory in the root path.
- Copy docker-compose files to Common directory.
- Main Project (dev_v1) => Add Docker support 
- Main Project (dev_v1) Add Container Orchestrator Support 
- Update docker-compose path in the Main Project.sln file.

2. Copy content of Docker-compose.override to docker-compose.
- Set Ports (5000:80 && 5001:80)
- Remove https links in ASPNETCORE_URLS.(443)
- Comment httpsredirection() line in Startup.cs.

