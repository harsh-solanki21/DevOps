# Continuous Delivery

## Continuous Delivery Explained

Continuous delivery is a software development practice where code changes are automatically prepared for a release to production. It is a pillar of modern application development that expands upon continuous integration.

Key aspects:

- Deploys all code changes to a testing environment and/or a production environment after the build stage
- When properly implemented, developers always have a deployment-ready build artifact that has passed through a standardized test process
- Allows developers to automate testing beyond just unit tests
- Helps verify application updates across multiple dimensions before deploying to customers

Types of tests that can be included:

- UI testing
- Load testing
- Integration testing
- API reliability testing

Benefits of cloud implementation:

- Easy and cost-effective automation of creating and replicating multiple testing environments

<br />

## Continuous Delivery vs. Continuous Deployment

### Continuous Delivery:

- Every code change is built, tested, and pushed to a non-production testing or staging environment
- Can have multiple, parallel test stages before production deployment
- Requires manual approval for production update

### Continuous Deployment:

- Production deployment happens automatically without explicit approval

## Continuous Delivery Process

1. Code revision is committed
2. Automated flow is triggered
3. Build process runs
4. Tests are conducted
5. Update is staged
6. Developer triggers final deployment to production

## Continuous Delivery Benefits

1. **Automate the Software Release Process**

   - Automatically build, test, and prepare code changes for production release
   - More efficient and rapid software delivery

2. **Improve Developer Productivity**

   - Frees developers from manual tasks
   - Encourages behaviors that reduce errors and bugs deployed to customers

3. **Find and Address Bugs Quicker**

   - More frequent and comprehensive testing
   - Discover and address bugs earlier before they grow into larger problems
   - Easier to perform additional types of tests due to process automation

4. **Deliver Updates Faster**
   - Faster and more frequent updates to customers
   - Always have a deployment-ready build artifact that has passed through a standardized test process
