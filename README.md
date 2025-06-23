# 📘 Webhook Subscription Documentation / Webhook 订阅服务文档

## Overview / 概述

This service allows users to subscribe via a webhook. Once subscribed, the service will POST news data to the subscriber. The request contains only a JSON body — no additional headers or parameters are used.

本服务支持用户通过 Webhook 订阅。一旦成功订阅，服务将向订阅者发送 POST 请求。请求仅包含 JSON 格式的正文，不带任何额外的请求头或参数。

---

## 🖱️ Subscription Page / 订阅页面

Users can subscribe by visiting the following page:  
用户可通过以下页面进行订阅：

**[https://subscribe.danews.workers.dev/](https://subscribe.danews.workers.dev/)**

---

## 🔁 Posting Frequency / 推送频率

- The service checks for new news **every minute**.  
  本服务**每分钟**检查一次是否有新新闻。
- If there are **multiple news items** in a minute, each will be sent as a **separate POST** request.  
  如果某一分钟有**多条新闻**，将分别发送多个 POST 请求。
- If there is **no new news**, no request will be sent for that minute.  
  如果某一分钟**没有新闻更新**，将不会发送请求。

---

## 🔗 Webhook POST Format / Webhook POST 请求格式

- **Method / 请求方式**: `POST`  
- **Content-Type / 内容类型**: `application/json`  
- **Headers / 请求头**: _None / 无_

---

## 📝 JSON Body Structure / JSON 正文结构

```json
{
  "i2": "source_id",
  "t1": "news_text"
}

```

## 💬 Contact / 联系方式

Join our Telegram group for questions, updates, or help.  
如有任何问题、需要帮助或想了解最新动态，请加入我们的 Telegram 群组：  
👉 [https://t.me/+mk9SYszWccI5MmQ1](https://t.me/+mk9SYszWccI5MmQ1)

