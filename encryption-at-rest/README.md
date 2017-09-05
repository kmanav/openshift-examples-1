### Work in progress

## Step 1
> Start api server with `--experimental-encryption-provider-config`  flag

## Setp 2
> Import following object info k8s as cluster-admin.    this will encrypt all configmaps going forward

```yaml
kind: EncryptionConfig
apiVersion: v1
resources:
  - resources: 
      - configmaps
    providers:
      - aescbc:
          keys:
            - name: mykey
              secret: HON5ISH9XMfFB6dnm25U0vSwxR58n7UrpxKPvmCJLTw=
 ```
 
 ## Step 3
 > Restart api server
 
 