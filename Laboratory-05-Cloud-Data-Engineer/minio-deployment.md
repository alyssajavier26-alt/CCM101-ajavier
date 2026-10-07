# <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/server-16.svg" width="28" height="28" /> MinIO Object Storage Deployment

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/terminal-16.svg" width="20" height="20" /> Deployment Command

To bypass restrictive network environments blocking standard registry pulls, a local Docker image was built using `alpine:latest` with MinIO installed directly via `apk`. The container was launched using the following command:

bash
docker run -d 

-p 9000:9000 

-p 9001:9001 

--name minio-server 

-e "MINIO_ROOT_USER=cloudadmin" 

-e "MINIO_ROOT_PASSWORD=CloudNova2026!" 

minio/minio server /data --console-address ":9001"


---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/gear-16.svg" width="20" height="20" /> Network & Configuration Summary

| Parameter | Configuration Detail | Description |
| :--- | :--- | :--- |
| <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/plug-16.svg" width="16" height="16" /> **API Port** | `9000` | Handles S3 API traffic and programmatic object operations. |
| <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/browser-16.svg" width="16" height="16" /> **Console Port** | `9001` | Web Management Console port accessed via KillerCoda Port Forwarding. |
| <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/container-16.svg" width="16" height="16" /> **Storage Bucket** | `client-photos` | Dedicated S3-compatible storage bucket created for client asset uploads. |

---

### <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/key-16.svg" width="20" height="20" /> Environment Variables Explanation

* <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/person-16.svg" width="16" height="16" /> **`-e "MINIO_ROOT_USER=cloudadmin"`**: Defines the root administrative username required to log into the MinIO Web Console and perform API operations.
* <img src="https://raw.githubusercontent.com/primer/octicons/main/icons/lock-16.svg" width="16" height="16" /> **`-e "MINIO_ROOT_PASSWORD=CloudNova2026!"`**: Sets the secure administrative password for authenticating access to the Object Storage server.
