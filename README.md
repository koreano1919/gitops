# gitops

Repo GitOps del DevSecOps Lab: lo stato desiderato del cluster (manifest Kustomize).
ArgoCD osserva questo repo e sincronizza il cluster (deploy pull-based).
La CI del repo "app" aggiorna qui il tag dell'immagine; nessuno fa `kubectl apply` a mano.

## Struttura
- `base/`            manifest comuni (notes-api, postgres, secret)
- `overlays/dev/`    ambiente dev (namespace notes-dev, tag immagine)
- `apps/`            ArgoCD Application
