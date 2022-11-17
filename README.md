# argocd-kustomize

Step 1: Clone repo

Step 2: Install ArgoCD with kustomize

kustomize build . | kubectl apply -n argocd -f -

Step 3: Clone and change the below repo visibility to private.

https://github.com/abkura/argocd-kustomize-private

Step 4: Update the below line to point to the above private repo

https://github.com/abkura/argocd-kustomize-public/blob/main/kustomization.yaml#L6

Step 5: Add the above repository in ArgoCD passing required credentials

Step 6: Create ArgoCD application using below file

https://github.com/abkura/argocd-kustomize/blob/main/argocd-application.yaml

Issue encountered:

rpc error: code = Unknown desc = `bash -c kustomize build .` failed exit status 1: Error: accumulating resources: 
accumulation err='accumulating resources from 'https://github.com/abkura/argocd-kustomize-private.git': yaml: 
line 173: mapping values are not allowed in this context': git cmd = '/usr/bin/git fetch --depth=1 origin HEAD': exit status 128
