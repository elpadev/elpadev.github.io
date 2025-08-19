---
layout: post
title: What is a Kubernetes controller?
description:
summary:
tags: [kubernetes]
---

A Kubernetes controller is a loop that compares the desired state with the current state and takes actions to make the necessary changes to the current state to equal it to the desired state.

For instance, if the cruise control of a car was deployed into Kubernetes, it would be a controller. The controller would run a loop that checks the current speed of the car and either accelerates or brakes (or doesn't do anything) to keep the car speed at a constant value.

In technical terms, the desired state is defined in a `Resource` or `Custom Resource`. The controller loop is typically a Golang program running in a container in the cluster. The loop makes API calls, e.g. to the Kubernetes API server, to find out the current state.

For example, let's say we want to deploy a database instance on AWS. We define the desired state, the database, in a `Custom Resource` called `my-db-cr`. The controller watches the `my-db-cr` and makes calls to AWS to see if such a database instance exists. If not, it makes another API call to AWS to create the database instance based on the specifications provided in `my-db-cr`.
