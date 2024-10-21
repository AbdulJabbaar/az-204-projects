A web application that allows users to track weather updates in real-time for their chosen cities. The system also triggers Azure Functions for alerts when a specific weather threshold is met (like if it's going to rain).

# Infrastructure
- Azure App Service Web App (Hosting the web application)
- Azure Container Registry (Storing Docker images for the app)
- Azure Container Instance (Running the containers for development/testing)
- Azure Functions (Weather alert system)
- Azure Container Apps (Running the containers in production)

# Implementation Guide
<ol>
  <li>Create an Azure App Service Web App.</li>
  <li>Develop a basic web application that uses weather APIs.</li>
  <li>Containerize the application.</li>
  <li>Publish the container image to Azure Container Registry.</li>
  <li>Test the application using Azure Container Instance.</li>
  <li>Implement an Azure Function to send alerts when a specified weather threshold is met.</li>
  <li>Integrate Azure Function with your web application.</li>
  <li>Deploy the web application to Azure Container Apps.</li>
  <li>Setup a CI/CD pipeline for your application and Function.</li>
  <li>Setup a CI/CD pipeline for your application and Function.</li>
  <li>Setup Application insights and Azure monitor</li>
  
</ol>
