# 🚀 OpenShift Deployment Demonstration

This project demonstrates how to **import a Git repository** and **deploy an application on OpenShift** using its web console or CLI.  
It showcases the end-to-end workflow of building, deploying, and exposing a containerized application on the OpenShift platform.

---

## 🧩 Steps Involved

### 1. Import Git Repository
- The application source code is hosted on GitHub.  
- In the OpenShift console, go to **+Add → Import from Git**.  
- Provide the Git repository URL.  
- OpenShift automatically detects the build type (e.g., Node.js, Java, Python, etc.) using **Source-to-Image (S2I)**.  

### 2. Build Configuration
- OpenShift creates:
  - A **BuildConfig** (to define how the source is built)
  - An **ImageStream** (to store the resulting image)
- The source code is pulled from Git and built into a container image.  
- The built image is stored in the internal OpenShift registry.  

### 3. Deployment
- OpenShift automatically deploys the image as a **Pod** using a **DeploymentConfig** or **Deployment** resource.  
- A **Service** is created to expose the pod within the cluster.  
- A **Route** is created to make the application accessible externally via a public URL.  

### 4. Accessing the Application
- After deployment, OpenShift provides a **route URL** that can be used to access the running application in a browser.  
- Developers can:
  - View pod logs  
  - Trigger rebuilds or redeploys  
  - Scale the application (increase or decrease pod replicas)  
  - Monitor resource usage  

---

## ⚙️ Tools & Technologies Used
- **Red Hat OpenShift / OKD**  
- **Git / GitHub**  
- **Source-to-Image (S2I)**  
- **Docker / Podman** *(optional for local builds)*  
- **Web Console / oc CLI**  

---

## 🎯 Outcome
By the end of this demonstration, you will understand:
- How to connect a Git repository to OpenShift  
- How OpenShift automates build and deployment pipelines  
- How to expose and access applications running in OpenShift 
