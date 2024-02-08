# Kubernetes Dashboard Setup

This repo provides a bash script that simplifies the deployment and management of the Kubernetes Dashboard. With this script, you can easily start, stop, and check the running status of the Dashboard, as well as access it from your browser. The script also handles the creation of an admin service account and cluster role binding, as well as the generation of a bearer token for authentication. The repo will help you to quickly set up and use the Kubernetes Dashboard without manually applying YAML manifests or configuring RBAC permissions.
## Usage

- **Kubernetes**: Ensure you have a Kubernetes cluster running locally.
- **Terminal**: You'll need a terminal emulator like Bash or Zsh.

## Setup Phase

1. **Clone this repository:**
   ```bash
   git clone git@github.com:Marknjo/kubernetes-dashboard.git
   ```
2. **Make the script executable:**
   ```bash
   chmod +x kubernetes-dashboard/dashboard.sh
   ```
3. **Create a shortcut to the script:**

   ```bash
   sudo ln -s kubernetes-dashboard/dashboard.sh /usr/local/bin/dashboard

   ```

**PS**: If you don't mind applying and deleting dashboard resources every time yo u run the script, leave line **12** and **28** uncommented

Now you're ready to set up the dashboard user and token!

## Using the Script

This script has 3 main commands

1. **`dashboard start`:** Starts the dashboard and prints the URL and access token. Copy the token and paste it into the login page.
2. **`dashboard status`:** Checks if the dashboard is running and prints the URL and token.
3. **`dashboard stop`:** Stops the dashboard and removes its resources.

**Important:**
This script is designed for Windows with WSL2, Linux, and Mac.

## Additional Notes:

- As a new bash scripter, I welcome suggestions for improvement! Feel free to share resources for further exploration.
- Make sure to log out from the client dashboard before running the stop command to avoid running into a token error.
- While I attempted using **xdg-open** for automatic browser launch, it might not work in WSL environments due to browser location on Windows. If you know a workaround, please share!

## Helpful links

- Official documentation: [Kubernetes Dashboard](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/)
- Creating a Sample User (Github Guide): [https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md](https://github.com/kubernetes/dashboard/blob/master/docs/user/access-control/creating-sample-user.md)
- Deploy Kubernetes Dashboard: [https://upcloud.com/resources/tutorials/deploy-kubernetes-dashboard](https://upcloud.com/resources/tutorials/deploy-kubernetes-dashboard)

## License

Feel free to use and modify this script!
