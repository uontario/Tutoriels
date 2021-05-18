# AWS CLI

## :o: Installation

https://aws.amazon.com/fr/cli/

:m: Avec `package Managers`

:pushpin: [MacOS](https://formulae.brew.sh/formula/awscli)

```
$ brew install awscli
```

:pushpin: [Windows](https://chocolatey.org/packages/awscli)

```
$ choco install awscli
```

* Test de l'installation

```
$ aws --version
aws-cli/2.2.5 Python/3.9.5 Darwin/20.4.0 source/arm64 prompt/off
```

## :one: Configuration ~/.aws/config

* Afficher la liste des régions

```
$ aws ec2 describe-regions
```

* [Configurer](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html) la  région par défault (dans notre example ca-central-1)

```
$ aws configure
AWS Access Key ID [None]: ****************DN2Q
AWS Secret Access Key [None]: ****************nl3Z
Default region name [None]: ca-central-1
Default output format [None]:
```

* avec un profil

```
$ aws configure --profile mon-profil
AWS Access Key ID [None]: ****************DN2Q
AWS Secret Access Key [None]: ****************nl3Z
Default region name [None]: ca-central-1
Default output format [None]:
```

:bulb: pour initialiser un profil par défaut, assigner le profil à la variable d'environemment `AWS_PROFILE`

```
$ export AWS_PROFILE=mon-profil
```

## :two: Utilisation

:bulb: `[ --profile <profile-name> ]` est a rajouter si les profils sont geres

:pushpin:  Groupes de Sécurité

* Liste les groupes de sécurités  

```
$ aws ec2 describe-security-groups | grep GroupName  [ --profile <profile-name> ]
```

* Décrit le groupe de sécurité `default`

```
$ aws ec2 describe-security-groups --group-names default  [ --profile <profile-name> ]
```

:pushpin:  Instances

```
$ aws ec2 describe-instances --output table  [ --profile <profile-name> ]
```

:pushpin:  [Authoriser](https://docs.aws.amazon.com/cli/latest/reference/ec2/authorize-security-group-ingress.html) un port en entree

```
$ aws ec2 authorize-security-group-ingress --group-name <group-name> \
                                           --protocol tcp --port 9021 \
                                           --cidr 0.0.0.0/0 [ --profile <profile-name> ]
```

:pushpin:  [Revoquer](https://docs.aws.amazon.com/cli/latest/reference/ec2/revoke-security-group-ingress.html) un port en entree

```
$ aws ec2 revoke-security-group-ingress --group-name <group-name> \
                                        --protocol tcp --port 9021 \
                                        --cidr 0.0.0.0/0  [ --profile <profile-name> ]
```

## :o: EKSTL Installation

https://docs.aws.amazon.com/eks/latest/userguide/getting-started-eksctl.html

:m: Avec `package Managers`

:pushpin: [MacOS](https://formulae.brew.sh/formula/awscli)

```
$ brew install weaveworks/tap/eksctl
```

:pushpin: [Windows](https://chocolatey.org/packages/awscli)

```
$ choco install eksctl
```
