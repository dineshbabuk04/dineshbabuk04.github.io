---
layout: post
title: "Migrating from JGroups to gRPC at 500+ node scale"
date: 2025-01-15
description: "Why we're replacing JGroups, what we evaluated, and the architectural trade-offs that mattered most."
---

This is a sample first post. Replace this content with your own writing.

## Why we're migrating

JGroups served us well at smaller cluster sizes, but as we approach 500+ nodes
the N² connection problem becomes a real constraint...

## What we evaluated

- **etcd** for coordination and leader election
- **NATS** for messaging (hub-and-spoke instead of full mesh)
- **Consul** for service discovery

## The decision

...
