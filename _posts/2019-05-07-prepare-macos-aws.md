---
layout: post
title: "Prepare MacOS for interacting with AWS EKS"
published: true
---
![alt text](https://github.com/mhmdio/mhmdio.github.io/raw/master/images/amazoneks.jpg)


Amazon EKS clusters require kubectl and kubelet binaries and the aws-iam-authenticator binary to allow IAM authentication for your Kubernetes cluster.

If you do not already have Homebrew installed on your Mac, install it with the following command.

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## INSTALL KUBERNETES TOOLS

- kubectl
```bash
brew install kubectl
```

- aws-iam-authenticator
```bash
brew install aws-iam-authenticator
```

- jq
```bash
brew install jq
```

- envsubst
```bash
brew install gettext
brew link --force gettext
```

## Verify

```bash
for command in kubectl aws-iam-authenticator jq envsubst
  do
    which $command &>/dev/null && echo "$command in path" || echo "$command NOT FOUND"
  done
```