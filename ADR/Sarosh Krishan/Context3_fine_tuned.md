# ADR: Modularized Monolith for FMMS

## Decision
The core of the FMMS is a modularized monolith. While this might seem like a contradiction, a monolith with modules is the best option for integrating new functionality into an existing system while maintaining the benefits of a monolith—primarily, reliability, security, and ease of deployment. By defining the core of FMMS as a modularized monolith, we can make isolated updates to individual components without the need for the entire system to undergo a rebuild and redeployment. This approach enables us
