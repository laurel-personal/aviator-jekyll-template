---
title: /weatherdata
position: 1.1
type: get
description: Get weather forecast by latitude and longitude
parameters:
  - name: lat
    content: Latitude of the location whose weather you want
  - name: lng
    content: Longitude of the location whose weather you want
content_markdown: |-
  The book will automatically be added to your reading list
  {: .success}

  Adds a book to your collection.
left_code_blocks:
  - code_block: |-
      $.post("http://api.myapp.com/books/", {
        "token": "YOUR_APP_KEY",
        "title": "The Book Thief",
        "score": 4.3
      }, function(data) {
        alert(data);
      });
    title: jQuery
    language: javascript
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
