

```mermaid
---
title: Publishing
---
flowchart TD
    user("User(Client)")
    load_balancer[/"Load Balancer"\]
    web_servers{"Web Servers"}
    
    post_service("Post Service")
    fanout_service("Fanout Service")
    notification_service("Notification Service")
    
    post_cache[\Post Cache/]
    post_db[("Post DB")]
    
    news_feed_cache[\News Feed Cache/]

    user --> load_balancer

    load_balancer --> web_servers

    web_servers --> post_service --> post_cache --> post_db

    web_servers --> fanout_service --> news_feed_cache

    web_servers --> notification_service

    B["fab:fa-twitter for peace"]