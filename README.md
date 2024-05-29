# GitHub Actions
## [env-system-alternative](.github/workflows/env-system-alternative.yaml)
If you have an organization on the free plan and you are using a private repository, you cannot use GitHub Environment. You need to use a dynamic Environment instead. It includes a solution for this. If you want to use GitHub Environment, you need to upgrade to the paid version.

|Prod Secrets|Value|
|-|-|
|**PROD**_OPENVPN_CONFIG|.ovpn client file content.|
|**PROD**_SSH_HOST|Instance private ip information because you are using OpenVPN.|
|**PROD**_SSH_USERNAME|Will connect to Instance and restricted username.|
|**PROD**_SSH_PRIVATE_KEY|Private key to be used when connecting to the instance.|
|**PROD**_SSH_PORT|The port information to make the SSH connection. It is usually used as 22. It would be good if you change this port for security.|

|Dev Secrets|Value|
|-|-|
|**DEV**_OPENVPN_CONFIG|.ovpn client file content.|
|**DEV**_SSH_HOST|Instance private ip information because you are using OpenVPN.|
|**DEV**_SSH_USERNAME|Will connect to Instance and restricted username.|
|**DEV**_SSH_PRIVATE_KEY|Private key to be used when connecting to the instance.|
|**DEV**_SSH_PORT|The port information to make the SSH connection. It is usually used as 22. It would be good if you change this port for security.|

|Test Secrets|Value|
|-|-|
|**TEST**_OPENVPN_CONFIG|.ovpn client file content.|
|**TEST**_SSH_HOST|Instance private ip information because you are using OpenVPN.|
|**TEST**_SSH_USERNAME|Will connect to Instance and restricted username.|
|**TEST**_SSH_PRIVATE_KEY|Private key to be used when connecting to the instance.|
|**TEST**_SSH_PORT|The port information to make the SSH connection. It is usually used as 22. It would be good if you change this port for security.|

## [openvpn-with-ssh](.github/workflows/openvpn-with-ssh.yaml)
In many OpenVPN solutions, the .ovpn client file must be included in the repository. This is not a very logical approach. You can use OpenVPN for this by defining the client file as secret.

|Secrets|Value|
|-|-|
|OPENVPN_CONFIG|.ovpn client file content.|
|SSH_HOST|Instance private ip information because you are using OpenVPN.|
|SSH_USERNAME|Will connect to Instance and restricted username.|
|SSH_PRIVATE_KEY|Private key to be used when connecting to the instance.|
|SSH_PORT|The port information to make the SSH connection. It is usually used as 22. It would be good if you change this port for security.|
