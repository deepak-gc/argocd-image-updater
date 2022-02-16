# ArgoCD image updater
This action by default will update git commit id in image tag of all staging deployments  

## Inputs

### `image-tag`

Use this field, if you want to deploy any specific TAG or commit id

### `update-deployment-list`

Use this option If you want to update the image TAG only for specific deploymens

## Example usage
Will update image TAG for all staging deployments
```yaml
- name: Staging Auto deployment
  uses: 'deepak-gc/argocd-image-updater@v1'
```

Will update image TAG for `deployment-folder-name-1` & `deployment-folder-name-2`
```yaml
- name: Staging Auto deployment
  uses: 'deepak-gc/argocd-image-updater@v1'
  update-deployment-list: |
    deployment-folder-name-1
    deployment-folder-name-2
```


