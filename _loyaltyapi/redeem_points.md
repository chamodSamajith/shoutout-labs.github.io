---
title: /points Redeem
position: 1.5
type: post
description: Redeem points from a user
parameters:
  - name: userId
    content: Loyalty id of the user
  - name: activityData
    content: JSON object with required key "points" and any other arbitary keys
content_markdown: |-
  Make sure you include either <b>points</b> in the <b>activityData</b> object
  {: .warning}

  Points will be redeemed from the user's loyalty account
left_code_blocks:
  - code_block: |-
      curl -X POST \
        https://api.getshoutout.com/loyaltyservice/points \
        -H 'authorization: Bearer <API_KEY>' \
        -H 'content-type: application/json' \
        -d '{
        "userId":"LOYAL-USER-001",
        "activityData":{
        "points":-17,
        "employee":"Smith",
        "location":"Colombo"
        }
      }'
    title: Curl
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "id": 3,
        "title": "The Book Thief",
        "score": 4.3,
        "dateAdded": "5/1/2015"
      }
    title: Response
    language: json
  - code_block: |-
      {
        "error": true,
        "message": "Invalid score"
      }
    title: Error
    language: json
---


