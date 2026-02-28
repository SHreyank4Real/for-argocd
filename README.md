# for-argocd
these will be deployed to argocd


for argocd: 
- update api.<endpint> and minio.<endpoint> before applying arcd application

add deploy keys to argocd
- ssh-keygen -t ed25519 -C "argocd" -f argocd-minio-key
- Settings → Deploy keys → Add deploy key
- Paste contents of publickey - readonly is also okay
- argocd login <endpoint>
- argocd repo add git@github.com:SHreyank4Real/for-argocd.git \
  --ssh-private-key-path argocd-minio-key