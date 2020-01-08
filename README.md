# .NET Core on Linux

This project is more of a proof of concept for myself that maybe could be presented to the my company at some point.  The project itself is meaningless, but the steps to get to an end goal has much greater significance.

## Project Management

This project will make use of the Github project tab as well as the wiki page.

## Tests

Tests will be written against the user stories in the project.  Backend tests will be written with XUnit or MSUnit and frontend tests will be written with Jest

## Data

Initial data loads will be in CSV files, but the goal is to get to SQL Server on Linux in Azure as long as cost can be kept down.  Another relational DB may be subsituted to keep costs low for the long run, but initial testing will be done on SQL Server 2017/2019. I would like to create a Graph QL implementation using Apollo or such for data.

## Backend - APIs

The backed APIs will be written in C# in .NET Core 3.x in a small microservices architecture that aligns with containerization

## FrontEnd

The frontend will be written in JS in React as a stand alone application using either Express or Next.js as the backend to communicate with the .NET Core APIs

## Authorization/Authentication

Auth will be integrated with front and back end.  OAuth will be the provider for the time being until a better IDP solution is found

## Containerization

The overall goal of this experiment outside of development on Linux is to have the application containerized.  The goal is to have each API in a container and the frontend in a container with APIs attaching to Azure SQL Server

## Orchestration

Too early to tell, but most likely kubernetes

## Deployment 

This needs to be hashed out as well.  Build tools could be gradle, Makefiles, or powershell scripts.  Currently a target of Circle CI for build and deployment.  That could change depending on cost for Azure DevOps.  Exploring the capabilities of nginx vs IIS as well as determining a final deployment location.  Azure/AWS/Digital Ocean/Raspberry Pi.  That will also determine the IaC side of things (Ansible/Terraform/Cloud Provider service).  