Develope a platform where users can upload documents, assign tags for easier organization, and retrieve them. Set expiry dates on shared links. Utilize the Azure CDN to deliver content efficiently to users across various region.

# Infrastructure
<ol>
  <li>Azure Blob Storage (For storing documents)</li>
  <li>Azure Cosmos DB (For metadata, tags, and expiring link details)</li>
  <li>Azure Functions (To handle link expiration logic)</li>
  <li>Azure CDN (To efficiently deliver documents)</li>
</ol>

# Implementation Guide
1. Design Document Uploader Interface:
   - Create a user-friendly interface for document uploads and tagging.
2. Azure Blob Storage Setup: 
   - Set up Azure Blob Storage containers for document storage.
   - Implement authentication and authorization.
3. Azure Cosmos DB Integration:
   - Initialize Azure Cosmos DB.
   - Store metadata for each document upload, like the upload date, document type, user ID, and tags.
4. Develop Document Upload and Tagging Portal:
   - Build a portal where users can upload and tag documents.
   - Use SDKs to communicate with Blob Storage and Cosmos DB.
5. Develop Expiration Logic with Azure Functions:
   - Allow users to generate unique download URLs with set expiration dates.
   - The function will store the URL, associated document reference, and expiration in Cosmos DB.
6. Modify Document Retrieval:
   - Check the URL's validity and serve the document either directly from Azure Blob Storage or via Azure CDN.
7. Setup Azure CDN:
   - Create a CDN profile and endpoint.
   - Link it to Azure Blob Storage.
8. Modify Document Serving Logic with CDN:
   - Use Azure CDN to cache and deliver documents, enhancing the retrieval speed.
9. Manage Cache Lifespan:
   - Set appropriate TTL (Time to Live) for cached documents on CDN.
   -
10. Setup a CI/CD pipeline for your application and Function.
11. Setup Application insights and Azure monitor

# Diagram
![doc](./doc-app.png)
