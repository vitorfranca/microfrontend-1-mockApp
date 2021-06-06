# Microfrontend example #2 - Mock application

## Description

### Project is composed by 5 pages:
- Home
- Pricing
- Signin
- Signup
- Dashboard

### Pages are separated in different applications with different technologies:
- Marketing - React
  - Home
  - Pricing
- Authentication - React
  - Signin
  - Signup
- Dashboard - Vue

## Requirements
- Zero coupling between child projects
  - No importing of functions/object/classes/etc
  - No shared state
  - Shared libraries through MFs is ok
- Near-zero coupling between container and child apps
  - Container shouldn't assume that a child is using a particular framework
  - Any necessary communication done with callbacks or simple events
- CSS from one project shouldn't affect another
- Version control (monorepo vs separate) shouldn't have any impact on the overall project
  - some people want to use monorepos
  - some people want to keep everything in a separate repo
- Container should be able to decide to always use the latest version of a microfrontend or a specific version
  - container will always use the latest version of a child app (doesn't require a redeploy of container)
  - container can specify exactly what version of a child it wants to use (requires a redeploy to change)
- Deployment
  - Want to deploy each microfrontend independently (including the container)
  - Location of child app remoteEntry.js files must be known at buid time
  - Many front-end deployment solutions assume you're deploying a sing project - we need something that can handle multiple different ones
  - Probably need a CI/CD pipeline of some sort
  - At present, the remoteEntry.js file is fixed, need to think about caching issues