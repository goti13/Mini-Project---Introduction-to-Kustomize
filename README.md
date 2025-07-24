# Mini-Project---Introduction-to-Kustomize

# Pre-requisites

Technical Prerequisites for the Kustomize Project

To successfully complete this project on Configuration Management in Kubernetes using Kustomize, the following technical prerequisites are necessary. Each item includes a brief description and relevant links for installation and documentation.

1. Basic Understanding of Kubernetes

- Description: Familiarity with Kubernetes concepts like pods, deployments, services, etc.

- Resource: [Kubernetes Basics](https://kubernetes.io/docs/tutorials/kubernetes-basics/)

2. Docker Installation

- Description: Docker is required to run containers, which is fundamental for Kubernetes environments.

- Installation Guide: [Install Docker](https://docs.docker.com/get-started/get-docker/)

- Documentation: [Docker Documentation](https://docs.docker.com/)

3. Kubernetes Command-Line Tool (kubectl)

- Description: Essential for managing Kubernetes clusters.

- Installation Guide: [Install and Set Up kubectl](https://kubernetes.io/docs/tasks/tools/)

- Documentation: [kubectl Overview](https://kubernetes.io/docs/reference/kubectl/)


4. Minikube
   
- Description: Minikube runs a single-node Kubernetes cluster on your personal computer (including Windows, macOS, and Linux PCs) for users looking to try out Kubernetes or develop       with it day-to-day.
  
- Installation Guide: [Installing Minikube](https://minikube.sigs.k8s.io/docs/start/?arch=%2Fmacos%2Fx86-64%2Fstable%2Fbinary+download)
  
- Documentation: [Minikube Documentation](https://minikube.sigs.k8s.io/docs/)

5. Kustomize

- Description: Kustomize is a tool for customizing Kubernetes configurations. It's integrated with kubectl from v1.14.
  Installation Guide: [Install Kustomize](https://kubectl.docs.kubernetes.io/installation/kustomize/)

- Documentation: [Kustomize GitHub Repository](https://github.com/kubernetes-sigs/kustomize)

6. A Code Editor

- Description: Any text editor for writing and editing YAML files. Popular choices include Visual Studio Code, Atom, or Sublime Text.

- Recommended Editor: Visual Studio Code

- Extensions: Kubernetes and YAML extensions for ease of use.

7. Internet Connection

- Description: Required for downloading necessary tools and accessing documentation.

8. A GitHub Account (Optional)

- Description: Useful for storing and versioning your configurations.

- Sign Up: [GitHub](https://github.com/)

9. A Computer with Adequate Resources

- Description: Ensure your computer has sufficient memory and CPU resources, as Kubernetes can be resource-intensive. A minimum of 8GB RAM and 2 CPU cores is recommended for smooth operation.

# Lesson 1.1: Understanding Kubernetes Configuration

Objective: Familiarize with Kubernetes objects and configurations.

Tasks and Detailed Steps:

1. Explore Kubernetes Documentation:

- Visit the [Kubernetes Objects Overview.](https://kubernetes.io/docs/concepts/overview/working-with-objects/)

- Read about Pods, Deployments, Services, and ConfigMaps.

2. Write a Sample Pod YAML File:

- Create a file named 'mypod. yam!'

```

apiVersion: v1
kind: Pod
metadata:
  name: mypod
spec:
  containers:
  - name: mycontainer
    image: nginx
```
- Explanation: This file defines a Kubernetes Pod named 'mypod' with a single container running the NGINX image.

3. Discussion:

- Reflect on the importance of managing these configurations consistently, especially as the scale and complexity of the environment grow.

# Lesson 1.2: Introduction to Kustomize

Objective: Understand Kustomize's role in Kubernetes.

Tasks and Detailed Steps:

1. Learn About Kustomize:

- Watch a beginner-friendly video or read an article about Kustomize. Recommended: [Introduction to Kustomize.](https://kubectl.docs.kubernetes.io/guides/introduction/kustomize/)

- Key points to understand: Kustomize allows for managing Kubernetes objects with a declarative approach and helps in maintaining multiple environments with ease.

# Lesson 1.3: Setting Up the Environment

Objective: Install Kustomize and set up a basic Kubernetes cluster.

Lesson 1.3: Setting Up the Environment

Objective: Install Kustomize and set up a basic Kubernetes cluster using Minikube.

Task 1: Install Kustomize

Kustomize is a tool that allows you to customize raw, template-free YAML files for multiple purposes, essential in Kubernetes deployments.

Detailed Steps for Linux:

1. Visit the Kustomize GitHub Releases Page:

- Open your web browser and go to the [Kustomize GitHub Releases](https://github.com/kubernetes-sigs/kustomize/releases) page.

2. Select the Appropriate Version:

- Choose the version that is suitable for your Linux operating system. Look for a file that ends with 'linux_amd64.tar.gz'.
3. Download the tar.gz File:

- Click on the link for the 'Linux_amd64. tar.gz' file to download it.

4. Open Terminal:

- Open your terminal application.


5. Navigate to the Download Directory:

- Use the ' cd' command to navigate to the directory where the downloaded file is located.
  
- Example: 'cd ~/Downloads'

6. Extract the File:

- Run the command: 'tar xzf kustomize_vX.Y.Z_linux_amd64.tar.gz,replacing *X.y.Z with the version number you downloaded.

  
- This command will extract the Kustomize executable.

7. Move Kustomize to Your PATH:

- Move the extracted 'kustomize' file to a directory in your PATH for easy access. The '/usr/local/bin' directory is a common choice.

- Run: sudo mv kustomize /usr/local/bin/'

8. Check Kustomize Installation:

- Verify the installation by typing 'kustomize version' in the terminal.

- You should see the version of kustomize displayed

**For Mac Os installation**

```

brew install kustomize


```

<img width="2192" height="874" alt="image" src="https://github.com/user-attachments/assets/f90c7612-69e7-4db4-8050-058b2d6004b7" />



Task 2: Set Up a Mini Kubernetes Cluster with Minikube

Minikube is a tool that runs a single-node Kubernetes cluster locally on your machine, ideal for learning and testing purposes.

Detailed Steps:

1. Install Minikube:
- Visit the [Minikube Start](https://minikube.sigs.k8s.io/docs/start/?arch=%2Fmacos%2Fx86-64%2Fstable%2Fbinary+download) page.

- Follow the detailed instructions provided for your specific operating system (Linux, macOS, or Windows).

2. Start Minikube:
- Open your terminal.

- Run the command: 'minikube start'.

- This command initializes a local Kubernetes cluster.

3. Verify Minikube Installation:

- Once Minikube starts, verify the cluster is up and running with the command: 'kubectl get nodes'.

- This should list the nodes in your cluster, which in this case, will be a single node managed by Minikube.


Verification Task

1. Check Kustomize Version:

- Run 'kustomize version' in the terminal Ensure that it displays the installed version without errors

<img width="1752" height="116" alt="image" src="https://github.com/user-attachments/assets/b18d1c08-7b8b-4c0d-bb48-a89ffd795247" />



2. Check kubectl Version:

- Run 'kubectl version' to ensure that kubectl is properly installed and can communicate with the Minikube cluster.








