---
id: gfm
title: Docs Page GFM
---



# GFM

## Autolink literals

www.example.com, https://example.com, and contact@example.com.

## Strikethrough

~one~ or ~~two~~ tildes.

## Table

| Endpoint            | Methods | Usage                                         |
| ------------------- | ------- | --------------------------------------------- |
| /nodes/add          | POST    | Add a DNS node                                |
| /nodes/list         | GET     | Get all DNS node                              |
| /nodes/power        | POST    | Enable or disable the node's BGP daemon       |
| /stats              | GET     | Get system stats counters (nodes/zones/users) |
| /users              | GET     | Get all users                                 |
| /user/[USER]/toggle | POST    | Toggle [USER]'s enabled state                 |

## Tasklist

* [ ] to do
* [x] done

<style>
    table {
        display: block;
        width: 100%;
        width: -webkit-max-content;
        width: -moz-max-content;
        width: max-content;
        max-width: 100%;
        overflow: auto;
        border-spacing: 0;
        border-collapse: collapse;
    }

    table tr {
        background-color: white;
        border-top: 1px solid gray;
    }

    table th {
        font-weight: 600;
    }

    table td, table th {
        padding: 6px 13px;
        border: 1px solid gray;
    }

    table tbody tr:nth-child(even) {
        background-color: #eee
    }


</style>