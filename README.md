Introduction
------------

A proof-of-concept of cooperation framework in a distributed system of IoT.

Scenario
--------

This implementation is set in a scenario where:

- You ask your microwave oven for a dinner by sending a voice message via whatsapp/wechat etc.
- But your cell phone is shared with your wife or even already stolen!
- So the microwave needs to tell who is the real commander and decide which food style it should provide.
- Specifically we use iOS as the client to send voice message and implement a python program to mock the microwave oven.
- It is clearly not limited in this setting, however, easy to be applied to other settings of IoT.

API
---

### Speakers List

#### GET **/speakers?offset=&limit=**

speakers list

**Request**

| parameter   | type | value              | default  | note                                                    |
|-------------|------|--------------------|----------|------------------------------------------------|
|    offset    |  int   |      page number |        0      |                                                          |
|    limit      |  int   |      speakers in one page    |    10  |                                                   |


**Status Code**

| status      | code |
|-------------|------|
| success            |  200   |
| parameter invalid      |  401   |

**Response**

```json

[
    {
        "name": "Yuannan",
        "time": "2010-04-22T18:25:33.511Z"
    },
    {

    }
]

```

### Add Speaker

#### POST **/speakers**

add one speaker

**Request**

| parameter     | type    | value                | default    | note                                                               |
|:-------------:|:------:|:--------------------:|:----------:|:------------------------------------------------------------------:|
|    name    |  String   |      name |        ""      |                                                          |
|    time      |  String   |       time stamp     |    ""  |                                                   |

**Status Code**

| status      | code |
|-------------|------|
| success            |  200   |
| parameter invalid      |  401   |

**Response**

```json

{
}

```

