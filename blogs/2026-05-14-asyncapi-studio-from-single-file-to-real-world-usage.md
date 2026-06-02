---
title: 'AsyncAPI Studio: From Single File to Real World Usage'
url: https://www.asyncapi.com/blog/asyncapi-studio-from-single-file-to-real-world-usage?utm_source=rss
date: '2026-05-14'
author: ''
feed_url: https://www.asyncapi.com/rss.xml
---
AsyncAPI Studio was previously a single in-memory file editor. This prevented the use of relative $refs to external .avsc Avro files. This new contribution now tracks the document source, resolves relative references, and can read and write files directly to disk using the browser's File System Access API when working with a local folder.
