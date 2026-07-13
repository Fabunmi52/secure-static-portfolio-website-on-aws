# 10. Lessons learned and roadmap

## Lessons learned

1. Build and verify the network infrastructure before troubleshooting the application. A correctly configured VPC, subnet, route table, and Internet Gateway are the foundation of a successful deployment.

2. A public IP address alone does not make a server accessible. Security Groups and Route Tables must also be configured to allow the required inbound and outbound traffic.

3. Restrict administrative access whenever possible. Limit SSH (port 22) access to your own public IP address instead of allowing access from anywhere on the internet.

4. DNS propagation is not instantaneous. Always verify DNS records using tools like DNSChecker before troubleshooting website or SSL issues.

5. HTTPS should be implemented as part of the deployment process, not as an afterthought. Securing web traffic with SSL/TLS protects user data and builds trust.

6. Monitor AWS resource usage and costs from the beginning of every project. Selecting the appropriate instance type and cleaning up unused resources helps avoid unexpected charges.

7. Store source code and documentation outside the EC2 instance. Use platforms such as GitHub for version control and documentation to prevent data loss if the server is terminated.

8. Capture screenshots throughout the deployment process as evidence of your work, but remove or mask sensitive information such as public IP addresses, account IDs, and domain management details before sharing publicly.

9. Validate every deployment step before moving to the next. Confirm that networking, DNS, Nginx, and HTTPS are functioning correctly to simplify troubleshooting and reduce deployment errors.

10. Documentation is just as important as deployment. Recording architecture decisions, implementation steps, challenges, and lessons learned makes projects easier to maintain, demonstrate, and reproduce in the future.
