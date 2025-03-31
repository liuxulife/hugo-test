---
title: "API 参考文档"
date: 2023-10-02
image: "/images/doc/doc2.jpg"
description: "完整的 API 参考文档，帮助开发者集成我们的服务"
categories: ["开发"]
tags: ["API", "开发"]
draft: false
---

# API 参考文档

本文档提供了完整的 API 参考，帮助开发者快速集成我们的服务。

## 认证方式

所有 API 请求都需要通过以下认证方式之一：

### Bearer Token 认证

```http
Authorization: Bearer YOUR_API_TOKEN
```

### API Key 认证

```http
X-API-Key: YOUR_API_KEY
```

## 基础 URL

所有 API 请求都应该使用以下基础 URL：

```
https://api.example.com/v1/
```

## 端点列表

### 用户管理

| 端点 | 方法 | 描述 |
|------|------|------|
| `/users` | GET | 获取用户列表 |
| `/users/{id}` | GET | 获取特定用户信息 |
| `/users` | POST | 创建新用户 |
| `/users/{id}` | PUT | 更新用户信息 |
| `/users/{id}` | DELETE | 删除用户 |

### 示例请求

```bash
curl -X GET "https://api.example.com/v1/users" \
  -H "Authorization: Bearer YOUR_API_TOKEN"
```

### 示例响应

```json
{
  "users": [
    {
      "id": "usr_123456",
      "name": "John Doe",
      "email": "john@example.com",
      "created_at": "2023-09-01T12:00:00Z"
    },
    {
      "id": "usr_789012",
      "name": "Jane Smith",
      "email": "jane@example.com",
      "created_at": "2023-09-02T10:30:00Z"
    }
  ],
  "pagination": {
    "total": 125,
    "page": 1,
    "per_page": 10,
    "pages": 13
  }
}
```
