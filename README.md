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