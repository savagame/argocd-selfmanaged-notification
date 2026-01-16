# argocd-selfmanaged-notification

## Argo CD self-management

Argo CD can manage itself in the same way it manages other applications from the cluster. This is similar to what AutoPilot (https://argocd-autopilot.readthedocs.io/en/stable/) does under the hood. I will create an Argo CD application that points to the folder where I have our Kustomize manifests. This way, Argo CD will start monitoring that repository and folder for changes. Any new commits you make to the folder will be applied automatically.

## Installing Argo CD Notifications

Like Argo CD, the Notifications project can be installed in three different ways: via a Helm chart (https://github.com/argoproj/argo-helm/tree/master/charts/argocd-notifications), using simple manifests (https://github.com/argoproj-labs/argocd-notifications/tree/master/manifests), or via Kustomize. We will go with the Kustomize option and install it using GitOps mode.
