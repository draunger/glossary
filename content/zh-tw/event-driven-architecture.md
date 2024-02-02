---
title: 事件驱动架构
status: 完成
category: 概念
tags: ["架构", "", ""]
---

## 是什么

事件驱动架构是一种促进事件创建、处理和消费的软件架构。
事件指的是对应用程序状态的任何变化。
例如，在共享乘车应用中叫车就代表一个事件。
这种架构创建了一个结构，使得事件能够从其来源（请求共享乘车的应用程序）适当地路由到所需的接收方（附近可用司机的应用程序）。

## 解决的问题

随着更多数据变为实时，确保事件被捕获并路由到必须处理事件请求的适当 [服务](/service/) 的可靠方法变得越来越具有挑战性。
传统处理事件的方法通常无法保证消息被适当地路由，或者实际上是否已发送或接收。
随着应用程序开始扩展，协调事件变得越来越具有挑战性。

## 如何帮助

事件驱动架构建立了所有事件（例如 Kafka）的中央枢纽。
然后，您定义事件的生产者（来源）和消费者（接收方），中央事件枢纽保证事件的流动。
此架构确保服务保持解耦，确保事件从生产者流向消费者。
生产者将接收到的事件信息，通常通过 HTTP 协议，然后路由事件信息。