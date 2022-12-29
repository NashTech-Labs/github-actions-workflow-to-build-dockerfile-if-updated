## GitHub Actions Workflow For Building Updated Dockerfile

This workflow will first check if the Dockerfile changed or not and based on that it will build it.

Configuration options (update accordingly):

```
        with:
          context: .
          build-args: |
            INSTALL_ALL=true
          platforms: linux/amd64
          push: false
          tags: ghcr.io/${{ github.repository }}:${{ env.IMAGE_TAG }}
```