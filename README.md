
# CICD Flow 
![enter image description here](https://res.cloudinary.com/dgiozc0lj/image/upload/v1737433550/onpeeljsje14abzs4xw6.png)

-   **Developer pushes commit to repository**
    
    -   **Action**: The Developer commits the code to the GitHub repository.
    -   **Participants**: Developer → GitHub
-   **GitHub notifies Maintainer for code review**
    
    -   **Action**: GitHub notifies the Maintainer to review the code.
    -   **Participants**: GitHub → Maintainer
-   **Maintainer approves pull request**
    
    -   **Action**: The Maintainer reviews and approves the pull request on GitHub.
    -   **Participants**: Maintainer → GitHub
-   **GitHub merges the code into the main branch**
    
    -   **Action**: GitHub merges the approved pull request into the main branch.
    -   **Participants**: GitHub → GitHub
-   **Trigger CI/CD Pipeline**
    
    -   **Action**: GitHub triggers the CI/CD pipeline through GitHub Actions.
    -   **Participants**: GitHub → GitHubActions
-   **GitHubActions checks out the source code**
    
    -   **Action**: GitHub Actions fetches the source code from the GitHub repository.
    -   **Participants**: GitHubActions → GitHub
-   **Build image from source code**
    
    -   **Action**: GitHub Actions builds a Docker image from the source code.
    -   **Participants**: GitHubActions → GitHubActions
-   **Push image to registry**
    
    -   **Action**: GitHub Actions pushes the built image to a Docker registry.
    -   **Participants**: GitHubActions → Registry
-   **Connect to hosting server**
    
    -   **Action**: GitHub Actions connects to the hosting server where the application will run.
    -   **Participants**: GitHubActions → Server
-   **Establish connection with the server**
    
    -   **Action**: The server establishes the connection with GitHub Actions.
    -   **Participants**: Server → GitHubActions
-   **Server pulls image from registry**
    
    -   **Action**: The server pulls the updated image from the Docker registry.
    -   **Participants**: Server → Registry
-   **Image pull successful**
    
    -   **Action**: The image is successfully pulled to the server.
    -   **Participants**: Registry → Server
-   **Update service with new image**
    
    -   **Action**: The server updates the service with the newly pulled image.
    -   **Participants**: Server → Server
-   **Service updated successfully**
    
    -   **Action**: The server confirms that the service has been updated with the new image.
    -   **Participants**: Server → GitHubActions
-   **CI/CD pipeline completed**
    
    -   **Action**: GitHub Actions signals that the CI/CD pipeline has been completed successfully.
    -   **Participants**: GitHubActions → GitHub