[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Apps Deployment

- **Software Deployment** is the process of publishing and preparing the program for market

## IaaS, PaaS and SaaS

### Infrastructure as a Service

- Refers to a model in which the hardware (i.e. server, storage and network) is delivered as a service for a metered cost
- **Pro:** you have complete control over every aspect of the system
- **Con:** you need sysadmin knowledge or a team of sysadmins to maintain the system since you're responsible for uptime & security

### Platform as a Service

- Refers to a model in which providing a platform to develop applications that can be delivered over the web
- **Pro:** PaaS provides a complete environment that is actively managed, letting you focus on your code
- **Con:** developers are often restricted to certain major/minor versions of packages available on the system so that the vendor can manage the platform effectively

### Software as a Service

- Refers to a model in which cloud-based software is provided at a cost
- **Pro:** the entire stack is provided by the vendor except users and associated data
- **Con:** you have limited control over the hosted application and it's often hard to integrate external workflows into the system

## Application Scaling

- **Vertical Scaling** — upgrading specs
- **Horizontal Scaling** — increasing the number of computers with the same specs

## Deployment Process

1. Prepare to deploy
2. Know your credentials and target
3. (Optional) Configure domains
4. Determine delpoyment options
5. Push the app