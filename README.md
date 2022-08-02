# Spot Zombie \*(Concept Program)

Defibrillator for aws ec2 spot instance

## What is this?

This program is a sidecar program for distributed instance management.
Spot instances can be killed in unexpected situations.
Therefore, when operating a spot instance, it is operated with a general ec2 instance,
and the ec2 instance checks the spot instances heartbeat
and plans to allocate a new spot instance in place of the removed spot instance.
In these cases, you will always need a managed instance.
This program automates these distributed plan within spot instances.
Therefore, if distributed storage is provided, users will always be provided with available instances.

## How to make?

It is implemented using the raft algorithm, which is one of the distributed decision algorithms.

## How to use?

### 1. Set your aws env

```sh
export AWS_REGION=ap-northeast-2
export AWS_ACCESS_KEY_ID=''
export AWS_SECRET_ACCESS_KEY=''
```

### 2. Set your initial script link

```sh
export INIT_SCRIPT_URL=''
```

### 3. Setting your plan

```yml
- Starts with one instance
```
