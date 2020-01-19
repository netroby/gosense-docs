# 2018-09-26  Export protocol

## Define

This document is about to define the export protocol, include server side , client side implement.

## Protocol


```json
{
    "data": {
        "Aid": 4389,
        "Title": "The title",
        "Content": "The content",
        "Publish_time": "2018-09-26 13:20:11",
        "Views": 15
    },
    "next": 4381
}
```

## Server side

the server side will expose an api, may location at

/admin/exportEndPoint

and default this api will start from aid desc, means the largest aid.

the next will to next aid lower than the current aid

## Client side

Must read the data , and perform next request at

/admin/exportEndPoint?current={next}

The next is previous got next

