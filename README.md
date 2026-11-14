# 基座

## SBOM（软件物料清单）
官方提供了带 SPDX 的文件，里面列出了镜像里的包，例如：
[download.opensuse.org/distribution/leap/16.0/appliances](https://download.opensuse.org/distribution/leap/16.0/appliances/)
里面有对应的 .spdx.json 文件。

```
curl -sL "https://download.opensuse.org/distribution/leap/16.0/appliances/opensuse-leap-image.x86_64-16.0.0-docker-Build5.16.docker.spdx.json" \
  | jq -r '.packages[] | "\(.name)-\(.versionInfo)"' | sort
```
