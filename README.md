# Full-Stack Cloud Native Development (CST8915-LAB2)

## Reflection Questions

1. What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology?

*I modified both services to load their configuration values from environment variables rather than hard-coding them, including RabbitMQ connection strings and ports. I used Node.js's dotenv package to read variables from a.env file for the order-service. To read the port value from the.env file, I introduced the dotenv package to the product-service in Rust. In order to treat RabbitMQ as a backend service rather than an integrated dependency, the order-service was also set up to connect to it via an external connection string.*

2. Why is it important to use environment variables instead of hard-coding configurations in your application?

*Environment variables allow to switch configuration parameters across development, testing, and production environments without changing the source code. This improves portability, maintainability, and security. By simply altering the environment variables, the same software may execute in several environments, facilitating easier deployments.*

3. Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?

*Every microservice has its own isolated codebase, dependencies, and version history due to distinct repositories. Teams may separately create, test, and launch services because to this separation, which avoids close integration. By allowing services to develop according to their own schedules, using various technology stacks or scaling techniques, while still integrating as a component of the wider system, it also promotes scalability.*

### Youtube Demo Link: 
https://youtu.be/n-G2uzp12rw

### Order-Service:
https://github.com/nada0038/order-service-Lab2

### Product Service:
https://github.com/nada0038/product-service-Lab2

### Store Front:
https://github.com/nada0038/store-front-Lab2



