# feefo
This repository contains a sample app to be built and deployed as an image to docker hub.

## CI
The GitHub action workflow builds and publishes the image to a docker registry, however in concideration is building a AWS ECR and publishing it there.

This can be extended with unit-tests or e2e tests if built and connected with the CD pipeline

## Infrastructure
A sample infrastructure, on which a microserviced solution may reside can be seen here https://github.com/georg-nikola/terraform-eks

## CD
There are numerous solutions, however the best chosen for a highly robust with extensible cost-efficieny options would be EKS.

The chosen IaC solution in this case is terraform as it has continuos contributions. Other considered was eksctl, which is easier to use but with a tradeoff for configuration oppurtunities on the provisioned clusters.

Variants of Development, Staging and Production environments can be built from the sample depending on the needs of the project

A suitable deployment strategy would again utilize GitHub actions with steps on PR/Merge to deploy on the corresponding environments
